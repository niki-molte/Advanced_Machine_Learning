# Advanced Machine Learning

![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange?logo=jupyter)
![Course](https://img.shields.io/badge/Course-Advanced%20Machine%20Learning-purple)
![Academic Year](https://img.shields.io/badge/Academic%20Year-2025%2F2026-green)

Repository containing the assignments developed for the **Advanced Machine Learning** course at the **University of Milano-Bicocca (UNIMIB)** during the **2025/2026 academic year**.

The repository collects the practical work carried out throughout the course, covering different aspects of modern machine learning, from data preprocessing and exploratory analysis to model training, evaluation, and comparison.

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
* [Reproducibility](#reproducibility)
* [Academic Context](#academic-context)
* [Author](#author)
* [License](#license)

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

## Repository Structure

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

Each assignment contains the material related to the corresponding coursework, including notebooks, source code, datasets, and/or supporting files where applicable.

---

# Assignments

## Assignment 1

📁 [`assignment_1/`](./assignment_1/)

### Overview

The first assignment focuses on a multinomial classification problem using the **Dry Bean Dataset** from the **UCI Machine Learning Repository**.

The dataset contains 16 numeric features extracted from images of dry beans captured with an RGB camera, categorized into 7 imbalanced classes.

### Main Steps

* Exploratory Data Analysis (EDA) and class distribution check
* Data preprocessing (label encoding and one-hot encoding)
* Dataset splitting (train/validation/test)
* Feature standardization to prevent data leakage
* Feed-Forward Neural Network development
* Hyperparameter optimization (batch size, epochs, learning rate)
* Model evaluation

### Methods

* Feed-Forward Neural Networks

  * 1 input layer
  * 2 hidden layers with ReLU activation
  * 1 output layer with Softmax activation
* Categorical Focal Cross-Entropy Loss to handle class imbalance
* Adam Optimizer

### Results

The models were evaluated mainly using accuracy and the **Macro-Average ROC-AUC**, due to the presence of class imbalance.

The optimized model achieved excellent classification capabilities.

| **Model**       | **Metric**        | **Score** |
| --------------- | ----------------- | --------: |
| First Model     | Macro-Average AUC |      0.99 |
| Optimized Model | Macro-Average AUC |      0.99 |

---

## Assignment 2

📁 [`assignment_2/`](./assignment_2/)

### Overview

The second assignment focuses on **neural network optimization techniques** across three different problems.

The main goal is to analyze baseline models suffering from unstable training, poor generalization, overfitting, or underfitting, and improve their architectures and training routines.

### Main Steps

* Analysis of learning curves (train/validation loss and accuracy)
* Analysis of weight distributions
* Hyperparameter tuning, particularly learning rate adjustment
* Implementation of regularization techniques
* Early Stopping implementation

### Methods

* L1 regularization
* L2 regularization
* Combined L1/L2 regularization
* Dropout layers
* Early Stopping
* Deep Neural Network optimization

### Results

* **Problem 1 & 3:** Severe overfitting and unstable training were successfully mitigated by decreasing the learning rate, applying L2 regularization, adding Dropout (0.25), and using Early Stopping. The final models achieved smooth loss curves and good generalization.

* **Problem 2:** The original dense network was highly prone to overfitting. L1/L2 and L2 regularization were combined with Dropout (0.2). Although overfitting was solved, the resulting model suffered from underfitting, with accuracy around 50%. This suggests that, for this specific task, an alternative architecture such as a **Convolutional Neural Network (CNN)** may be more appropriate.

---

## Assignment 3

📁 [`assignment_3/`](./assignment_3/)

### Overview

The third assignment focuses on improving the **efficiency of Deep Learning models**.

The objective is to take a baseline Convolutional Neural Network trained on the **MNIST digit dataset**, which contains 34,826 parameters and achieves approximately 98.75% accuracy, and drastically reduce its complexity to fewer than 7,000 parameters without degrading predictive performance.

### Main Steps

* Baseline model evaluation
* Iterative parameter reduction strategies
* Modification of pooling layers
* Kernel size tuning
* Dense layer removal

### Methods

* Convolutional Neural Networks (CNNs)
* Average Pooling, used to replace Max Pooling to preserve contextual information
* Network pruning and simplification
* Dropout

### Results

The goal was successfully achieved.

The best model (**Model 3**) used a consistent 3×3 kernel size, removed the final pooling layer to preserve spatial structure, and achieved higher accuracy than the baseline while reducing the number of parameters to less than one tenth.

| **Model**    | **Parameters** | **Accuracy** |
| ------------ | -------------: | -----------: |
| Baseline CNN |         34,826 |      ~98.75% |
| Model 1      |          4,546 |      ~97.30% |
| Model 2      |          4,138 |      ~98.92% |
| **Model 3**  |      **3,282** |  **~99.02%** |

---

## Assignment 4

📁 [`assignment_4/`](./assignment_4/)

### Overview

The fourth assignment focuses on **sequential data and Natural Language Processing (NLP)**.

The goal is to perform **next-character prediction** based on a fixed-size input window.

The dataset used for this task is the text of *Alice's Adventures in Wonderland* by **Lewis Carroll**.

### Main Steps

* Raw text preprocessing

  * Removal of Gutenberg introductions
  * Removal of table of contents
  * Removal of licenses
* Sequential dataset creation

  * Maximum sentence length of 40
  * Step size of 2
* Temporal train/validation/test split without shuffling
* Baseline CNN evaluation
* Development of a proposed hybrid architecture

### Methods

* Natural Language Processing (NLP)
* Text generation
* 1D Convolutional Neural Networks (Conv1D) for feature extraction
* Long Short-Term Memory Networks (LSTM) for recurrent pattern capturing
* Adam Optimizer
* Early Stopping

### Results

The proposed hybrid architecture (**Conv1D + LSTM**) significantly outperformed the purely convolutional baseline, demonstrating greater effectiveness in predicting both frequent and infrequent characters.

| **Model**                    | **Metric**            |  **Score** |
| ---------------------------- | --------------------- | ---------: |
| Baseline (CNN)               | Accuracy              |     16.76% |
| Baseline (CNN)               | Macro-Average AUC     |      0.582 |
| **Proposed (Conv1D + LSTM)** | **Accuracy**          | **51.76%** |
| **Proposed (Conv1D + LSTM)** | **Macro-Average AUC** |  **0.893** |

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

This structure allows the experiments to be evaluated not only in terms of final predictive performance, but also in terms of preprocessing choices, model assumptions, and generalization capabilities.

---

# Technologies

The projects are primarily developed in **Python**, using the scientific Python and machine learning ecosystem.

### Core Technologies

* [Python](https://www.python.org/)
* [Jupyter Notebook](https://jupyter.org/)
* [NumPy](https://numpy.org/)
* [Pandas](https://pandas.pydata.org/)
* [Scikit-learn](https://scikit-learn.org/)
* [TensorFlow / Keras](https://www.tensorflow.org/)
* [Matplotlib](https://matplotlib.org/)
* [Seaborn](https://seaborn.pydata.org/)

Additional libraries may be used in individual assignments depending on the specific problem and methodology.

---

# Installation

## Clone the Repository

```bash
git clone https://github.com/niki-molte/Advanced_Machine_Learning.git
cd Advanced_Machine_Learning
```

## Create a Virtual Environment

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

## Install Dependencies

```bash
pip install -r requirements.txt
```

If a global `requirements.txt` is not available, install the dependencies specified by the individual assignments.

---

# Running the Notebooks

The assignments are primarily designed to be executed using **Jupyter Notebook**.

Start Jupyter Notebook with:

```bash
jupyter notebook
```

or JupyterLab with:

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
* ROC-AUC (Macro-Average)
* Confusion Matrix

### Regression

* Mean Absolute Error (MAE)
* Mean Squared Error (MSE)
* Root Mean Squared Error (RMSE)
* R² score

### Unsupervised Learning

* Silhouette Score
* Inertia
* Reconstruction Error
* Cluster Quality Measures

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

# License

This repository contains coursework developed as part of a university course.

Unless otherwise specified, the material is intended for **educational purposes**.
