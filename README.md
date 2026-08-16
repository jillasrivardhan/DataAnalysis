# 📊 Data Analysis & Machine Learning

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.x-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python">
  <img src="https://img.shields.io/badge/Pandas-Data%20Analysis-150458?style=for-the-badge&logo=pandas&logoColor=white" alt="Pandas">
  <img src="https://img.shields.io/badge/NumPy-Numerical%20Computing-013243?style=for-the-badge&logo=numpy&logoColor=white" alt="NumPy">
  <img src="https://img.shields.io/badge/Matplotlib-Visualization-11557C?style=for-the-badge&logo=matplotlib&logoColor=white" alt="Matplotlib">
  <img src="https://img.shields.io/badge/Seaborn-Visualization-4C72B0?style=for-the-badge" alt="Seaborn">
  <img src="https://img.shields.io/badge/Scikit--learn-Machine%20Learning-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white" alt="Scikit-learn">
  <img src="https://img.shields.io/badge/Jupyter-Notebook-F37626?style=for-the-badge&logo=jupyter&logoColor=white" alt="Jupyter">
</p>

<p align="center">
  <strong>A practical Data Analysis and Machine Learning repository covering data preprocessing, visualization, classification, regression, model evaluation, and real-world datasets.</strong>
</p>

---

## 📖 About

This repository contains hands-on implementations and experiments developed while learning **Data Analysis and Machine Learning with Python**.

The project progresses from fundamental data preprocessing concepts to machine learning algorithms and real-world data analysis projects.

It includes:

* 📊 Exploratory Data Analysis (EDA)
* 🧹 Data Cleaning & Preprocessing
* 🔢 Numerical Data Processing
* 🏷️ Label Encoding
* 🔢 One-Hot Encoding
* ⚙️ Machine Learning Pipelines
* 📈 Regression Algorithms
* 🤖 Classification Algorithms
* ❤️ Heart Disease Analysis
* 🏏 IPL Data Analysis
* 📊 Data Visualization
* 📐 Feature Selection
* 🔄 Cross-Validation
* 📏 Model Evaluation
* 🏆 Multiple Model Comparison

The notebooks are designed as practical learning exercises using real datasets.

---

# 🚀 Repository Overview

```text
                         DATA ANALYSIS
                               │
                               ▼
                     Exploratory Data Analysis
                               │
                               ▼
                     Data Cleaning & Processing
                               │
                 ┌─────────────┴─────────────┐
                 ▼                           ▼
        Numerical Features          Categorical Features
                 │                           │
                 │                  ┌────────┴────────┐
                 │                  ▼                 ▼
                 │            Label Encoding    One-Hot Encoding
                 │                  │                 │
                 └──────────────────┴─────────────────┘
                                    │
                                    ▼
                            ML Preprocessing
                                    │
                                    ▼
                             Model Training
                                    │
              ┌─────────────────────┼─────────────────────┐
              ▼                     ▼                     ▼
         Classification         Regression         Real-World Analysis
              │                     │                     │
        ┌─────┼─────┐               │              ┌──────┴──────┐
        ▼     ▼     ▼               ▼              ▼             ▼
       KNN   SVM  Logistic       Linear         Heart          IPL
                  Regression     Regression     Disease       Analysis
```

---

# ✨ Key Features

## 📊 Exploratory Data Analysis

The repository contains practical examples of:

* Dataset inspection
* DataFrame exploration
* Understanding data types
* Statistical analysis
* Missing-value detection
* Feature analysis
* Data visualization
* Correlation analysis

Common libraries used:

```python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
```

---

## 🧹 Data Preprocessing

Data preprocessing is an essential part of the machine learning workflow.

This repository demonstrates:

* Missing-value handling
* Data cleaning
* Feature preparation
* Numerical feature processing
* Categorical feature processing
* Feature selection
* Data transformation

Typical workflow:

```text
Raw Dataset
     ↓
Data Inspection
     ↓
Data Cleaning
     ↓
Missing Value Handling
     ↓
Feature Transformation
     ↓
Feature Selection
     ↓
Model Training
```

---

# 🏷️ Data Encoding

The `Data-Preprocessing` folder contains examples of converting categorical data into numerical representations.

### Label Encoding

```text
Categorical Data
      ↓
Label Encoder
      ↓
Numerical Labels
```

Example:

```text
Male    → 1
Female  → 0
```

Implemented in:

```text
Data-Preprocessing/
└── Lable_Encoder.ipynb
```

