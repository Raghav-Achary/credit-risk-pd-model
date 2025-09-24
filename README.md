# Loan Default Prediction Model

This project is a prototype predictive model designed to estimate the **probability of default (PD)** for retail banking customers with outstanding personal loans. It also calculates the **expected loss (EL)** on a loan, assuming a recovery rate of 10%.

This model assists risk teams in assessing potential loan losses, helping inform capital reserves and lending decisions.

---

## 📊 Problem Statement

Retail banking has been experiencing higher-than-expected personal loan defaults. To proactively manage credit risk, we aim to:

- Predict the **likelihood of default** for each borrower.
- Estimate **expected loss** using:
  
 Expected Loss (EL)=Probability of Default (PD)×(1−Recovery Rate)×Loan Amount

---

## 🧮 Dataset

The dataset includes borrower-level data with the following features:

- `credit_lines_outstanding`
- `loan_amt_outstanding`
- `total_debt_outstanding`
- `income`
- `years_employed`
- `fico_score`
- `default` (target variable: 1 if defaulted, else 0)

Additional engineered features:

- `payment_to_income` = loan_amt_outstanding / income
- `debt_to_income` = total_debt_outstanding / income

---

## 🔧 Approach

- **Model**: Logistic Regression (using scikit-learn)
- **Target**: Binary classification (`default`: 0 or 1)
- **Feature Engineering**:
  - Created meaningful financial ratios to capture borrower stress.
- **Evaluation**:
  - ROC-AUC
  - Accuracy
  - Confusion matrix (optional)

---

## 🧪 Sample Output

The model produces:

- **Probability of default (PD)** for each borrower
- **Expected Loss (EL)** based on the formula

---

## 📦 Files in this Repository

| File | Description |
|------|-------------|
| `loan_default_model.py` | Main script to train and test the model |
| `loan_data_sample.csv` | Sample dataset (anonymized) |
| `expected_loss_function.py` | Function to calculate expected loss for a given borrower |
| `README.md` | This file |

---

## 🛠️ Tools & Libraries

- Python 3.8+
- `pandas`, `numpy`
- `scikit-learn`
- `matplotlib`, `seaborn` (for optional visualizations)

---


