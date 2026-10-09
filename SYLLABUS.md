# Syllabus: Explainable Artificial Intelligence

## Course information

| Item | Detail |
|---|---|
| Course | Explainable Artificial Intelligence |
| Code | VTR UGE 21, value added course |
| Institution | Vel Tech Rangarajan Dr. Sagunthala R&D Institute of Science and Technology, Chennai, India |
| Credits | L-T-P-C 1-0-0-1 |
| Format | Five days, one module per day, synchronous sessions with materials for asynchronous study |
| Instructor | Prof. Dr. Utku Kose |
| Language | English |

## Course description

Machine learning models now support decisions in medicine, finance, engineering and public services, and many of them are too complex to be read directly. Explainable artificial intelligence (XAI) develops methods that describe what such models do and why, and it develops the means to check whether those descriptions are right . The course is built around one argument: An explanation is a second model of the first model, and like any model it can be wrong. Day 1 separates interpretable models from explained ones and measures when an interpretable model is enough . Day 2 builds the model-agnostic methods from first principles, Day 3 explains deep networks, Day 4 attacks every explanation built so far, and Day 5 turns the results into records, dashboards and model cards that can be defended . Three of the four datasets of the course are synthetic with a known ground truth, so that every explanation can be graded rather than admired.

## Prerequisites

No programming experience is required. Basic secondary-school mathematics is assumed: Functions and graphs, simple probability and the idea of a derivative. Students without programming experience should complete the start-here notebook before Day 1.

## Learning outcomes

On completion, students are expected to distinguish interpretable models from post-hoc explanations and choose between them on measured evidence, to implement permutation importance, partial dependence, accumulated local effects, LIME, Shapley values, counterfactuals and anchors from first principles, to explain image and text models with gradients, Grad-CAM, relevance propagation, attention and concept probes, to test explanations for calibration, shift, adversarial fragility and fairness with a benchmark against a random baseline, and to document a model with reproducible explanation records and a model card. In Python, students are expected to write and debug short programs with variables, lists, dictionaries, loops and functions, to use NumPy, pandas, Matplotlib and scikit-learn for data and models, and to read a small neural network written in NumPy, with its forward and backward pass.

## Daily plan

| Day | Module | Python step |
|---|---|---|
| 1 | Foundations of Interpretability | Values, variables, lists and decisions |
| 2 | Model-Agnostic Explanation Methods | NumPy arrays, randomness and functions |
| 3 | Explaining Deep Neural Networks | A neural network as arrays and the chain rule |
| 4 | Reliability of Explanations | Data frames and plots |
| 5 | Practice, Tooling and Governance | Classes, records and files |

## Learning activities and workload

Each day combines about three hours of synchronous session with about three to five hours of individual work on the notebook, the lab, the challenges and the daily task. In asynchronous study, the study path of each day gives a suggested time for every activity, about six to eight hours per day in total. The final project needs about twenty hours.

## Assessment

Assessment rests on a final project, an explanation audit of a predictive model, which consists of a coding application and a short technical report. Each day also offers an optional task, an optional research and report assignment and a self-assessment in the lab. During an active delivery of the course, components and weights are announced by the instructor at the start of the course in line with the regulations of Vel Tech University, and the daily task can be sent together with the exported learning log to utkukose@sdu.edu.tr or utkukose@gmail.com. The self-assessments are formative and do not count towards the grade.

## Policy on generative AI tools

Generative AI tools may be used for explanation, debugging and drafting, under three conditions. Every use is declared in the statement on tools of the report, every output that enters the submitted work is checked by the student, and every reference is verified against its source. A fabricated reference, a fabricated result or undeclared generated text is treated as a breach of academic integrity.

## Academic integrity

Work submitted for assessment must be the student's own. Collaboration in class is encouraged, while code and reports for the final project are written individually or by the declared pair. Sources are cited for every idea, figure, dataset and piece of code taken from others.

## Accessibility

All pages run in a browser without installation and work on phones. Labs can be used with the keyboard, and animations respect the reduced-motion setting of the operating system. Lecture notes are also provided as PDF.

## Main textbooks and open resources

The course is self-contained, and every source is cited where it is used. Useful open companions are the documentation of scikit-learn, SHAP, LIME and Captum, and the open book Fairness and Machine Learning by Barocas, Hardt and Narayanan at <https://fairmlbook.org/>.
