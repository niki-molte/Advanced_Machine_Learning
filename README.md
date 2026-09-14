# Advanced Machine Learning

![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange?logo=jupyter)
![Course](https://img.shields.io/badge/Course-Advanced%20Machine%20Learning-purple)
![Academic Year](https://img.shields.io/badge/Academic%20Year-2025%2F2026-green)

Repository containing the assignments developed for the **Advanced Machine Learning** course at the **University of Milano-Bicocca (UNIMIB)** during the **2025/2026 academic year**.

The repository collects the practical work carried out throughout the course, covering different aspects of modern machine learning, from data preprocessing and exploratory analysis to model training, evaluation and comparison.

---

## 📚 Table of Contents

* [About](#about)
* [Repository Structure](#repository-structure)
* [Assignments](#assignments)

  * [Assignment 1](#assignment-1)
  * [Assignment 2](#assignment-2)
  * [Assignment 3](#assignment-3)
  * [Assignment 4](#assignment-4)
* [Machine Learning Workflow](#machine-learning-workflow)
* [Technologies](#technologies)
* [Installation](#installation)
* [Running the Notebooks](#running-the-notebooks)
* [Results](#results)
* [Academic Context](#academic-context)
* [Author](#author)

---

## About

This repository contains the practical assignments for the **Advanced Machine Learning** course at **Università degli Studi di Milano-Bicocca**.

The main objective of the coursework is to apply theoretical machine learning concepts to practical problems, developing complete and reproducible machine learning workflows.

The assignments cover different stages of the machine learning process, including:

* Data exploration and preprocessing
* Feature engineering
* Statistical analysis
* Model selection
* Supervised learning
* Unsupervised learning
* Model optimization
* Hyperparameter tuning
* Model evaluation
* Performance comparison
* Data visualization

The repository is structured so that each assignment can be explored independently.

---

# Repository Structure

```text
Advanced_Machine_Learning/
│
├── assignment_1/
│   └── ...
│
├── assignment_2/
│   └── ...
│
├── assignment_3/
│   └── ...
│
├── assignment_4/
│   └── ...
│
└── README.md
```

Each assignment contains the material related to the corresponding coursework, including notebooks, source code, datasets and/or supporting files where applicable.

---

# Assignments

## Assignment 1

📁 [`assignment_1/`](./assignment_1/)

### Overview

The first assignment introduces the first set of practical problems addressed during the course.

The work focuses on applying machine learning methodologies to a dataset, following a complete workflow from data preparation to model evaluation.

### Main steps

* Dataset exploration
* Exploratory Data Analysis
* Data preprocessing
* Feature preparation
* Model development
* Model training
* Model evaluation
* Interpretation of results

### Methods

> **To be completed with the specific models/algorithms implemented in the notebook.**

Examples:

* Regression / Classification
* Linear models
* Regularization
* Cross-validation
* Hyperparameter optimization

### Results

> **Add the main quantitative results here.**

For example:

| Model      | Metric               | Score |
| ---------- | -------------------- | ----: |
| Baseline   | Accuracy / RMSE / R² |     — |
| Model 1    | Accuracy / RMSE / R² |     — |
| Model 2    | Accuracy / RMSE / R² |     — |
| Best Model | Accuracy / RMSE / R² |     — |

---

## Assignment 2

📁 [`assignment_2/`](./assignment_2/)

### Overview

The second assignment builds upon the concepts introduced previously and focuses on more advanced machine learning techniques.

The analysis includes model development, comparison and evaluation using appropriate validation strategies.

### Main steps

* Data preprocessing
* Exploratory analysis
* Feature engineering
* Model training
* Validation
* Hyperparameter tuning
* Model comparison
* Error analysis

### Methods

> **To be completed with the specific algorithms used in Assignment 2.**

Potential topics include:

* Ensemble learning
* Tree-based models
* Gradient boosting
* Support Vector Machines
* Neural networks
* Dimensionality reduction

### Results

The performance of the considered approaches is compared using appropriate evaluation metrics.

| Model      | Metric | Score |
| ---------- | ------ | ----: |
| Baseline   | —      |     — |
| Model 1    | —      |     — |
| Model 2    | —      |     — |
| Best Model | —      |     — |

---

## Assignment 3

📁 [`assignment_3/`](./assignment_3/)

### Overview

The third assignment explores additional advanced machine learning concepts, with particular attention to model performance, generalization and the analysis of the obtained results.

### Main steps

* Data analysis
* Preprocessing
* Feature extraction / engineering
* Model selection
* Training
* Validation
* Performance evaluation
* Comparison of alternative approaches

### Methods

> **To be completed based on the actual notebook.**

Possible techniques include:

* Unsupervised learning
* Dimensionality reduction
* Clustering
* Anomaly detection
* Advanced classification methods

### Results

The main results obtained during the experiments are summarized below.

| Approach      | Metric | Result |
| ------------- | ------ | -----: |
| Baseline      | —      |      — |
| Method 1      | —      |      — |
| Method 2      | —      |      — |
| Best approach | —      |      — |

---

## Assignment 4

📁 [`assignment_4/`](./assignment_4/)

### Overview

The fourth assignment concludes the practical part of the course by applying advanced machine learning methodologies to a final problem.

The analysis emphasizes model comparison, performance evaluation and interpretation of the results.

### Main steps

* Dataset preparation
* Exploratory Data Analysis
* Feature engineering
* Model development
* Hyperparameter optimization
* Model evaluation
* Comparison of different approaches
* Final analysis

### Methods

> **To be completed with the actual models implemented in Assignment 4.**

### Results

| Model      | Metric | Score |
| ---------- | ------ | ----: |
| Baseline   | —      |     — |
| Model 1    | —      |     — |
| Model 2    | —      |     — |
| Best Model | —      |     — |

---

# Machine Learning Workflow

Across the assignments, the projects follow a typical machine learning pipeline:

```text
             ┌──────────────────┐
             │      Dataset     │
             └────────┬─────────┘
                      │
                      ▼
             ┌──────────────────┐
             │ Data Exploration │
             │      & EDA       │
             └────────┬─────────┘
                      │
                      ▼
             ┌──────────────────┐
             │  Preprocessing   │
             │ & Feature Eng.   │
             └────────┬─────────┘
                      │
                      ▼
             ┌──────────────────┐
             │ Train / Test     │
             │      Split       │
             └────────┬─────────┘
                      │
                      ▼
             ┌──────────────────┐
             │ Model Training   │
             └────────┬─────────┘
                      │
                      ▼
             ┌──────────────────┐
             │ Hyperparameter   │
             │     Tuning       │
             └────────┬─────────┘
                      │
                      ▼
             ┌──────────────────┐
             │    Evaluation    │
             └────────┬─────────┘
                      │
                      ▼
             ┌──────────────────┐
             │ Model Comparison │
             └──────────────────┘
```

This structure allows the experiments to be evaluated not only in terms of final predictive performance, but also in terms of preprocessing choices, model assumptions and generalization capabilities.

---

# Technologies

The projects are primarily developed in **Python** using the scientific Python and machine learning ecosystem.

### Core technologies

* [Python](https://www.python.org/)
* [Jupyter Notebook](https://jupyter.org/)
* [NumPy](https://numpy.org/)
* [Pandas](https://pandas.pydata.org/)
* [Scikit-learn](https://scikit-learn.org/)
* [Matplotlib](https://matplotlib.org/)
* [Seaborn](https://seaborn.pydata.org/)

Additional libraries may be used in individual assignments depending on the specific problem and methodology.

---

# Installation

Clone the repository:

```bash
git clone https://github.com/niki-molte/Advanced_Machine_Learning.git
cd Advanced_Machine_Learning
```

Create a virtual environment:

### Linux / macOS

```bash
python3 -m venv .venv
source .venv/bin/activate
```

### Windows

```powershell
python -m venv .venv
.venv\Scripts\activate
```

Install the required dependencies:

```bash
pip install -r requirements.txt
```

If a global `requirements.txt` is not available, install the dependencies specified by the individual assignments.

---

# Running the Notebooks

The assignments are primarily designed to be executed using Jupyter Notebook.

Start Jupyter with:

```bash
jupyter notebook
```

or:

```bash
jupyter lab
```

Then open the desired assignment:

```text
assignment_1/
assignment_2/
assignment_3/
assignment_4/
```

Each notebook should preferably be executed from top to bottom to reproduce the analysis and results.

---

# Results

The assignments investigate different machine learning approaches and compare their performance using appropriate evaluation metrics.

Depending on the specific task, relevant metrics may include:

### Classification

* Accuracy
* Precision
* Recall
* F1-score
* ROC-AUC
* Confusion Matrix

### Regression

* Mean Absolute Error (MAE)
* Mean Squared Error (MSE)
* Root Mean Squared Error (RMSE)
* R² score

### Unsupervised Learning

* Silhouette Score
* Inertia
* Reconstruction error
* Cluster quality measures

The exact metrics used are reported within the corresponding assignment notebooks.

---

# Reproducibility

The experiments are intended to be reproducible.

Where applicable, random seeds are fixed to ensure consistent results across different runs.

For best reproducibility:

1. Use the same Python version.
2. Install the required dependencies.
3. Run the notebooks from the beginning.
4. Keep the original dataset and directory structure unchanged.
5. Use the same random seeds and train/test splits.

---

# Academic Context

**Course:** Advanced Machine Learning
**University:** Università degli Studi di Milano-Bicocca (UNIMIB)
**Academic Year:** 2025/2026

The repository is intended primarily for academic and educational purposes.

---

# Author

**Nicolò Molteni**

Advanced Machine Learning
Università degli Studi di Milano-Bicocca
Academic Year 2025/2026

---

## License

This repository contains coursework developed as part of a university course.

Unless otherwise specified, the material is intended for **educational purposes**.
