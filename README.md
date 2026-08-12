# 📊 Data Analysis with Python

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.x-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python">
  <img src="https://img.shields.io/badge/Pandas-Data%20Analysis-150458?style=for-the-badge&logo=pandas&logoColor=white" alt="Pandas">
  <img src="https://img.shields.io/badge/Scikit--learn-Preprocessing-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white" alt="Scikit-learn">
  <img src="https://img.shields.io/badge/Jupyter-Notebook-F37626?style=for-the-badge&logo=jupyter&logoColor=white" alt="Jupyter">
</p>

<p align="center">
  <strong>A practical Python data analysis project focused on exploring, cleaning, and preprocessing employee data using Pandas and Scikit-learn.</strong>
</p>

---

## 📖 About the Project

This project demonstrates the fundamental steps involved in preparing a real-world dataset for data analysis and machine learning.

The project uses an **employee dataset** containing information about:

- 👤 Age
- ⚧️ Gender
- 🎓 Education
- 💼 Experience
- 🏢 Department
- 🌆 City
- 📈 Job Level
- ⭐ Performance Score
- 🏢 Years at Company
- 💰 Salary

The analysis is performed using **Pandas**, while categorical data preprocessing is demonstrated using **Scikit-learn's `LabelEncoder`**.

---

## ✨ Features

- 📥 Load CSV data using Pandas
- 🔍 Explore the dataset
- 📋 Inspect DataFrame structure
- 🔢 Separate numerical and categorical columns
- ❓ Detect missing values
- 🧹 Handle missing numerical values
- 🗑️ Remove rows with missing critical values
- 🔤 Identify categorical features
- 🔢 Encode categorical values
- 📊 Inspect cleaned data
- 🤖 Prepare data for future machine-learning workflows

---

## 📂 Project Structure

```text
DataAnalysis/
│
├── 📊 Data.csv
│   └── Dataset used for data analysis and preprocessing
│
├── 🌸 Iris.csv
│   └── Iris dataset used for machine learning experiments
│
├── 🎓 Placements.csv
│   └── Student placement dataset used for prediction and analysis
│
├── 📁 test.csv/
│   └── test.csv
│       └── Additional test dataset
│
├── 🧠 KNN.ipynb
│   └── K-Nearest Neighbors classification implementation
│
├── 🏷️ Lable_Encoder.ipynb
│   └── Categorical data encoding using Label Encoding
│
├── 📈 Linear_Regression.ipynb
│   └── Linear Regression implementation and prediction
│
├── 🔐 Logistic_Regression.ipynb
│   └── Logistic Regression classification implementation
│
├── 🔢 ONE HOT ENCODING.ipynb
│   └── Categorical feature encoding using One-Hot Encoding
│
├── ⚙️ pipeline.ipynb
│   └── Machine learning preprocessing and pipeline implementation
│
├── 🧠 SVM.ipynb
│   └── Support Vector Machine classification implementation
│
└── 📖 README.md
    └── Project documentation
```

### 📌 File Overview

| File                        | Description                                                 |
| --------------------------- | ----------------------------------------------------------- |
| `Data.csv`                  | Dataset used for data analysis and preprocessing            |
| `Iris.csv`                  | Iris dataset for classification experiments                 |
| `Placements.csv`            | Student placement dataset for predictive analysis           |
| `test.csv/test.csv`         | Additional test dataset                                     |
| `KNN.ipynb`                 | Implementation of the K-Nearest Neighbors algorithm         |
| `Lable_Encoder.ipynb`       | Demonstrates categorical data encoding using Label Encoding |
| `Linear_Regression.ipynb`   | Linear Regression model implementation                      |
| `Logistic_Regression.ipynb` | Logistic Regression classification model                    |
| `ONE HOT ENCODING.ipynb`    | Demonstrates One-Hot Encoding for categorical features      |
| `pipeline.ipynb`            | Demonstrates ML preprocessing and pipeline creation         |
| `SVM.ipynb`                 | Support Vector Machine implementation                       |
| `README.md`                 | Project documentation                                       |

### 🧠 Machine Learning Topics Covered

This repository currently covers:

* 📊 Data Analysis & Preprocessing
* 🧹 Data Cleaning
* 🏷️ Label Encoding
* 🔢 One-Hot Encoding
* ⚙️ Machine Learning Pipelines
* 📍 K-Nearest Neighbors (KNN)
* 📈 Linear Regression
* 🔐 Logistic Regression
* 🧠 Support Vector Machines (SVM)

> **Note:** The repository also contains `test.csv.zip`. If this archive is only being used as a source for `test.csv`, consider keeping either the ZIP or extracted dataset in the repository rather than both, to avoid unnecessary duplication.

---

## 🛠️ Technologies Used

| Technology | Purpose |
|------------|---------|
| 🐍 Python | Programming language |
| 🐼 Pandas | Data manipulation and analysis |
| 🤖 Scikit-learn | Data preprocessing |
| 📓 Jupyter Notebook | Interactive analysis |
| 📄 CSV | Dataset format |

---

# 🔎 Analysis Workflow

The project follows a basic data preprocessing pipeline:

```text
             Employee Dataset
                    │
                    ▼
            Load Data with Pandas
                    │
                    ▼
              Explore Dataset
                    │
                    ▼
          Inspect DataFrame Info
                    │
                    ▼
        ┌───────────┴───────────┐
        ▼                       ▼
 Numerical Data          Categorical Data
        │                       │
        ▼                       ▼
 Handle Missing Values    Identify Categories
        │                       │
        └───────────┬───────────┘
                    ▼
          Categorical Encoding
                    │
                    ▼
             Cleaned Dataset
                    │
                    ▼
       Ready for Further Analysis
```

---

# 📚 Concepts Covered

