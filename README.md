📊 Data Analysis & Machine Learning

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.x-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python">
  <img src="https://img.shields.io/badge/Pandas-Data%20Analysis-150458?style=for-the-badge&logo=pandas&logoColor=white" alt="Pandas">
  <img src="https://img.shields.io/badge/NumPy-Numerical%20Computing-013243?style=for-the-badge&logo=numpy&logoColor=white" alt="NumPy">
  <img src="https://img.shields.io/badge/Seaborn-Visualization-4C72B0?style=for-the-badge" alt="Seaborn">
  <img src="https://img.shields.io/badge/Scikit--learn-Machine%20Learning-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white" alt="Scikit-learn">
  <img src="https://img.shields.io/badge/Jupyter-Notebook-F37626?style=for-the-badge&logo=jupyter&logoColor=white" alt="Jupyter">
</p>

<p align="center">
  <strong>A practical collection of Data Analysis, Data Preprocessing, Exploratory Data Analysis, Visualization, and Machine Learning experiments using Python.</strong>
</p>

📖 About

This repository contains hands-on work covering the fundamentals of Data Analysis and Machine Learning with Python.

The project progresses from data exploration and preprocessing to classification and regression algorithms. It also includes a more complete Heart Disease Analysis project that demonstrates exploratory data analysis, feature preprocessing, feature selection, model training, cross-validation, and model evaluation.

Main Areas Covered

📊 Data Analysis with Pandas

🧹 Data Cleaning and Preprocessing

🔍 Exploratory Data Analysis (EDA)

📈 Data Visualization with Matplotlib and Seaborn

🔢 Label Encoding

🔤 One-Hot Encoding

⚙️ Machine Learning Pipelines

📍 K-Nearest Neighbors (KNN)

🔐 Logistic Regression

🧠 Support Vector Machines (SVM)

📈 Linear Regression

❤️ Heart Disease Classification

🌲 Random Forest Classification

📏 Model Evaluation and Cross-Validation

🗂️ Project Structure

DataAnalysis/
│
├── Classification-Algorithms/
│   ├── Iris.csv
│   ├── KNN.ipynb
│   ├── Logistic_Regression.ipynb
│   ├── SVM.ipynb
│   └── test.csv/
│       └── test.csv
│
├── Data-Preprocessing/
│   ├── Lable_Encoder.ipynb
│   ├── ONE HOT ENCODING.ipynb
│   └── pipeline.ipynb
│
├── Heart-Disease-Analysis/
│   ├── heart.csv
│   ├── HeartDisease.ipynb
│   ├── HeartDisease_2.ipynb
│   └── HeartDisease_3.ipynb
│
├── IPL-Analysis/
│   ├── matches.csv
│   ├── IPL_Analysis.ipynb
│   └── IPL_Analysis_01.ipynb
│
├── Regression-Algorithms/
│   ├── Data.csv
│   └── Linear_Regression.ipynb
│
├── Placements.csv
├── test.csv.zip
└── README.md

❤️ Heart Disease Analysis

The Heart-Disease-Analysis folder contains a machine learning project based on the heart.csv dataset.

The objective is to analyze patient-related features and build classification models that predict the HeartDisease target.

Workflow

Heart Disease Dataset
        │
        ▼
Exploratory Data Analysis
        │
        ▼
Data Cleaning
        │
        ▼
Feature Encoding
        │
        ▼
Feature Scaling
        │
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
Evaluation
        │
        ▼
Cross-Validation
        │
        ▼
Feature Reduction & Accuracy Improvement

🔎 Exploratory Data Analysis

The notebooks inspect:

Dataset shape

Data types

Missing values

Duplicate records

Descriptive statistics

Unique categorical values

Value distributions

Relationships between features and HeartDisease

Visualizations include:

Histograms

Box plots

Count plots

🧹 Data Preprocessing

The Heart Disease project demonstrates several preprocessing techniques.

Categorical Encoding

Examples include:

df_copy['Sex'].replace({'M': 1, 'F': 0}, inplace=True)

and:

df_copy['ExerciseAngina'] = df_copy['ExerciseAngina'].map({
    'Y': 1,
    'N': 0
})

One-hot encoding is used for categorical features such as:

ChestPainType

RestingECG

ST_Slope

Feature Scaling

Selected numerical features are standardized using StandardScaler:

cols = ['Age', 'RestingBP', 'Cholesterol', 'MaxHR']

ss = StandardScaler()

df_copy[cols] = ss.fit_transform(df_copy[cols])

🧠 Machine Learning Models

The project explores multiple classification algorithms:

Logistic Regression

Random Forest Classifier

Support Vector Classifier (SVC)

K-Nearest Neighbors (KNN)

Cross-validation is used to compare model performance.

scores = cross_val_score(
    model,
    X,
    y,
    cv=2,
    scoring="accuracy"
)

📏 Model Evaluation

The Heart Disease notebooks use several evaluation metrics:

Accuracy

Confusion Matrix

Classification Report

Cross-Validation Accuracy

Example:

accuracy = accuracy_score(y_test, y_pred)

confusionmatrix = confusion_matrix(y_test, y_pred)

classificationreport = classification_report(y_test, y_pred)

⚠️ Important: HeartDisease_3.ipynb Evaluation Order

Please follow the cell execution order carefully in HeartDisease_3.ipynb.

The notebook evaluates the Random Forest model twice:

First, the model is evaluated using the complete feature set.

Later, unwanted/redundant features are removed and the model is trained and evaluated again to compare the accuracy.

First Evaluation