> **Note:** Label encoding should be used carefully for categorical features because assigning numbers can introduce an artificial ordering. For nominal feature columns, One-Hot Encoding is often more appropriate.

---

## 🔢 One-Hot Encoding

One-Hot Encoding converts categories into separate binary columns.

Example:

```text
Class
-----
Business
Economy
```

becomes:

```text
Class_Business    Class_Economy
1                 0
0                 1
```

Implemented in:

```text
Data-Preprocessing/
└── ONE HOT ENCODING.ipynb
```

---

# ⚙️ Machine Learning Pipeline

The project also demonstrates the use of Scikit-learn pipelines.

A pipeline allows preprocessing and model training to be combined into a single workflow.

```text
Input Data
    ↓
Preprocessing
    ↓
Encoding / Transformation
    ↓
Model
    ↓
Prediction
```

Implemented in:

```text
Data-Preprocessing/
└── pipeline.ipynb
```

---

# 🤖 Machine Learning Algorithms

## 📌 Classification

The repository currently contains implementations of:

### K-Nearest Neighbors

Implemented in:

```text
Classification-Algorithms/
└── KNN.ipynb
```

KNN predicts a class based on the nearest data points.

```text
Training Data
      ↓
Calculate Distance
      ↓
Find K Neighbors
      ↓
Majority Vote
      ↓
Prediction
```

---

### Logistic Regression

Implemented in:

```text
Classification-Algorithms/
└── Logistic_Regression.ipynb
```

Logistic Regression is used for classification problems where the target represents a class or category.

---

### Support Vector Machine

Implemented in:

```text
Classification-Algorithms/
└── SVM.ipynb
```

SVM attempts to identify an optimal decision boundary between different classes.

---

# 📈 Regression

## Linear Regression

Implemented in:

```text
Regression-Algorithms/
└── Linear_Regression.ipynb
```

Linear Regression is used to model relationships between input features and continuous numerical targets.

Basic workflow:

```text
Input Features
      ↓
Linear Regression
      ↓
Predicted Continuous Value
```

---

# ❤️ Heart Disease Analysis

The `Heart-Disease-Analysis` folder contains a more complete machine learning workflow based on a heart disease dataset.

```text
Heart-Disease-Analysis/
│
├── HeartDisease.ipynb
├── HeartDisease_2.ipynb
├── HeartDisease_3.ipynb
└── heart.csv
```

## Analysis Workflow

The project progresses through:

```text
Exploratory Data Analysis
          ↓
Data Cleaning
          ↓
Data Preprocessing
          ↓
Feature Selection
          ↓
Train/Test Split
          ↓
Model Training
          ↓
Model Evaluation
          ↓
Multiple Algorithm Comparison
          ↓
Feature Reduction
          ↓
Accuracy Improvement
```

### Algorithms Explored

The Heart Disease notebooks experiment with models including:

* Logistic Regression
* Random Forest Classifier
* Support Vector Classifier
* K-Nearest Neighbors

### Evaluation Techniques

The notebooks use:

* Accuracy Score
* Confusion Matrix
* Classification Report
* Cross-Validation

---

## ⚠️ Important: Heart Disease Evaluation Metrics

`HeartDisease_2.ipynb` and `HeartDisease_3.ipynb` contain evaluation-metric calculations that depend on variables created in earlier cells.

### `HeartDisease_3.ipynb`

**Run the first cell before running the evaluation-metric cell.**

The notebook performs model evaluation more than once because it evaluates the model both:

1. Before removing unwanted features
2. After removing unwanted features

The second evaluation is used to compare whether removing unnecessary features improves model performance.

### Recommended execution order

```text
1. Run the first/import cell
        ↓
2. Run EDA cells
        ↓
3. Run preprocessing cells
        ↓
4. Run feature-selection cells
        ↓
5. Run model-training cells
        ↓
6. Run evaluation metrics
        ↓
7. Run multiple-algorithm comparison
        ↓
8. Run feature-removal section
        ↓
9. Run the final evaluation metrics
```

> **Important:** Do not execute the evaluation section independently before running the cells that create the required variables.

---

# 🏏 IPL Analysis

The `IPL-Analysis` folder contains data analysis and visualization work using IPL match data.

```text
IPL-Analysis/
│
├── IPL_Analysis.ipynb
├── IPL_Analysis_01.ipynb
└── matches.csv
```

The notebooks explore IPL match data using Python data-analysis and machine-learning libraries.

Topics include:

