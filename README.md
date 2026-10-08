# 💰 Salary Prediction Model

> A Machine Learning classification project that predicts whether an employee's salary is **above $100K** based on their **company, job role, and education level**.

![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-150458?logo=pandas)
![Scikit--learn](https://img.shields.io/badge/Scikit--learn-Machine%20Learning-F7931E?logo=scikit-learn)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange?logo=jupyter)
![License](https://img.shields.io/badge/License-MIT-green)

---

## 📌 Overview

This project uses Machine Learning to determine whether an employee is likely to earn **more than $100,000** based on three key factors:

* 🏢 **Company**
* 💼 **Job Role**
* 🎓 **Education Level**

The project demonstrates a complete beginner-friendly Machine Learning workflow, including data exploration, preprocessing, feature encoding, feature selection, model training, prediction, and evaluation.

The final model uses a **Decision Tree Classifier** and achieves an accuracy of **76.3%** on the test dataset.

---

## 🎯 Problem Statement

Salary can depend on several factors such as company, job position, and educational background.

The objective of this project is to build a classification model that answers:

> **"Is this employee's salary likely to be more than $100K?"**

The target variable is:

* `0` → Salary ≤ $100K
* `1` → Salary > $100K

---

## 📊 Dataset

The dataset contains **5,000 records** and the following features:

| Feature                 | Description                                             |
| ----------------------- | ------------------------------------------------------- |
| `company`               | Company where the employee works                        |
| `job`                   | Employee's job role                                     |
| `degree`                | Employee's highest degree                               |
| `salary_more_then_100k` | Target variable indicating whether salary exceeds $100K |

### Dataset Structure

```text
5,000 rows
4 columns
3 input features
1 target variable
```

The dataset contains no missing values.

---

## 🔄 Machine Learning Workflow

The project follows this pipeline:

```text
Raw Dataset
     ↓
Data Exploration
     ↓
Train/Test Split
     ↓
Feature Encoding
     ↓
Feature Scaling
     ↓
Feature Selection
     ↓
Decision Tree Classifier
     ↓
Predictions
     ↓
Model Evaluation
```

---

## 🧹 Data Preprocessing

### 1. Train/Test Split

The dataset is divided into:

* **80% Training Data** → 4,000 records
* **20% Testing Data** → 1,000 records

A fixed `random_state=42` is used for reproducibility.

### 2. Categorical Encoding

Different encoding techniques are applied to the categorical features:

**One-Hot Encoding**

* Company
* Job Role

**Ordinal Encoding**

* Education Level

### 3. Feature Scaling

`MinMaxScaler` is used to scale the transformed features.

### 4. Feature Selection

`SelectKBest` with the **Chi-Square (`chi2`) test** is used to select the four most relevant features.

---

## 🤖 Machine Learning Model

The final model is a:

### 🌳 Decision Tree Classifier

The complete preprocessing and classification workflow is implemented using a Scikit-learn `Pipeline`.

```text
OneHotEncoder / OrdinalEncoder
            ↓
       MinMaxScaler
            ↓
       SelectKBest
            ↓
  DecisionTreeClassifier
```

Using a pipeline helps keep preprocessing and model training organized into a single workflow.

---

## 📈 Model Performance

The model was evaluated on **1,000 unseen test samples**.

### Accuracy

**76.3%**

```text
Accuracy: 76.3%
```

### Classification Report

| Class       | Precision |   Recall | F1-Score |
| ----------- | --------: | -------: | -------: |
| 0 — ≤ $100K |      0.74 |     0.65 |     0.69 |
| 1 — > $100K |      0.78 |     0.84 |     0.81 |
| **Overall** |  **0.76** | **0.76** | **0.76** |

### Confusion Matrix

```text
[[264, 143],
 [ 94, 499]]
```

The model performs particularly well at identifying employees whose predicted salary is **above $100K**.

---

## 🛠️ Technologies Used

* **Python**
* **Pandas** — Data manipulation and analysis
* **NumPy** — Numerical operations
* **Matplotlib** — Data visualization
* **Seaborn** — Data visualization
* **Scikit-learn** — Machine Learning
* **Jupyter Notebook / Google Colab** — Development environment

---

## 📁 Project Structure

```text
Salary-Prediction-Model/
│
├── Salary_Prediction_model.ipynb
├── salaries_dataset.csv
├── LICENSE
└── README.md
```

---

## 🚀 How to Run

### 1. Clone the repository

```bash
git clone https://github.com/Umer00/Salary-Prediction-Model.git
```

### 2. Navigate to the project

```bash
cd Salary-Prediction-Model
```

### 3. Install dependencies

```bash
pip install pandas numpy matplotlib seaborn scikit-learn jupyter
```

### 4. Open the notebook

```bash
jupyter notebook Salary_Prediction_model.ipynb
```

You can also open the notebook directly using **Google Colab**.

---

## 💡 Example Prediction

The model takes information such as:

```text
Company: Google
Job: Computer Programmer
Degree: Masters
```

and predicts whether the employee's salary is likely to be:

```text
> $100K
```

or

```text
≤ $100K
```

---

## 📚 What I Learned

Through this project, I practiced:

* Exploratory Data Analysis
* Data preprocessing
* Handling categorical variables
* One-Hot Encoding
* Ordinal Encoding
* Feature scaling
* Feature selection
* Chi-Square statistical testing
* Scikit-learn Pipelines
* Decision Tree Classification
* Train/Test splitting
* Model evaluation
* Confusion matrices
* Classification reports

---

## 🔮 Future Improvements

Possible improvements for future versions include:

* 🔹 Testing Random Forest and Gradient Boosting models
* 🔹 Hyperparameter tuning
* 🔹 Cross-validation
* 🔹 Adding more salary-related features
* 🔹 Building an interactive prediction web app
* 🔹 Deploying the model as a web application
* 🔹 Adding explainable AI techniques
* 🔹 Comparing multiple classification algorithms

---

## 👨‍💻 Author

**Umer**

Computer Science Student | Aspiring Data Analyst / Data Scientist

GitHub: [@Umer00](https://github.com/Umer00)

---

## 📄 License

This project is licensed under the **MIT License**.
