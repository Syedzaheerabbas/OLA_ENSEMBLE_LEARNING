!<img width="275" height="183" alt="image" src="https://github.com/user-attachments/assets/02e20d15-c383-4653-b0ae-aa9e0f7edb5d" />


# 💼 LoanTap Credit Risk Modeling Project

## 📌 Introduction

**LoanTap** is a digital lending platform that provides flexible loan products to salaried professionals. With the rise of fintech-driven credit solutions, underwriting accuracy becomes crucial to minimize default risk while ensuring timely loan disbursement. This project builds a predictive model to assess credit risk and assist LoanTap in making data-driven lending decisions.

---

## 🧠 Project Overview

The objective of this project is to develop a machine learning model that predicts whether a borrower is likely to **repay the loan (Fully Paid)** or **default (Charged Off)**. The model supports LoanTap’s credit risk team in automating and improving the efficiency of their underwriting process.

---

## 📊 Dataset

The dataset includes borrower-level and loan-level features such as:

- **Loan Amount**
- **Annual Income**
- **Interest Rate**
- **EMI**
- **Credit Score**
- **Loan Tenure**
- **Purpose of Loan**
- **Employment Details**
- **Repayment Status (Target Variable)**

**Target Variable:**
- `Fully Paid` → 1  
- `Charged Off` → 0  

The dataset was imbalanced, with a majority of loans marked as “Fully Paid.”

---

## 🔬 Methodology

### 1. Exploratory Data Analysis (EDA)
- Identified skewness and outliers in numeric variables.
- Detected important patterns between features and repayment behavior.
- Handled missing values and ensured clean formatting.

### 2. Data Preprocessing
- Encoded categorical variables.
- Normalized numerical features.
- Addressed data imbalance using:
  - **SMOTE (Synthetic Minority Over-sampling Technique)**
  - **Class Weighting**

### 3. Model Building
Built multiple Logistic Regression models:
- Baseline Logistic Regression
- Logistic Regression with Class Weights
- Logistic Regression with SMOTE
- SMOTE + Class Weights
- Threshold-tuned model for best F1-score
- Reglurazed model

### 4. Model Evaluation
- Evaluated using **Confusion Matrix**, **F1-Score**, **Precision**, **Recall**, **ROC-AUC**, and **PR Curve**.
- Tuned the classification threshold using F1 optimization to improve performance on minority class.

---

## 📈 Results and Insights

- **Best Model**: Logistic Regression with SMOTE + Class Weighting + Threshold Tuning
- **Key Features Impacting Default Risk**:
  - **Zip Code**(Geographical presence)
  - High **EMI** relative to income
  - Low **Credit Score**
  - High **Interest Rate**
  - Purpose categories like “Debt Consolidation” showed higher risk
- **F1-score improved** significantly after addressing imbalance and threshold tuning.

---

## ✅ Recommendations

- **Prioritize 36-Month Loan Terms**: Given the higher default rates on 60-month loans, encourage 36-month loans by offering slightly better terms (e.g., lower interest or processing fees) to reduce long-term risk exposure.
- Implement regional risk scoring by incorporating pincode-level default trends. High-risk areas could be subjected to stricter eligibility or additional checks.
Limit Loan Size in Risk Bands
- Incorporate external credit bureau data for enhanced accuracy.
- Regularly retrain the model to account for shifts in applicant behavior and economic conditions.

---

## 🔭 Future Improvements

- Experiment with advanced models like **XGBoost**, **Random Forest**, and **LightGBM**.
- Deploy the model using **Flask** or **Streamlit** to create an interactive loan approval dashboard.
- Integrate explainability tools like **SHAP** or **LIME** for transparent decision-making.
- Monitor model drift and performance using a feedback loop from live loan outcomes.

---

## Colab Notebook
- You can access the full Python analysis on Google Colab using the following link: [View the notebook](https://colab.research.google.com/drive/11MP_rUCVyKrtoH_NQa3tq6GFzMe9Xq8T#scrollTo=WTCNvu7F-D68)

## PDF Report

A detailed analysis report is available in the following PDF file: [View Report](Loan_Tap.pdf).

## Contact

[SYED ZAHEER ABBAS] - [SYEDZAHEER.C@GMAIL.COM]