* Dataset exploration
* Data preprocessing
* Missing-value handling
* Feature transformation
* Visualization
* Classification experimentation

Libraries used include:

```python
pandas
numpy
matplotlib
seaborn
scikit-learn
```

---

# 🗂️ Project Structure

```text
DataAnalysis-main/
│
├── Classification-Algorithms/
│   │
│   ├── Iris.csv
│   ├── KNN.ipynb
│   ├── Logistic_Regression.ipynb
│   ├── SVM.ipynb
│   │
│   └── test.csv/
│       └── test.csv
│
├── Data-Preprocessing/
│   │
│   ├── Lable_Encoder.ipynb
│   ├── ONE HOT ENCODING.ipynb
│   └── pipeline.ipynb
│
├── Heart-Disease-Analysis/
│   │
│   ├── HeartDisease.ipynb
│   ├── HeartDisease_2.ipynb
│   ├── HeartDisease_3.ipynb
│   └── heart.csv
│
├── IPL-Analysis/
│   │
│   ├── IPL_Analysis.ipynb
│   ├── IPL_Analysis_01.ipynb
│   └── matches.csv
│
├── Regression-Algorithms/
│   │
│   ├── Data.csv
│   └── Linear_Regression.ipynb
│
├── Placements.csv
├── test.csv.zip
│
└── README.md
```

---

# 📚 Notebook Guide

| Folder                      | Notebook                    | Purpose                                  |
| --------------------------- | --------------------------- | ---------------------------------------- |
| `Data-Preprocessing`        | `Lable_Encoder.ipynb`       | Label Encoding                           |
| `Data-Preprocessing`        | `ONE HOT ENCODING.ipynb`    | One-Hot Encoding                         |
| `Data-Preprocessing`        | `pipeline.ipynb`            | Machine Learning Pipelines               |
| `Classification-Algorithms` | `KNN.ipynb`                 | K-Nearest Neighbors                      |
| `Classification-Algorithms` | `Logistic_Regression.ipynb` | Logistic Regression                      |
| `Classification-Algorithms` | `SVM.ipynb`                 | Support Vector Machine                   |
| `Regression-Algorithms`     | `Linear_Regression.ipynb`   | Linear Regression                        |
| `Heart-Disease-Analysis`    | `HeartDisease.ipynb`        | EDA & preprocessing                      |
| `Heart-Disease-Analysis`    | `HeartDisease_2.ipynb`      | Feature selection & multiple models      |
| `Heart-Disease-Analysis`    | `HeartDisease_3.ipynb`      | Feature reduction & accuracy improvement |
| `IPL-Analysis`              | `IPL_Analysis.ipynb`        | IPL data analysis                        |
| `IPL-Analysis`              | `IPL_Analysis_01.ipynb`     | Extended IPL analysis                    |

---

# 📊 Datasets

## `Iris.csv`

The Iris dataset is used for classification experiments.

Typical features include:

```text
SepalLength
SepalWidth
PetalLength
PetalWidth
Species
```

Useful for experimenting with:

* KNN
* Logistic Regression
* SVM

---

## `heart.csv`

Dataset used for the Heart Disease Analysis project.

The dataset is used for:

* Exploratory Data Analysis
* Data preprocessing
* Feature selection
* Classification
* Model comparison
* Model evaluation

---

## `matches.csv`

IPL match dataset used for analysis and visualization.

---

## `Data.csv`

Dataset used with the regression and preprocessing experiments.

---

## `Placements.csv`

Dataset containing student placement-related information and used for predictive/data-analysis exercises.

---

# 🛠️ Technologies Used

| Technology          | Purpose                        |
| ------------------- | ------------------------------ |
| 🐍 Python           | Core programming language      |
| 🐼 Pandas           | Data manipulation and analysis |
| 🔢 NumPy            | Numerical computing            |
| 📊 Matplotlib       | Data visualization             |
| 🌊 Seaborn          | Statistical visualization      |
| 🤖 Scikit-learn     | Machine Learning               |
| 📓 Jupyter Notebook | Interactive development        |
| 📄 CSV              | Dataset storage                |

---

# 💻 Installation

## 1. Clone the Repository

```bash
git clone https://github.com/YOUR_USERNAME/DataAnalysis.git
```

Replace `YOUR_USERNAME` with your GitHub username.

---

## 2. Navigate to the Project

```bash
cd DataAnalysis
```

---

## 3. Install Required Libraries

```bash
pip install pandas numpy matplotlib seaborn scikit-learn jupyter
```

---

