# BILE Initiative — ML Capstone Datasets

This repository contains the prepared datasets students need for the
**Machine Learning Capstone Projects**.

Students should use the datasets provided in this repository unless the
instructor approves a different dataset.

---

## Important: Classification vs Regression

All five projects in this repository are **Classification projects**.

- **Classification** = the model predicts a category or class.
  Examples: `Approved / Not Approved`, `Heart Disease / No Heart Disease`,
  or a recommended crop name.

- **Regression** = the model predicts a continuous numerical value.
  Example: `house price = 85,000`.

**None of these five projects requires regression.**

---

## Dataset Summary

| Dataset | Project Idea | Main ML Task | Target / Classes | Rows | Source |
|---|---|---|---|---:|---|
| `loan_approval.csv` | Loan Approval Prediction | **Classification** | `Loan_Status`: `Y`, `N` | 614 | Public Loan Prediction Dataset |
| `Crop_recommendation.csv` | Crop Recommendation System | **Classification** | `crop`: Recommended Crop | Check packaged CSV | Kaggle Crop Recommendation Dataset |
| `heart_disease.csv` | Heart Disease Risk Prediction | **Classification** | `target_binary`: `0`, `1` | 1,025 | | `Crop_recommendation.csv` | Crop Recommendation System |**Classification** | `crop`: Recommended Crop | Check packaged CSV | Kaggle Crop Recommendation Dataset |Kaggle Heart Disease-derived Extended Dataset |
| `student_dropout.csv` | Student Dropout Prediction | **Classification** | `Dropout`: `0`, `1` | 10,000 | Kaggle Student Dropout Prediction Dataset |
| `Phishing_Email.csv` | AI Email Phishing Detector | **Classification (NLP)** | `Email Type`: `Safe Email`, `Phishing Email` | 18,650 | Hugging Face copy of Kaggle Phishing Email Dataset |

---

# 1. Loan Approval Prediction

## Project Information

**ML Task:** Classification  
**Target Variable:** `Loan_Status`

### Classes

- `Y` = Loan Approved
- `N` = Loan Not Approved

The objective of this project is to build a machine learning model that
predicts whether a loan application is likely to be approved based on
applicant and financial information.

## Main Input Features

The dataset contains features such as:

- `Gender`
- `Married`
- `Dependents`
- `Education`
- `Self_Employed`
- `ApplicantIncome`
- `CoapplicantIncome`
- `LoanAmount`
- `Loan_Amount_Term`
- `Credit_History`
- `Property_Area`

## Student Work

Students must:

- Load and inspect the dataset.
- Identify the input features and target variable.
- Handle missing values.
- Encode categorical variables.
- Perform Exploratory Data Analysis (EDA).
- Prepare features `X` and target `y`.
- Split the dataset into training and testing sets.
- Train at least two classification models.
- Evaluate and compare the models.
- Select the best-performing model.
- Save the final trained model.
- Build a functional user interface.
- Allow users to enter applicant information.
- Display the predicted loan approval result.

## Dataset File

`loan_approval/loan_approval.csv`

---

# 2. Crop Recommendation System

## Project Information

**ML Task:** Classification  
**Target Variable:** `crop`

The objective of this project is to build a machine learning model that
recommends a suitable crop based on soil nutrients and environmental
conditions.

The model receives soil and climate information and predicts the
recommended crop.

## Input Features

The dataset contains:

- `N` — Nitrogen content in soil (kg/ha)
- `P` — Phosphorus content in soil (kg/ha)
- `K` — Potassium content in soil (kg/ha)
- `temperature` — Average temperature (°C)
- `humidity` — Relative humidity (%)
- `ph` — Soil pH level
- `rainfall` — Annual rainfall (mm)

## Target Variable

`crop`

The `crop` column contains the recommended crop name.

Example:

N = 90  
P = 42  
K = 43  
Temperature = 20.8°C  
Humidity = 82%  
pH = 6.5  
Rainfall = 202 mm

Output:

`Recommended Crop → rice`

## Student Work

Students must:

- Load and inspect the dataset.
- Identify the seven input features.
- Identify `crop` as the target variable.
- Check missing values and duplicates.
- Perform Exploratory Data Analysis (EDA).
- Analyze soil and environmental features.
- Prepare features `X` and target `y`.
- Split the dataset into training and testing sets.
- Train at least two classification models.
- Evaluate the models using appropriate classification metrics.
- Compare model performance.
- Select the best-performing model.
- Save the final trained model.
- Build a functional user interface.
- Allow the user to enter:
  - N
  - P
  - K
  - Temperature
  - Humidity
  - pH
  - Rainfall
- Display the recommended crop.

## Dataset File

`crop_recommendation/Crop_recommendation.csv`

## Dataset Source

Kaggle — Crop Recommendation Dataset

https://www.kaggle.com/datasets/miadul/crop-recommendation-dataset

## Important Dataset Note

The Kaggle dataset documentation states that this dataset is
**synthetically generated**.

Therefore, students should treat this project as an educational machine
learning prototype and should not present the application as a
production agricultural advisory system.

---

# 3. Heart Disease Risk Prediction

## Project Information

**ML Task:** Classification  
**Classification Type:** Binary Classification  
**Target Variable:** `target_binary`

### Classes

- `0` = No Heart Disease
- `1` = Heart Disease

The objective of this project is to build a machine learning model that
predicts whether a patient belongs to the heart-disease or
no-heart-disease class based on clinical information.

The updated dataset contains **1,025 records**.

## Main Input Features

The dataset contains 13 common heart-disease prediction features:

