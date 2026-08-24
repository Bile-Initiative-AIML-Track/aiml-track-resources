# BILE Initiative — ML Capstone Datasets

This repository contains the datasets students need for the **Machine Learning capstone projects**.

---

# Important: Classification vs Regression

All six projects in this repository are **Classification Projects**.

- **Classification** = the model predicts a category/class such as `Approved / Not Approved`.
- **Regression** = the model predicts a continuous number such as `house price = 85,000`.
- **None of these five projects requires regression.**

| Dataset | Project Idea | Main ML Task | Classification Type | Target / Classes | Rows | Source |
|---|---|---|---|---|---:|---|
| `loan_approval.csv` | Loan Approval Prediction | **Classification** | Binary | `Loan_Status`: `Y`, `N` | 614 | Public mirror of the common Loan Prediction dataset |
| `Crop_recommendation.csv` | Crop Recommendation System | **Classification** | Multiclass | `label`: 15 crop classes | 1,697 | Hugging Face public crop dataset mirror |
| `heart_disease.csv` | Heart Disease Risk Score | **Classification** | Binary | `target`: `0`, `1` | 297 | UCI Heart Disease-derived public CSV mirror |
| `student_dropout.csv` | Student Dropout Prediction | **Classification** | Multiclass | `Target`: Dropout, Graduate, Enrolled | 4,424 | UCI Predict Students' Dropout and Academic Success-derived public CSV mirror |
| `Phishing_Email.csv` | AI Email Phishing Detector | **Classification (NLP)** | Binary | `Email Type`: `Safe Email`, `Phishing Email` | 18,650 | Hugging Face copy of the Kaggle Phishing Email dataset |

---

## 1. Loan Approval Prediction

**ML Task:** Classification  
**Classification Type:** Binary Classification  
**Target:** `Loan_Status`

Classes:
- `Y` = Approved
- `N` = Not Approved

Main fields include `Gender`, `Married`, `Dependents`, `Education`, `Self_Employed`, `ApplicantIncome`, `CoapplicantIncome`, `LoanAmount`, `Loan_Amount_Term`, `Credit_History`, and `Property_Area`.

**Student work:** cleaning, missing-value handling, categorical encoding, EDA, train/test split, at least two classifiers, evaluation, model selection, saved model, and UI integration.

Dataset file:
`loan_approval/loan_approval.csv`

---

## 2. Crop Recommendation System

**ML Task:** Classification  
**Classification Type:** Multiclass Classification  
**Target:** `label`

Inputs:
- `N`
- `P`
- `K`
- `temperature`
- `humidity`
- `ph`
- `rainfall`

This packaged dataset contains **15 crop classes** and **1,697 rows**.

**Student work:** EDA, feature analysis, train/test split, at least two multiclass classifiers, evaluation, model selection, saved model, and a UI where the user enters soil/environment values.

Dataset file:
`crop_recommendation/Crop_recommendation.csv`

---

## 3. Heart Disease Risk Score

**ML Task:** Classification  
**Classification Type:** Binary Classification  
**Target:** `target`

Classes:
- `0` = No heart-disease class
- `1` = Heart-disease class

The file includes common UCI-style variables such as age, sex, chest-pain type, resting blood pressure, cholesterol, fasting blood sugar, ECG-related features, maximum heart rate, exercise-induced angina, oldpeak, slope, ca, and thal.

**Student work:** data inspection, EDA, preprocessing, at least two classifiers, evaluation, model selection, saved model, and UI integration.

> Educational use only. The application must not be presented as a medical diagnosis tool.

Dataset file:
`heart_disease/heart_disease.csv`

---

## 4. Student Dropout Prediction

**ML Task:** Classification  
**Classification Type:** Multiclass Classification  
**Target:** `Target`

Classes in the packaged dataset:
- `Dropout`
- `Graduate`
- `Enrolled`

The dataset contains **4,424 students** and **36 input features**.

**Student work:** EDA, preprocessing, feature/target preparation, at least two classifiers, class evaluation, final model selection, saved model, and UI integration.

Dataset file:
`student_dropout/student_dropout.csv`

---

## 5. AI Email Phishing Detector

**ML Task:** Classification using NLP  
**Classification Type:** Binary Classification  
**Target:** `Email Type`

Classes:
- `Safe Email`
- `Phishing Email`

Input:
- `Email Text`

**Student work:** inspect/clean text, train/test split, TF-IDF or CountVectorizer, at least two classifiers such as Naive Bayes and Logistic Regression, evaluation, saved pipeline, and UI integration.

Dataset file:
`phishing_email/Phishing_Email.csv`

---

## Repository Structure

```text
BILE_ML_Datasets_Repo/
├── README.md
├── SOURCES.md
│
├── loan_approval/
│   └── loan_approval.csv
│
├── crop_recommendation/
│   └── Crop_recommendation.csv
├── heart_disease/
│   └── heart_disease.csv
│
├── student_dropout/
│   └── student_dropout.csv
└── phishing_email/
    └── Phishing_Email.csv
```

## Student Rule

Students should **not search for another dataset unless the instructor approves it**.  
Use the dataset already included in this repository so all groups start from the same source data.