# ▶️ Running the Project

Start Jupyter Notebook:

```bash
jupyter notebook
```

Or use JupyterLab:

```bash
jupyter lab
```

Then navigate to the required folder and open the corresponding notebook.

For example:

```text
Data-Preprocessing/
Classification-Algorithms/
Regression-Algorithms/
Heart-Disease-Analysis/
IPL-Analysis/
```

Run notebook cells **in order**, especially in the Heart Disease notebooks where later cells depend on variables created earlier.

---

# 🔬 Machine Learning Workflow

The general workflow followed throughout this repository is:

```text
                 Dataset
                    │
                    ▼
             Data Inspection
                    │
                    ▼
                  EDA
                    │
                    ▼
            Data Preprocessing
                    │
          ┌─────────┴─────────┐
          ▼                   ▼
     Numerical             Categorical
     Processing             Encoding
          │                   │
          └─────────┬─────────┘
                    ▼
             Feature Selection
                    │
                    ▼
              Train/Test Split
                    │
                    ▼
              Model Training
                    │
                    ▼
                Prediction
                    │
                    ▼
              Model Evaluation
                    │
                    ▼
             Model Comparison
```

---

# 📏 Model Evaluation

Depending on the problem, different evaluation techniques are explored.

### Classification Metrics

* Accuracy
* Confusion Matrix
* Precision
* Recall
* F1-Score
* Classification Report

### Cross-Validation

Cross-validation is used in the Heart Disease project to estimate model performance across multiple data splits.

Example:

```python
from sklearn.model_selection import cross_val_score

scores = cross_val_score(
    model,
    X,
    y,
    cv=5,
    scoring="accuracy"
)

print(scores)
print(scores.mean())
```

---

# 🎯 Learning Objectives

This repository is intended to build practical understanding of:

* Python for Data Science
* Pandas
* NumPy
* Data Cleaning
* Exploratory Data Analysis
* Data Visualization
* Missing-Value Handling
* Categorical Data
* Label Encoding
* One-Hot Encoding
* Machine Learning Pipelines
* Feature Selection
* Classification
* Regression
* Cross-Validation
* Model Evaluation
* Model Comparison

---

# 📈 Current Machine Learning Coverage

```text
                    Machine Learning
                           │
             ┌─────────────┴─────────────┐
             │                           │
      Supervised Learning         Data Preprocessing
             │                           │
      ┌──────┴──────┐              ┌─────┴─────┐
      │             │              │           │
Classification  Regression      Encoding    Pipeline
      │             │
 ┌────┼────┐        │
 ▼    ▼    ▼        ▼
KNN  SVM  Logistic  Linear
         Regression Regression
```

---

# 🔮 Future Improvements

Planned additions to this repository include:

* 📊 More Exploratory Data Analysis projects
* 📈 Advanced Data Visualization
* 📐 Feature Scaling
* 🔬 Feature Engineering
* 🌳 Decision Trees
* 🌲 Random Forest
* 🚀 Gradient Boosting
* 🧠 Neural Networks
* 🎯 Hyperparameter Tuning
* 🔄 Advanced Cross-Validation
* 📊 ROC-AUC Analysis
* 📉 Confusion Matrix Visualization
* 🏆 Model Performance Comparison
* 🤖 More Real-World Machine Learning Projects

---

# 🤝 Contributing

This repository is primarily a personal learning project, but improvements and suggestions are welcome.

### Fork the repository

```bash
git fork
```

### Clone your fork

```bash
git clone https://github.com/YOUR_USERNAME/DataAnalysis.git
```

### Create a branch

```bash
git checkout -b feature/new-analysis
```

### Commit your changes

```bash
git add .
git commit -m "Add new data analysis"
```

### Push the branch

```bash
git push origin feature/new-analysis
```

Then open a Pull Request.

---

# ⭐ Support

If you find this repository useful for learning **Data Analysis or Machine Learning**, consider giving it a ⭐ on GitHub.

---

# 👨‍💻 Author

## Sri Vardhan

**Python Developer | Data Analysis Learner | Machine Learning Enthusiast**

Currently exploring:

* 🐍 Python
* 📊 Data Analysis
* 🤖 Machine Learning
* 🧠 Artificial Intelligence
* 🌐 Web Development

---

# 📜 License

This project is created primarily for **educational and learning purposes**.

---

<p align="center">

### 🐍 Learn • Analyze • Build • Improve 🚀

<strong>Made with Python & curiosity ❤️</strong>

</p>
