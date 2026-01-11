
# Customer Churn Prediction with Logistic Regression

This project focuses on predicting customer churn using demographic, service-related, and billing information.  
The goal is to estimate the probability that a customer will leave the telecom operator and to analyze the key factors influencing churn.

---

## 📌 Project Overview

Customer churn is a critical business problem in subscription-based industries.  
In this project, a **Logistic Regression model** is developed to predict whether a customer will churn based on their characteristics and service usage.

The project follows a complete **end-to-end machine learning workflow**, including:
- Data cleaning and preprocessing
- Feature engineering
- Model training and comparison
- Model selection and evaluation
- Churn probability prediction for new customers

---

## 📂 Dataset

- Source: Telecom customer churn dataset
- Target variable: `Churn` (0 = No, 1 = Yes)
- Features include:
  - **Demographic information** (gender, senior citizen, partner, dependents)
  - **Service usage** (internet service, streaming, security, support)
  - **Billing details** (contract type, payment method, monthly and total charges)

The dataset is located in the `data/` directory.

---

## 🛠 Data Preprocessing & Feature Engineering

The following steps were applied:

- Handling categorical variables using **One-Hot Encoding**
- Mapping categorical values to **readable Turkish labels** for interpretability
- Separating numerical and categorical features
- Splitting data into **training and test sets** with stratification
- Using a **pipeline structure** to avoid data leakage

---

## 🤖 Models Trained & Compared

The following machine learning models were trained and evaluated:

- Logistic Regression
- Random Forest
- Gradient Boosting

### Model Comparison Results:

| Model | Accuracy | F1 Score |
|------|---------|----------|
| Logistic Regression | **0.804** | **0.583** |
| Random Forest | 0.793 | 0.569 |
| Gradient Boosting | 0.797 | 0.574 |

Based on overall performance and interpretability, **Logistic Regression** was selected as the final model.

---

## 📊 Final Model Performance (Logistic Regression)

- **Accuracy:** 80.4%
- **F1 Score (Churn):** 0.58

### Classification Report Summary:
- The model performs very well in identifying **non-churn customers**
- Churn detection performance is moderate, making the model suitable as an **early warning system**

This balance makes the model useful for **decision support** rather than automated decision-making.

---

## 📈 Feature Importance & Interpretability

Feature importance was analyzed using:
- Logistic Regression coefficients
- Tree-based feature importances for comparison

Key insights include:
- Contract type and payment method have strong influence on churn
- Monthly charges and service usage significantly impact churn probability

All visualizations are available in the `images_and_plots/` directory.

---

## 🧪 New Customer Churn Prediction

The final model is capable of predicting churn probability for new customers.

