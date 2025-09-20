<img width="1280" height="480" alt="image" src="https://github.com/user-attachments/assets/5440cb62-250b-462e-b0e5-bd98d054eca7" />



# 🚗 Ola Ensemble Learning  Project

## 📌 Introduction


**Ola Cabs**, officially ANI Technologies, is an Indian multinational ride-hailing company founded in 2010 by Bhavish Aggarwal and Ankit Bhati. It operates a vast mobility platform that connects users with various transport options like cabs, auto-rickshaws, and bike taxis through its mobile app. Ola is one of India's largest mobility platforms and serves over 250 cities in India, Australia, New Zealand, and the UK. In addition to ride-hailing, Ola offers other services like food delivery and a financial services arm, providing a comprehensive range of mobility solutions. 


## Context & Business Problem 
Driver retention is a critical challenge for ride-hailing platforms like Ola. High churn rates among drivers lead to increased recruitment costs, loss of trained manpower, and disruptions in service quality. Drivers can easily switch platforms based on fluctuating incentives, making it imperative for Ola to proactively identify at-risk drivers and take preventive action.

Ola’s Driver Operations and Analytics teams need to accurately predict which drivers are likely to leave the platform, enabling targeted interventions to improve retention. Currently, driver attrition not only increases operational costs due to frequent acquisition efforts but also negatively impacts organizational morale and customer satisfaction.

## 🧠 Project Overview

To build a predictive model that can classify whether a driver is likely to leave or stay with Ola in a given month, using historical and demographic data.

---

## 📊Scope of Data:

The dataset includes monthly information for a segment of drivers across 2019 and 2020. Key features include:

**Demographics**: City, age, gender, etc.

**Tenure Details**: Joining date, last working date, total tenure

**Performance Metrics**: Quarterly ratings, monthly income, business acquired, driver grade


## Deliverables:

A **binary classification model** that predicts driver attrition (Leave = 1, Stay = 0)

**Feature importance analysis** to identify key drivers of attrition

**Actionable insights** for the Driver Retention Team

A **dashboard** or reporting mechanism (optional) for real-time monitoring


## 🐱‍🏍Success Metric:
The model will be evaluated using accuracy, precision, recall, F1-score, and ROC-AUC, with particular emphasis on minimizing false negatives (i.e., drivers likely to leave but not flagged).

---

## ⚙️ Data Preparation

**Record Consolidation**: Merged multiple records per driver into a single driver-level row.

**Feature Engineering**:

Created flag columns such as Quarterly_Raise and Income_Raise.

Derived a binary Churn target from Last_Working_Day (1 = left, 0 = stayed).

**Outlier Handling**: Avoided aggressive removal to prevent major data loss and feature distortion.


---

## 🤖 Modeling

| Model             | Train Accuracy | Test Accuracy | Key Note                                         |
| ----------------- | -------------: | ------------: | ------------------------------------------------ |
| **Random Forest** |           1.00 |         0.916 | High accuracy; potential overfitting.            |
| **XGBoost**       |           1.00 |     **0.918** | **Best performer** with strong recall/precision. |
| **LightGBM**      |           1.00 |         0.890 | Good but slightly weaker generalization.         |
| **CatBoost**      |          0.986 |         0.899 | Balanced fit; good generalization.               |

- ROC–AUC: 0.95

- F1 Score: Improved significantly after addressing class imbalance and threshold tuning.

## 🔍 Exploratory Insights

**Income & Business Value**: Moderate negative correlation with churn—higher values reduce churn probability.

**Joining Designation**: Levels 1–3 show highest churn; 4–5 present moderate retention risk.

**Income Raise**: No churn observed among drivers receiving raises, highlighting it as a strong retention lever.

**Gender Imbalance**: Predominantly male driver base.


## Best Model & Key Predictors

**XGBoost** provided the best discrimination between churned and retained drivers.
Important predictors include:

- Income Raise

- Grade & Total Business Value

- Joining Designation

- Quarterly Rating

## Recommendations

- **Retention Incentives**: Provide income raises or performance bonuses for at-risk drivers.

- **Early Tenure Engagement**: Loyalty rewards for drivers in their first few years.

- **Focus on High-Risk Designations**: Target designations 1–3 with coaching and benefits.

- **Gender Balance Programs**: Recruit and support more female drivers.

---

## 🛠️ Tech Stack

- **Python**: pandas, NumPy, scikit-learn, XGBoost, LightGBM, CatBoost, matplotlib, seaborn

- **EDA & Visualization**: Jupyter Notebook, Matplotlib, Seaborn

- **Version Control**: Git & GitHub

## 📈 Business Impact

Accurately predicting driver churn enables proactive retention, reduces recruitment costs, and ensures better customer service reliability.

---
## Colab Notebook
- You can access the full Python analysis on Google Colab using the following link: [View the notebook](https://colab.research.google.com/drive/1XypbEknLQUbftTx9AqG_8QaCwNIb4Qlj#scrollTo=KgbZk4DlkF0I)

## PDF Report

A detailed analysis report is available in the following PDF file: [View Report](ola_retention_project.pdf
).

## 📬Contact
For questions or collaboration, please reach out via
[SYED ZAHEER ABBAS] - [SYEDZAHEER.C@GMAIL.COM]


