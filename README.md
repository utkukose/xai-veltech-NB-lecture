<div align="center">

# Explainable Artificial Intelligence

**VTR UGE 21 Value Added Course, Vel Tech Rangarajan Dr. Sagunthala R&D Institute of Science and Technology, Chennai, India**

*A five-day course on explaining machine learning models, with lecture pages, animations, interactive labs, Colab notebooks and a Python track for beginners*

![last update](https://img.shields.io/badge/last%20update-October%202026-B97813) ![course code](https://img.shields.io/badge/course%20code-VTR%20UGE%2021-1F5F8B) ![format](https://img.shields.io/badge/format-5%20days-1F5F8B) ![delivery](https://img.shields.io/badge/delivery-synchronous%20and%20asynchronous-0E7A78) ![notebooks](https://img.shields.io/badge/notebooks-Google%20Colab-F9AB00) ![content](https://img.shields.io/badge/content-CC%20BY%204.0-555555) ![code](https://img.shields.io/badge/code-MIT-555555)

**This course is updated in line with current developments in the field. Last update: October 2026.**

**Prof. Dr. Utku Kose**

Full Professor, Department of Computer Engineering, Süleyman Demirel University, Isparta, Türkiye  
Founding Director, AI Application and Research Center (YAZEM), Süleyman Demirel University  
Head of the Computer Science Division, Department of Computer Engineering, Süleyman Demirel University  
Additional affiliations: University of North Dakota (USA), Universidad Panamericana (Mexico City, Mexico), Vel Tech University (Chennai, India)  
IEEE Senior Member, ACM Professional Member

[ORCID 0000-0002-9652-6415](https://orcid.org/0000-0002-9652-6415) | [utkukose.com](https://www.utkukose.com) | [github.com/utkukose](https://github.com/utkukose)

[utkukose@sdu.edu.tr](mailto:utkukose@sdu.edu.tr) | [utku.kose@und.edu](mailto:utku.kose@und.edu) | [ukose@up.edu.mx](mailto:ukose@up.edu.mx) | [utkukose@gmail.com](mailto:utkukose@gmail.com)

</div>

## About the course

Machine learning models now support decisions in medicine, finance, engineering and public services, and many of them are too complex to be read directly. Explainable artificial intelligence (XAI) develops methods that describe what such models do and why, and it develops the means to check whether those descriptions are right [1, 2]. The course is built around one argument: An explanation is a second model of the first model, and like any model it can be wrong. Day 1 separates interpretable models from explained ones and measures when an interpretable model is enough [3]. Day 2 builds the model-agnostic methods from first principles, Day 3 explains deep networks, Day 4 attacks every explanation built so far, and Day 5 turns the results into records, dashboards and model cards that can be defended [4, 5]. Three of the four datasets of the course are synthetic with a known ground truth, so that every explanation can be graded rather than admired.

## Use in other courses

These materials were prepared for the value added course Explainable Artificial Intelligence delivered at Vel Tech Rangarajan Dr. Sagunthala R&D Institute of Science and Technology. They are openly available: Anyone may use and adapt them in courses of related content, at any level, with attribution as described in the license section. Instructors who adopt them are welcome to report errors or suggest improvements through the issues of this repository.

## A look inside

Every lecture page holds an interactive scene that turns a central idea of the day into a small story with buttons. A click on a picture opens its scene on the lecture page.

<table><tr><td width="33%" valign="top"><a href="https://utkukose.github.io/xai-veltech-NB-lecture/days/day-01/lecture.html#scene"><img src="days/day-01/figures/scene.png" alt="Day 1 interactive scene: Two doctors, one model"></a><br><sub>Day 1: Two doctors, one model</sub></td><td width="33%" valign="top"><a href="https://utkukose.github.io/xai-veltech-NB-lecture/days/day-02/lecture.html#scene"><img src="days/day-02/figures/scene.png" alt="Day 2 interactive scene: Shuffle a column"></a><br><sub>Day 2: Shuffle a column</sub></td><td width="33%" valign="top"><a href="https://utkukose.github.io/xai-veltech-NB-lecture/days/day-03/lecture.html#scene"><img src="days/day-03/figures/scene.png" alt="Day 3 interactive scene: Cover a part of the image"></a><br><sub>Day 3: Cover a part of the image</sub></td></tr><tr><td width="33%" valign="top"><a href="https://utkukose.github.io/xai-veltech-NB-lecture/days/day-04/lecture.html#scene"><img src="days/day-04/figures/scene.png" alt="Day 4 interactive scene: What a postcode reveals"></a><br><sub>Day 4: What a postcode reveals</sub></td><td width="33%" valign="top"><a href="https://utkukose.github.io/xai-veltech-NB-lecture/days/day-05/lecture.html#scene"><img src="days/day-05/figures/scene.png" alt="Day 5 interactive scene: Four letters"></a><br><sub>Day 5: Four letters</sub></td></tr></table>

The interactive labs of the first three days, as they appear in the browser.

<table><tr><td width="33%"><a href="days/day-01/README.md"><img src="days/day-01/screenshots/lab.png" alt="Day 1 interactive lab"></a><br><sub>Day 1: Glass-box lab</sub></td><td width="33%"><a href="days/day-02/README.md"><img src="days/day-02/screenshots/lab.png" alt="Day 2 interactive lab"></a><br><sub>Day 2: Explanation lab</sub></td><td width="33%"><a href="days/day-03/README.md"><img src="days/day-03/screenshots/lab.png" alt="Day 3 interactive lab"></a><br><sub>Day 3: Saliency lab</sub></td></tr></table>

## Who the course is for

The course is written for undergraduate and graduate students of engineering, science and health programmes and for self-learners anywhere. It assumes no earlier programming experience: The start-here notebook and the five Python steps teach the Python needed for the course, always through the problem of the day. Students who already program in Python can treat the Python steps as a quick review and spend the time on the exercises and the application challenges.

## Course learning outcomes

On completion, students are expected to distinguish interpretable models from post-hoc explanations and choose between them on measured evidence, to implement permutation importance, partial dependence, accumulated local effects, LIME, Shapley values, counterfactuals and anchors from first principles, to explain image and text models with gradients, Grad-CAM, relevance propagation, attention and concept probes, to test explanations for calibration, shift, adversarial fragility and fairness with a benchmark against a random baseline, and to document a model with reproducible explanation records and a model card. In Python, students are expected to write and debug short programs with variables, lists, dictionaries, loops and functions, to use NumPy, pandas, Matplotlib and scikit-learn for data and models, and to read a small neural network written in NumPy, with its forward and backward pass.

## How the course works

Each day has an overview page in its folder, which links to four materials with distinct roles. The lecture page explains the concepts with animations, knowledge checks and review cards. The Colab notebook holds the Python step and the hands-on work with real or carefully constructed data. Its exercises give immediate feedback, reference solutions sit in collapsed cells, and open questions invite observations on the results. Each section links back to the part of the lecture it applies, and each can be started on its own, because its first cell runs the code of the earlier sections. The interactive lab practises the ideas in several parts: A simulation that runs in the browser, a short classification task, a calculation by hand, and calculators that repeat the worked examples of the lecture step by step, with sliders for their numbers. The lecture page opens each part at the place where it belongs. The lab closes with a self-assessment and an exportable learning log. The PDF lecture notes collect the Python step and the lecture in one printable file. The course works in two modes. In a synchronous delivery, each day runs as one session of about three hours, following the live session plan on the overview page. In asynchronous study, the same materials are used along the study path on the overview page, which lists every activity with a suggested time.

Start with [`start-here/`](start-here/README.md) if you have never programmed, then follow the days in order. The course site at <https://utkukose.github.io/xai-veltech-NB-lecture/> links every page and keeps track of the days you have completed in your browser.

## The diagnosis case, the project of the course, day by day

One project runs through the whole week: the explanation audit of the models of one diagnostic task, the diagnosis of breast tumours from 30 measurements of cell nuclei, with an imaged version in which a planted marker leaks the label. Each day first teaches its methods on small examples and then takes the audit one stage further, in a lecture section titled *The diagnosis case, stage N*. The figure shows the five stages, and the table links each stage to its section.

<p align="center"><img src="assets/diagnosis_case_stages.png" width="860" alt="The five stages of the diagnosis case through the week"></p>

| Day | Stage of the project | Methods | Result |
|---|---|---|---|
| [Day 1](https://utkukose.github.io/xai-veltech-NB-lecture/days/day-01/lecture.html#the-diagnosis-case-stage-1-readable-models-and-a-shortcut-found) | Readable models of the tumour data, and a model of the lesion images whose weights reveal a shortcut. | A threshold rule, a logistic regression, a tree, a random forest for comparison, a map of the weights | 31 values of the logistic regression reach an accuracy of 0.986, against 0.958 for the forest; 4.7 percent of the weight of the lesion model lies on a marker of 1.6 percent of the image |
| [Day 2](https://utkukose.github.io/xai-veltech-NB-lecture/days/day-02/lecture.html#the-diagnosis-case-stage-2-the-random-forest-explained-from-the-outside) | The random forest stays closed and is questioned through its predictions alone. | Permutation importance, partial dependence and individual conditional expectation curves, LIME, SHAP, a counterfactual | Test patient 3: 0.626 + 0.262 = 0.888 from the SHAP values; a counterfactual that is valid and sparse but not plausible |
| [Day 3](https://utkukose.github.io/xai-veltech-NB-lecture/days/day-03/lecture.html#the-diagnosis-case-stage-3-the-network-caught-looking-at-the-marker) | A convolutional network on the lesion images, explained from the inside and graded against the planted marker. | Saliency, gradient times input, SmoothGrad, Integrated Gradients, Grad-CAM, a sanity test | The pixel-level maps peak on the marker in 40 of 40 images and pass the sanity test; 31 of 40 Grad-CAM maps are empty |
| [Day 4](https://utkukose.github.io/xai-veltech-NB-lecture/days/day-04/lecture.html#the-diagnosis-case-stage-4-how-far-the-results-can-be-trusted) | How far the probabilities, the explanations and the decisions of the models can be trusted. | Calibration, a domain classifier for shift, a manipulated explanation, fairness measures and a proxy, a benchmark against a random ranking | Recalibration brings the calibration error of the deep credit model from 0.203 to 0.026; the postcode carries 0.39 of a gap of 0.81; SHAP reaches a faithfulness of 0.188 against −0.101 for a random ranking |
| [Day 5](https://utkukose.github.io/xai-veltech-NB-lecture/days/day-05/lecture.html#the-diagnosis-case-stage-5-artefacts-for-the-clinic) | The results leave the notebook as artefacts for the people who use them. | An explanation record with a digest, a dashboard, a model card generated from the model, the risk tiers of the Artificial Intelligence Act of the European Union | The record of patient 518 with a fidelity of 0.7246; a card with an accuracy of 0.958 and an AUC of 0.994; an advisory model for health care is high risk |

The final project asks each student to audit a model of their own choice along the same five stages: the question of a stakeholder, a test of whether a readable model would be enough, at least three explanation methods with a reliability check, and a generated model card with a recommendation.

## Daily schedule

| Day | Topic | Overview | Lecture | Lab | Notebook | PDF |
|---|---|---|---|---|---|---|
| 1 | Foundations of Interpretability | [overview](days/day-01/README.md) | [lecture](https://utkukose.github.io/xai-veltech-NB-lecture/days/day-01/lecture.html) | [lab](https://utkukose.github.io/xai-veltech-NB-lecture/days/day-01/lab.html) | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/utkukose/xai-veltech-NB-lecture/blob/main/days/day-01/NB01_foundations_of_interpretability.ipynb) | [PDF](days/day-01/Day01_Lecture_Notes.pdf) |
| 2 | Model-Agnostic Explanation Methods | [overview](days/day-02/README.md) | [lecture](https://utkukose.github.io/xai-veltech-NB-lecture/days/day-02/lecture.html) | [lab](https://utkukose.github.io/xai-veltech-NB-lecture/days/day-02/lab.html) | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/utkukose/xai-veltech-NB-lecture/blob/main/days/day-02/NB02_model_agnostic_methods.ipynb) | [PDF](days/day-02/Day02_Lecture_Notes.pdf) |
| 3 | Explaining Deep Neural Networks | [overview](days/day-03/README.md) | [lecture](https://utkukose.github.io/xai-veltech-NB-lecture/days/day-03/lecture.html) | [lab](https://utkukose.github.io/xai-veltech-NB-lecture/days/day-03/lab.html) | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/utkukose/xai-veltech-NB-lecture/blob/main/days/day-03/NB03_explaining_deep_networks.ipynb) | [PDF](days/day-03/Day03_Lecture_Notes.pdf) |
| 4 | Reliability of Explanations | [overview](days/day-04/README.md) | [lecture](https://utkukose.github.io/xai-veltech-NB-lecture/days/day-04/lecture.html) | [lab](https://utkukose.github.io/xai-veltech-NB-lecture/days/day-04/lab.html) | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/utkukose/xai-veltech-NB-lecture/blob/main/days/day-04/NB04_reliability_of_explanations.ipynb) | [PDF](days/day-04/Day04_Lecture_Notes.pdf) |
| 5 | Practice, Tooling and Governance | [overview](days/day-05/README.md) | [lecture](https://utkukose.github.io/xai-veltech-NB-lecture/days/day-05/lecture.html) | [lab](https://utkukose.github.io/xai-veltech-NB-lecture/days/day-05/lab.html) | [![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/utkukose/xai-veltech-NB-lecture/blob/main/days/day-05/NB05_practice_tooling_governance.ipynb) | [PDF](days/day-05/Day05_Lecture_Notes.pdf) |

## Python for non-programmers

Python is taught step by step alongside the content of the course, always through the tool that the problem of the day needs [6]. Every day has a Python step in its notebook, right after the setup section, that explains one group of fundamentals with the example of the day in runnable cells and closes with a quick check and three exercises. The five steps lead from values, variables, lists and decisions on Day 1, through NumPy arrays and functions, a neural network as arrays and the chain rule, pandas data frames and plots, to classes and reproducible records on Day 5 [7, 8, 9].

The full sequence is described in [`PYTHON_PATH.md`](PYTHON_PATH.md).

## Assessment and submission

Assessment rests on a final project, an explanation audit of a predictive model, which consists of a coding application and a short technical report. Each day also offers an optional task, an optional research and report assignment and a self-assessment in the lab. During an active delivery of the course, components and weights are announced by the instructor at the start of the course in line with the regulations of Vel Tech University, and the daily task can be sent together with the exported learning log to utkukose@sdu.edu.tr or utkukose@gmail.com. The self-assessments are formative and do not count towards the grade.

| Component | Timing | Format | Page |
|---|---|---|---|
| Daily task and learning log | End of each day | Short coding task and exported log | each day folder |
| Final project: An explanation audit of a predictive model | One week after Day 5 | Coding application and technical report | [open](exams/final/README.md) |

The final project report is written in the Word template [exams/REPORT_TEMPLATE.docx](exams/REPORT_TEMPLATE.docx), and the reports of the research assignments can follow the same structure. The syllabus in [SYLLABUS.md](SYLLABUS.md) states the policies, including the rules for using generative AI tools.

## Running the materials

The notebooks run in Google Colab through the badge of each day, with no installation. For local work on Windows or Ubuntu, create a virtual environment with `python -m venv .venv`, activate it, run `pip install -r requirements.txt` and start `jupyter lab`. The lecture pages and labs open in any modern browser, also from the course site, and keep progress only in the browser.

## Reference integrity

All references were checked before release. Entries with a link in `references/REFERENCES.md` were confirmed against that DOI or publisher page during preparation, and the remaining entries are fully citable from the details given. No locator was reconstructed from memory. As an independent check, `tools/verify_references.py` compares every entry with Crossref and OpenAlex, and the GitHub Actions workflow runs it monthly and on every change of the references.

## Citing this course

Citation metadata is provided in `CITATION.cff`. A suggested citation is:

> Kose, U. (2026). *Explainable Artificial Intelligence: Open course materials* [Course materials]. GitHub. https://github.com/utkukose/xai-veltech-NB-lecture

## License

The course text, figures, lecture notes and interactive labs are licensed under the Creative Commons Attribution 4.0 International License (CC BY 4.0), as stated in `LICENSE-CONTENT`. The code in the notebooks, labs and tools is licensed under the MIT License, as stated in `LICENSE`.

## References cited on this page

[1] Arrieta, A. B., Díaz-Rodríguez, N., Del Ser, J., Bennetot, A., Tabik, S., Barbado, A., García, S., Gil-López, S., Molina, D., Benjamins, R., Chatila, R., & Herrera, F. (2020). Explainable Artificial Intelligence (XAI): Concepts, taxonomies, opportunities and challenges toward responsible AI. Information Fusion, 58, 82-115.

[2] Ortigossa, E. S., Gonçalves, T., & Nonato, L. G. (2024). Explainable Artificial Intelligence (XAI) - from theory to methods and applications. IEEE Access, 12, 80799-80846.

[3] Rudin, C. (2019). Stop explaining black box machine learning models for high stakes decisions and use interpretable models instead. Nature Machine Intelligence, 1(5), 206-215.

[4] Mitchell, M., Wu, S., Zaldivar, A., Barnes, P., Vasserman, L., Hutchinson, B., Spitzer, E., Raji, I. D., & Gebru, T. (2019). Model cards for model reporting. In Proceedings of the Conference on Fairness, Accountability, and Transparency (FAT* '19) (pp. 220-229). ACM. <https://doi.org/10.1145/3287560.3287596>

[5] Kose, U., Şengöz, N., Chen, X., & Marmolejo Saucedo, J. A. (Eds.). (2024). Explainable Artificial Intelligence (XAI) in Healthcare. CRC Press.

[6] Van Rossum, G., & Drake, F. L. (2009). Python 3 Reference Manual. CreateSpace.

[7] Harris, C. R., Millman, K. J., van der Walt, S. J., Gommers, R., Virtanen, P., Cournapeau, D., Wieser, E., Taylor, J., Berg, S., Smith, N. J., et al. (2020). Array programming with NumPy. Nature, 585(7825), 357-362. <https://doi.org/10.1038/s41586-020-2649-2>

[8] McKinney, W. (2010). Data structures for statistical computing in Python. In Proceedings of the 9th Python in Science Conference (pp. 56-61). <https://doi.org/10.25080/Majora-92bf1922-00a>

[9] Pedregosa, F., Varoquaux, G., Gramfort, A., Michel, V., Thirion, B., Grisel, O., Blondel, M., Prettenhofer, P., Weiss, R., Dubourg, V., Vanderplas, J., Passos, A., Cournapeau, D., Brucher, M., Perrot, M., & Duchesnay, E. (2011). Scikit-learn: Machine learning in Python. Journal of Machine Learning Research, 12, 2825-2830.

---

<div align="center">

**Prof. Dr. Utku Kose**

Full Professor, Department of Computer Engineering, Süleyman Demirel University, Isparta, Türkiye  
Founding Director, AI Application and Research Center (YAZEM), Süleyman Demirel University  
Head of the Computer Science Division, Department of Computer Engineering, Süleyman Demirel University  
Additional affiliations: University of North Dakota (USA), Universidad Panamericana (Mexico City, Mexico), Vel Tech University (Chennai, India)  
IEEE Senior Member, ACM Professional Member

[ORCID 0000-0002-9652-6415](https://orcid.org/0000-0002-9652-6415) | [utkukose.com](https://www.utkukose.com) | [github.com/utkukose](https://github.com/utkukose)

[utkukose@sdu.edu.tr](mailto:utkukose@sdu.edu.tr) | [utku.kose@und.edu](mailto:utku.kose@und.edu) | [ukose@up.edu.mx](mailto:ukose@up.edu.mx) | [utkukose@gmail.com](mailto:utkukose@gmail.com)

</div>

## Acknowledgments

The course draws on the work of the many researchers cited in the daily references and on the Breast Cancer Wisconsin (Diagnostic) dataset of the UCI Machine Learning Repository. It was prepared for the value added course programme of the Office of International Relations of Vel Tech Rangarajan Dr. Sagunthala R&D Institute of Science and Technology, Chennai.