The first model uses:

features_all
    ↓
X / y
    ↓
train_test_split()
    ↓
RandomForestClassifier
    ↓
prediction
    ↓
accuracy_score
    ↓
confusion_matrix
    ↓
classification_report

Second Evaluation

After removing unwanted features, the notebook creates a new feature set:

features_1
    ↓
X / y
    ↓
train_test_split()
    ↓
RandomForestClassifier
    ↓
prediction
    ↓
accuracy1
    ↓
confusionmatrix
    ↓
classificationreport

🚨 Execution Note

Because the evaluation metrics are used two times, do not run only the final evaluation cell.

Run the cells in order:

1. Run the first model-training/evaluation cell
2. Run its evaluation output cell
3. Continue to the feature-reduction section
4. Run the second model-training/evaluation cell
5. Run the second evaluation output cell

In particular, the second evaluation depends on variables created by the preceding training cell.

If you open the notebook after restarting the Jupyter kernel, Run All or execute the cells sequentially from the beginning to avoid NameError or undefined-variable issues.

📊 Heart Disease Notebook Overview

Notebook

Purpose

HeartDisease.ipynb

Initial Heart Disease EDA and preprocessing

HeartDisease_2.ipynb

Preprocessing, feature selection, Random Forest, and multiple algorithms

HeartDisease_3.ipynb

Extended analysis with feature reduction and a second model evaluation

heart.csv

Heart Disease dataset

🏏 IPL Analysis

The IPL-Analysis folder contains notebooks for analyzing IPL match data.

It uses Pandas and visualization techniques to answer questions such as:

Winning margins

Match results

Team performance

Match statistics

Distribution of match outcomes

Dataset:

IPL-Analysis/matches.csv

🧹 Data Preprocessing

The Data-Preprocessing folder demonstrates common techniques for preparing data for machine learning.

Label Encoding

Lable_Encoder.ipynb demonstrates converting categorical values into numerical representations.

One-Hot Encoding

ONE HOT ENCODING.ipynb demonstrates converting categorical variables into separate binary columns.

Pipelines

pipeline.ipynb demonstrates combining preprocessing and machine learning steps into a reusable Scikit-learn pipeline.

🤖 Classification Algorithms

The Classification-Algorithms folder contains implementations of common classification algorithms.

K-Nearest Neighbors

KNN.ipynb

Demonstrates classification based on the nearest observations.

Logistic Regression

Logistic_Regression.ipynb

Demonstrates classification using Logistic Regression.

Support Vector Machine

SVM.ipynb

Demonstrates classification using Support Vector Machines.

📈 Regression Algorithms

The Regression-Algorithms folder contains regression experiments.

Linear Regression

Linear_Regression.ipynb

Demonstrates predicting a continuous target using Linear Regression.

📚 Datasets

The repository contains several datasets used for experimentation:

Dataset

Purpose

heart.csv

Heart disease classification

Iris.csv

Classification experiments

matches.csv

IPL match analysis

Data.csv

Regression/data analysis experiments

Placements.csv

Placement-related predictive analysis

test.csv

Additional testing data

🛠️ Technologies & Libraries

Technology

Purpose

Python

Core programming language

Pandas

Data manipulation and analysis

NumPy

Numerical computing

Matplotlib

Data visualization

Seaborn

Statistical visualization

Scikit-learn

Machine learning

Jupyter Notebook

Interactive development

💻 Installation

1. Clone the Repository

git clone https://github.com/YOUR_USERNAME/DataAnalysis.git

2. Navigate to the Project

cd DataAnalysis

3. Install Dependencies

pip install pandas numpy matplotlib seaborn scikit-learn jupyter

▶️ Running the Notebooks

Start Jupyter Notebook:

jupyter notebook

Then open the required notebook.

For the Heart Disease project:

Heart-Disease-Analysis/
│
├── HeartDisease.ipynb
├── HeartDisease_2.ipynb
├── HeartDisease_3.ipynb
└── heart.csv

Recommended Execution

Run notebook cells from top to bottom because later cells depend on variables created earlier.

This is especially important for:

HeartDisease_3.ipynb

because the notebook performs model evaluation twice using different feature sets.

🎯 Learning Objectives

This repository is designed to build practical knowledge of:

Python for Data Science

Pandas

NumPy

Data Cleaning

Exploratory Data Analysis

Data Visualization

Categorical Encoding

Feature Scaling

Feature Selection

Train/Test Splitting

Classification

Regression

Random Forest

KNN

SVM

Logistic Regression

Model Evaluation

Cross-Validation

Feature Reduction

🔮 Future Improvements

Planned additions include:

More real-world datasets

Advanced feature engineering

Hyperparameter tuning

ROC-AUC evaluation

Precision/Recall comparison

Advanced ensemble models

Decision Trees

Gradient Boosting

XGBoost

Neural Networks

Improved visualization

Automated model comparison

🤝 Contributing

This is primarily a learning and experimentation repository. Suggestions, improvements, and educational contributions are welcome.

If you want to contribute:

git checkout -b feature/new-analysis

Make your changes, then:

git add .
git commit -m "Add new analysis"
git push origin feature/new-analysis

👨‍💻 Author

Sri Vardhan

Python Developer | Data Analysis Learner | Machine Learning Enthusiast

Currently exploring:

Python

Data Analysis

Machine Learning

Artificial Intelligence

Web Development

📜 License

This repository is intended primarily for educational and learning purposes.

<p align="center">

🐍 Learn • Analyze • Build • Improve 🚀

</p>