## 1. Loading Data

The dataset is loaded using Pandas:

```python
import pandas as pd

df = pd.read_csv("Data.txt")
```

---

## 2. Exploring the Dataset

The project uses:

```python
df.head()
```

to view the first few records.

The structure and data types are inspected using:

```python
df.info()
```

---

## 3. Selecting Numerical Columns

Numerical features are selected using:

```python
numerical_values = df.select_dtypes(
    include=["int64", "float64"]
)
```

This separates columns such as:

- Age
- Experience
- Performance Score
- Years at Company
- Salary

---

## 4. Selecting Categorical Columns

Categorical features are identified using:

```python
categorical_values = df.select_dtypes(
    exclude=["int64", "float64"]
)
```

Examples include:

- Gender
- Education
- Department
- City
- Job Level

---

## 5. Handling Missing Values

Missing values are checked using:

```python
df.isnull().sum()
```

Numerical missing values are handled using the mean:

```python
nv = numerical_values.fillna(
    numerical_values.mean()
)
```

The project also removes rows where important values are missing:

```python
df = df.dropna(
    subset=["Experience", "Performance_Score"]
)
```

---

## 6. Categorical Encoding

The project demonstrates categorical encoding using `LabelEncoder`.

```python
from sklearn.preprocessing import LabelEncoder

le = LabelEncoder()

scd = [
    "Gender",
    "Education",
    "Job_Level",
    "Department",
    "City"
]

for col in scd:
    df[col] = le.fit_transform(df[col])
```

This converts categorical values into numerical representations that can be used by machine-learning algorithms.

### Example

Before encoding:

```text
Education
----------
Bachelors
Masters
PhD
```

After encoding:

```text
Education
----------
0
1
2
```

> **Note:** `LabelEncoder` is generally intended for encoding a target label. For multiple categorical feature columns, `OrdinalEncoder` or `OneHotEncoder` may be more appropriate depending on the machine-learning problem.

---

# 📊 Dataset

The dataset contains **30 employee records** with the following features:

| Column | Description |
|--------|-------------|
| `Age` | Employee age |
| `Gender` | Employee gender |
| `Education` | Highest education level |
| `Experience` | Years of professional experience |
| `Department` | Employee department |
| `City` | Employee location |
| `Job_Level` | Employee job level |
| `Performance_Score` | Performance rating |
| `Years_at_Company` | Years spent at the company |
| `Salary` | Employee salary |

---

# 🚀 Getting Started

## 1. Clone the Repository

```bash
git clone https://github.com/YOUR_USERNAME/DataAnalysis.git
```

## 2. Navigate to the Project

```bash
cd DataAnalysis
```

## 3. Install Required Libraries

```bash
pip install pandas scikit-learn jupyter
```

Or install them together:

```bash
pip install pandas scikit-learn notebook
```

## 4. Start Jupyter Notebook

```bash
jupyter notebook
```

Then open:

```text
DataAnalysis.ipynb
```

---

# 💻 Example

Load the dataset:

```python
import pandas as pd

df = pd.read_csv("Data.txt")

print(df.head())
```

Check missing values:

```python
print(df.isnull().sum())
```

View dataset information:

```python
df.info()
```

---

# 🎯 Learning Objectives

This project is designed to strengthen understanding of:

- 🐼 Pandas DataFrames
- 📥 Data loading
- 🔍 Exploratory data analysis
- 📊 Data types
- 🔢 Numerical features
- 🔤 Categorical features
- ❓ Missing-value detection
- 🧹 Data cleaning
- 🔄 Data preprocessing
- 🏷️ Label encoding
- 🤖 Machine-learning preparation

---

# 🔮 Future Improvements

The project can be extended with:

- 📊 Exploratory Data Analysis (EDA)
- 📈 Data visualization using Matplotlib
- 🎨 Statistical visualizations using Seaborn
- 🔥 Correlation analysis
- 💰 Salary analysis
- 📍 City-wise salary comparison
- 🏢 Department-wise analysis
- ⭐ Performance analysis
- 📈 Experience vs Salary analysis
- 🤖 Salary prediction using Machine Learning
- 🧠 Feature engineering
- 🔬 Model evaluation
- 📊 Interactive dashboards

---

# 📈 Possible Future Analysis

Some interesting questions that can be explored using this dataset:

### 💰 Salary Analysis

- Does experience affect salary?
- Which department has the highest average salary?
- How does salary change with job level?

### ⭐ Performance Analysis

- Does experience correlate with performance?
- Which departments have the highest performance scores?

### 🎓 Education Analysis

- Does higher education correspond to higher salaries?
- How does education level vary across departments?

### 🌆 Location Analysis

- Which city has the highest average salary?
- Are certain departments concentrated in specific cities?

---

# 🤝 Contributing

Contributions and improvements are welcome!

### 1. Fork the repository

```bash
git fork
```

### 2. Create a feature branch

```bash
git checkout -b feature/new-analysis
```

### 3. Commit your changes

```bash
git add .

git commit -m "Add new data analysis"
```

### 4. Push your branch

```bash
git push origin feature/new-analysis
```

### 5. Open a Pull Request

---

# ⭐ Support

If you found this project useful or educational, consider giving the repository a ⭐ **Star**.

It helps support the project and encourages further development.

---

# 📄 License

This project is created for **educational and learning purposes**.

---

# 👨‍💻 Author

**Sri Vardhan**

🐍 Python Developer | 📊 Data Analysis Learner | 🤖 AI Enthusiast

Interested in building practical Python applications, exploring Data Science, learning Machine Learning, and developing AI-powered projects.

---

<p align="center">

### 📊 Analyze • Clean • Transform • Learn 🚀

**Happy Data Analyzing! 🐍**

</p>