- `age`
- `sex`
- `cp` — Chest pain type
- `trestbps` — Resting blood pressure
- `chol` — Serum cholesterol
- `fbs` — Fasting blood sugar
- `restecg` — Resting ECG result
- `thalach` — Maximum heart rate achieved
- `exang` — Exercise-induced angina
- `oldpeak`
- `slope`
- `ca`
- `thal`

## Target Variable

Students must use:

`target_binary`

Do **not** use the original `num` column as the project target.

### Target Meaning

`0 → No Heart Disease`

`1 → Heart Disease`

## Student Work

Students must:

- Load and inspect the dataset.
- Check missing values.
- Perform Exploratory Data Analysis (EDA).
- Identify the 13 input features.
- Use `target_binary` as the target.
- Prepare features `X` and target `y`.
- Split data into training and testing sets.
- Train at least two classification models.
- Evaluate the models.
- Use classification metrics such as:
  - Accuracy
  - Precision
  - Recall
  - F1-score
  - Confusion Matrix
- Compare model performance.
- Select the best-performing model.
- Save the final trained model.
- Build a functional user interface.
- Allow users to enter the required patient information.
- Display the prediction result clearly.

## Dataset File

`heart_disease/heart_disease.csv`

## Dataset Source

Kaggle — Heart Disease Dataset  
Extended from the UCI Heart Disease Dataset.

https://www.kaggle.com/datasets/sintariosatya/heart-disease-dataset

## Important Dataset Note

This dataset contains **1,025 records** and is an extended version of the
UCI Heart Disease Dataset.

The dataset combines original heart-disease records with
**synthetically generated records**.

Students should mention this limitation in their final README/report.

> **Educational use only:** This project is a machine learning learning
> exercise and must not be presented as a medical diagnosis system.

---

# 4. Student Dropout Prediction

## Project Information

**ML Task:** Classification  
**Classification Type:** Binary Classification  
**Target Variable:** `Dropout`

The objective of this project is to identify students who may be at risk
of dropping out so educational institutions can provide early support.

The updated dataset contains:

- **10,000 student records**
- **19 columns**
- Numerical and categorical features
- Missing values in some columns
- Binary dropout target

## Target Variable

`Dropout`

### Classes

- `0` = Student Retained / Did Not Drop Out
- `1` = Student Dropped Out

This means students are solving a straightforward **Binary
Classification** problem.

## Main Features

The dataset includes information such as:

- `Age`
- `Gender`
- `Family_Income`
- `Internet_Access`
- `Study_Hours_per_Day`
- `Attendance_Rate`
- `Assignment_Delay_Days`
- `Travel_Time_Minutes`
- `Part_Time_Job`
- `Scholarship`
- `Stress_Index`
- `GPA`
- `Semester_GPA`
- `CGPA`
- `Semester`
- `Department`
- `Parental_Education`

`Student_ID` is an identifier and should normally not be used as a
predictive feature.

## Student Work

Students must:

- Load and inspect the dataset.
- Identify `Dropout` as the target.
- Remove or exclude identifiers such as `Student_ID` from model features.
- Check missing values.
- Check duplicate records.
- Analyze numerical and categorical features.
- Perform Exploratory Data Analysis (EDA).
- Examine the distribution of the target variable.
- Prepare features `X` and target `y`.
- Encode categorical variables where necessary.
- Split the dataset into training and testing sets.
- Train at least two classification models.
- Evaluate the models using:
  - Accuracy
  - Precision
  - Recall
  - F1-score
  - Confusion Matrix
- Compare model performance.
- Select the best-performing model.
- Save the final model and preprocessing steps.
- Build a functional user interface.
- Allow student information to be entered.
- Display the predicted dropout risk.

## Dataset File

`student_dropout/student_dropout.csv`

## Dataset Source

Kaggle — Student Dropout Prediction Dataset

https://www.kaggle.com/datasets/meharshanali/student-dropout-prediction-dataset

## Important Dataset Note

This dataset contains **10,000 synthetic student records** designed for
student-dropout prediction.

The target is already binary:

`0 = Retained`

`1 = Dropped Out`

The dataset documentation reports an approximate dropout rate of
**23.5%**.

Students should mention that the dataset is synthetic when documenting
the limitations of the project.

---

# 5. AI Email Phishing Detector

## Project Information

**ML Task:** Classification using NLP  
**Classification Type:** Binary Classification  
**Target Variable:** `Email Type`

The objective of this project is to build an NLP machine learning model
that determines whether an email is safe or potentially phishing.

## Input

`Email Text`

## Target Variable

`Email Type`

### Classes

- `Safe Email`
- `Phishing Email`

## Student Work

Students must:

- Load and inspect the email dataset.
- Identify `Email Text` as the input.
- Identify `Email Type` as the target.
- Clean and preprocess email text.
- Handle empty or invalid email text.
- Split the dataset into training and testing sets.
- Convert text into numerical features using:
  - TF-IDF, or
  - CountVectorizer
- Train at least two NLP classification models.

Recommended beginner-friendly models include:

- Naive Bayes
- Logistic Regression

Students must then:

- Evaluate both models.
- Compare their performance.
- Select the best-performing model.
- Save the text vectorizer and classifier or complete pipeline.
- Build a functional user interface.
- Allow the user to paste email text.
- Display:
  - `Safe Email`, or
  - `Phishing Email`

## Dataset File

`phishing_email/Phishing_Email.csv`

---

# Repository Structure

```text
datasets/
├── README.md
├── SOURCES.md
│
├── loan_approval/
│   └── loan_approval.csv
│
├── crop_recommendation/
│   └── Crop_recommendation(1).csv
│
├── heart_disease/
│   └── heart_disease.csv
│
├── student_dropout/
│   └── student_dropout_dataset_v3.csv
│
└── phishing_email/
    └── Phishing_Email.csv