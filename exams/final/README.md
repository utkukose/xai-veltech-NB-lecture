# Final project: An explanation audit of a predictive model

## Overview

The final project applies the whole course to one model. Students audit a model of their choice: They decide which stakeholder question the audit answers, test whether an interpretable model would be enough, explain the model with at least three methods, test the explanations for reliability and close with a model card and a recommendation. The project is done alone or in pairs.

## Learning outcomes assessed

The project assesses the course learning outcomes on choosing between interpretable and explained models, implementing and comparing explanation methods, testing the reliability of explanations and documenting a model.

## Options

Each option comes with a short first step in Python. The examples run in Colab as they are and stop where the project begins.

### Option 1: A tabular model from your own field

Choose a public tabular dataset from the UCI Machine Learning Repository or OpenML that relates to your programme. Train an ensemble model, measure the frontier against interpretable models, explain it with SHAP, LIME and counterfactuals, and run the benchmark of Day 4.

**A first step.** The code below compares a tree of depth 2, a logistic regression and a random forest on the wine data of scikit-learn, the first measurement of the frontier between readability and accuracy.

```python
from sklearn.datasets import load_wine
from sklearn.model_selection import train_test_split
from sklearn.ensemble import RandomForestClassifier
from sklearn.linear_model import LogisticRegression
from sklearn.tree import DecisionTreeClassifier
from sklearn.pipeline import make_pipeline
from sklearn.preprocessing import StandardScaler

# Any tabular dataset of your field fits here; the wine data of scikit-learn stand in for it
X, y = load_wine(return_X_y=True, as_frame=True)
X_tr, X_te, y_tr, y_te = train_test_split(X, y, test_size=0.3, stratify=y, random_state=0)

models = {"tree of depth 2": DecisionTreeClassifier(max_depth=2, random_state=0),
          "logistic regression": make_pipeline(StandardScaler(), LogisticRegression(max_iter=1000)),
          "random forest": RandomForestClassifier(n_estimators=300, random_state=0)}
for name, model in models.items():
    model.fit(X_tr, y_tr)
    print(f"{name:20s} test accuracy {model.score(X_te, y_te):.3f}")
```

### Option 2: A shortcut hunt in images

Modify the lesion generator of Day 1 so that a different shortcut is planted, such as a border or a texture. Train a network, find the shortcut with the methods of Day 3, quantify it with counter-slices and report which methods would have caught it.

**A first step.** The code below plants a frame in the images of one class, trains a linear model on the pixels and shows how much the frame alone adds to the score of that class.

```python
import numpy as np
import matplotlib.pyplot as plt
from sklearn.linear_model import LogisticRegression

rng = np.random.default_rng(0)

def make_images(n, size=16):
    """Bright blobs on a dark background, slightly larger in class 1. A frame is planted in class 1 as the shortcut."""
    X, y = [], []
    rows, cols = np.mgrid[0:size, 0:size]
    for _ in range(n):
        label = int(rng.integers(0, 2))
        r, c = rng.uniform(5, 11, 2)
        img = np.exp(-((rows - r) ** 2 + (cols - c) ** 2) / (2 * (2.5 + 0.3 * label) ** 2))
        if label == 1 and rng.random() < 0.9:              # the frame appears in 90 percent of class 1
            img[0, :] = img[-1, :] = img[:, 0] = img[:, -1] = 0.8
        X.append(img + rng.normal(0, 0.1, img.shape))
        y.append(label)
    return np.array(X), np.array(y)

X, y = make_images(600)
model = LogisticRegression(max_iter=2000).fit(X.reshape(len(X), -1), y)
w = model.coef_.reshape(16, 16)
frame = np.zeros((16, 16), bool)
frame[0, :] = frame[-1, :] = frame[:, 0] = frame[:, -1] = True
print(f"training accuracy {model.score(X.reshape(len(X), -1), y):.3f}")
print(f"a frame of brightness 0.8 adds {0.8 * w[frame].sum():.1f} to the score of class 1")

plt.imshow(w, cmap="coolwarm")
plt.colorbar(label="weight")
plt.title("Weights of the linear model, pixel by pixel")
plt.show()
```

### Option 3: A fairness audit with recourse

Build or choose a credit, hiring or admission dataset with a protected attribute. Measure group disparities, locate the channel with group-wise attributions, verify it by ablation and write actionable recourse statements for three rejected cases.

**A first step.** The code below builds hiring data in which past decisions favoured one group, trains a model without the group and compares the selection rates of the two groups.

```python
import numpy as np
import pandas as pd
from sklearn.linear_model import LogisticRegression

rng = np.random.default_rng(0)
n = 2000
group = rng.choice(["A", "B"], n, p=[0.6, 0.4])                     # the protected attribute
skill = rng.normal(0, 1, n)
district = np.where(group == "A", rng.normal(1, 1, n), rng.normal(-1, 1, n))   # a proxy of the group
# Past decisions favoured group A, so the labels carry the bias
hired = (skill + 0.8 * (group == "A") + 0.5 * rng.normal(0, 1, n) > 0.5).astype(int)

data = pd.DataFrame({"skill": skill, "district": district, "group": group, "hired": hired})
model = LogisticRegression().fit(data[["skill", "district"]], data["hired"])   # the group is not a feature
data["selected"] = model.predict(data[["skill", "district"]])
print(data.groupby("group")[["hired", "selected"]].mean().round(3))
print("weight of the district in the model:", round(float(model.coef_[0][1]), 3))
```

## Proposal

Before starting, send a proposal of about 150 words that names the option, the dataset and the question the project answers. The proposal is optional during self-study and expected during an active delivery.

## Deliverables

The submission consists of one Colab notebook that runs from top to bottom without errors, and a technical report of 2000 to 3000 words that follows [the report template](../REPORT_TEMPLATE.md). Figures in the report must be produced by the notebook.

## Evaluation

| Criterion | Weight |
|---|---|
| The audit answers a stakeholder question rather than listing methods | 25 % |
| Explanations are reported with fidelity, seeds and settings | 20 % |
| The reliability section contains at least one genuine negative finding | 25 % |
| The model card is accurate and its limitations are specific | 15 % |
| The recommendation follows from the evidence | 15 % |

## Submission

During an active delivery of the course, the notebook and the report are sent within one week after Day 5 to utkukose@sdu.edu.tr or utkukose@gmail.com, with the subject line "VTR UGE 21 Explainable Artificial Intelligence final project".
