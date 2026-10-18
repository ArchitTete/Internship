# Internship

# Machine Learning Projects: Customer Churn Prediction & Credit Risk Modeling

This repository contains two machine learning projects focused on solving real-world business problems using data analysis, predictive modeling, and model evaluation techniques.

## Table of Contents

1. [Customer Churn Prediction](#1-customer-churn-prediction)
2. [Credit Risk Modeling](#2-credit-risk-modeling)
3. [Technologies Used](#technologies-used)
4. [Project Structure](#project-structure)
5. [Installation and Setup](#installation-and-setup)
6. [Evaluation Metrics](#evaluation-and-results)
7. [Key Learning Outcomes](#key-learning-outcomes)
8. [Limitations and Responsible Use](#limitations-and-responsible-use)

---

# 1. Customer Churn Prediction

## Objective

Predict which customers are likely to stop using a company's services. The project analyzes customer data to identify churn patterns and helps businesses understand factors associated with customer attrition.

## Dataset

Use a telecom, banking, or SaaS customer churn dataset.

**Recommended dataset:** [IBM Telco Customer Churn — Kaggle](https://www.kaggle.com/datasets/blastchar/telco-customer-churn)

The dataset includes customer demographics, services subscribed to, contract details, tenure, monthly charges, total charges, and churn status.

## Project Workflow

1. **Data Collection:** Load the customer churn dataset.
2. **Data Cleaning:** Handle missing values, duplicates, and inconsistent data types.
3. **Exploratory Data Analysis (EDA):** Analyze churn distribution and relationships between churn, tenure, contract type, payment method, and charges.
4. **Feature Engineering:** Encode categorical features and scale numerical variables where necessary.
5. **Model Training:** Train and compare Logistic Regression, Random Forest, and XGBoost classifiers.
6. **Model Evaluation:** Measure accuracy, recall, and ROC-AUC.
7. **Insights:** Identify customer characteristics associated with higher churn rates.

## Machine Learning Models

- Logistic Regression
- Random Forest Classifier
- XGBoost Classifier

## Evaluation Metrics

- **Accuracy:** Overall proportion of correct predictions.
- **Recall:** Proportion of actual churners correctly identified.
- **ROC-AUC:** Measures the model's ability to distinguish churners from non-churners across classification thresholds.

## Expected Outcome

A classification model that estimates customer churn risk and helps businesses identify customers who may benefit from retention strategies.

---

# 2. Credit Risk Modeling

## Objective

Assess the credit risk of loan applicants by classifying applicants into good-risk and bad-risk categories using historical credit data.

The project uses machine learning to identify patterns associated with credit risk and demonstrates how model predictions can be explained.

## Dataset

**Selected dataset:** [UCI Statlog German Credit Data](https://archive.ics.uci.edu/dataset/144/statlog+german+credit+data)

The dataset contains 1,000 applicant records with 20 input features.

Features include credit history, loan duration, credit amount, savings, employment status, and other financial or demographic indicators.

The target identifies applicants as good or bad credit risk.

## Project Workflow

1. **Data Collection:** Retrieve the German Credit dataset from the UCI Machine Learning Repository.
2. **Data Cleaning:** Inspect missing values, duplicates, feature types, and data quality.
3. **Exploratory Data Analysis (EDA):** Examine class distribution and relationships between applicant attributes and credit-risk labels.
4. **Data Preprocessing:** Encode categorical features, scale numerical variables where appropriate, and split the data into training and testing sets.
5. **Class Imbalance Handling:** Apply SMOTE to the training data to balance the classes.
6. **Model Training:** Train and compare Logistic Regression, Decision Tree, and Random Forest classifiers.
7. **Model Evaluation:** Evaluate models using accuracy, precision, recall, F1-score, and ROC-AUC.
8. **Model Explainability:** Use SHAP to understand the features influencing model predictions.
9. **Results Analysis:** Compare models and discuss their strengths, limitations, and potential sources of bias.

## Machine Learning Models

- Logistic Regression
- Decision Tree Classifier
- Random Forest Classifier

## Handling Class Imbalance

SMOTE (Synthetic Minority Over-sampling Technique) generates synthetic examples of the minority class to help the model learn from both classes.

**Important:** Apply SMOTE only to the training data. Keep the test data unchanged to obtain a meaningful evaluation.

## Model Explainability with SHAP

SHAP (SHapley Additive exPlanations) helps interpret machine learning predictions.

It can be used to:

- Identify features with the greatest influence on predictions.
- Understand whether features push a prediction toward good or bad credit risk.
- Explain individual applicant predictions.
- Improve transparency when discussing model behavior.

## Evaluation Metrics

- **Accuracy:** Overall classification correctness.
- **Precision:** Proportion of applicants predicted as bad risk who are actually bad risk.
- **Recall:** Proportion of actual bad-risk applicants identified by the model.
- **F1-score:** Harmonic mean of precision and recall.
- **ROC-AUC:** Measures the model's ability to distinguish between the two risk classes.

## Expected Outcome

A credit-risk classification pipeline that compares multiple models, handles class imbalance, evaluates predictive performance, and explains model predictions using SHAP.

The results are intended for educational analysis and do not constitute a validated lending decision system.

---

# Technologies Used

| Category | Technologies |
|---|---|
| Programming Language | Python |
| Data Analysis | Pandas, NumPy |
| Data Visualization | Matplotlib, Seaborn |
| Machine Learning | Scikit-learn |
| Advanced Classification | XGBoost |
| Imbalanced Data | imbalanced-learn, SMOTE |
| Model Explainability | SHAP |
| Development Environment | Google Colab, Jupyter Notebook |
| Dataset Sources | Kaggle, UCI Machine Learning Repository |

---

# Project Structure

```text
Machine-Learning-Projects/
│
├── Customer-Churn-Prediction/
│   ├── data/
│   ├── notebooks/
│   │   └── customer_churn_prediction.ipynb
│   ├── results/
│   └── README.md
│
├── Credit-Risk-Modeling/
│   ├── data/
│   ├── notebooks/
│   │   └── credit_risk_modeling.ipynb
│   ├── results/
│   └── README.md
│
├── requirements.txt
└── README.md
```

This structure can be adjusted to match the actual files in the repository.

---

# Installation and Setup

## 1. Clone the Repository

```bash
git clone <YOUR_REPOSITORY_URL>
cd Machine-Learning-Projects
```

Replace `<YOUR_REPOSITORY_URL>` with your GitHub repository URL.

## 2. Install Dependencies

```bash
pip install pandas numpy matplotlib seaborn scikit-learn xgboost imbalanced-learn shap ucimlrepo
```

## 3. Run the Notebooks

Open the respective project notebook in Google Colab or Jupyter Notebook.

- Run the Customer Churn Prediction notebook to analyze churn patterns and train classification models.
- Run the Credit Risk Modeling notebook to preprocess credit data, apply SMOTE, train classifiers, and explain predictions using SHAP.

Follow the notebook cells in order.

---

# Evaluation and Results

Both projects compare machine learning models using metrics appropriate to their classification tasks.

| Project | Primary Focus | Evaluation Metrics |
|---|---|---|
| Customer Churn Prediction | Identifying customers likely to leave | Accuracy, Recall, ROC-AUC |
| Credit Risk Modeling | Identifying applicants associated with higher credit risk | Accuracy, Precision, Recall, F1-score, ROC-AUC |

Actual performance values should be added after running the notebooks. Model performance depends on data quality, preprocessing, feature selection, and model parameters.

---

# Key Learning Outcomes

By completing these projects, you will gain practical experience in:

- Data cleaning and exploratory data analysis.
- Feature engineering and categorical encoding.
- Training and comparing classification algorithms.
- Handling class imbalance using SMOTE.
- Evaluating classification models using multiple metrics.
- Interpreting predictions with SHAP.
- Identifying patterns in customer behavior and credit risk.
- Communicating analytical findings and model limitations.

---

# Limitations and Responsible Use

- Predictive performance on historical data may not generalize to future cases.
- Churn predictions indicate risk, not certainty that a customer will leave.
- Credit-risk predictions should not be used as the sole basis for real lending decisions.
- Financial and demographic attributes may introduce fairness concerns.
- Both projects require appropriate validation, monitoring, and careful interpretation before practical deployment.

---

## Author

Archit Tete

Machine Learning | Data Science | Predictive Analytics
