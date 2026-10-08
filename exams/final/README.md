# Final project: An explanation audit of a predictive model

## Overview

The final project applies the whole course to one model. Students audit a model of their choice: They decide which stakeholder question the audit answers, test whether an interpretable model would be enough, explain the model with at least three methods, test the explanations for reliability and close with a model card and a recommendation. The project is done alone or in pairs.

## Learning outcomes assessed

The project assesses the course learning outcomes on choosing between interpretable and explained models, implementing and comparing explanation methods, testing the reliability of explanations and documenting a model.

## Options

### Option 1: A tabular model from your own field

Choose a public tabular dataset from the UCI Machine Learning Repository or OpenML that relates to your programme. Train an ensemble model, measure the frontier against interpretable models, explain it with SHAP, LIME and counterfactuals, and run the benchmark of Day 4.

### Option 2: A shortcut hunt in images

Modify the lesion generator of Day 1 so that a different shortcut is planted, such as a border or a texture. Train a network, find the shortcut with the methods of Day 3, quantify it with counter-slices and report which methods would have caught it.

### Option 3: A fairness audit with recourse

Build or choose a credit, hiring or admission dataset with a protected attribute. Measure group disparities, locate the channel with group-wise attributions, verify it by ablation and write actionable recourse statements for three rejected cases.

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
