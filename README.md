# credit risk pd model

This project builds a machine learning model to predict the **Probability of Default (PD)** for retail banking customers. It also calculates the **Expected Loss (EL)** assuming a 90% Loss Given Default (i.e., 10% recovery rate).

---

## 📂 Dataset Overview

The dataset includes anonymized borrower-level features:

- Credit lines outstanding
- Loan amount outstanding
- Total debt outstanding
- Income
- Years employed
- FICO score
- Target variable: `default` (1 if borrower defaulted)

---

## 🚀 Project Workflow

### 1. Data Exploration
- Checked missing values, class balance, basic statistics.

### 2. Feature Selection
- Selected key borrower financial indicators.
- No categorical variables in this dataset.

### 3. Model Training
- Trained both:
  - Logistic Regression (scaled)
  - Random Forest (no scaling needed)
- Evaluated using ROC AUC score.

### 4. Feature Importance
- Random Forest feature importances plotted to understand key drivers.

### 5. Expected Loss Calculation
- Used the formula:
Expected Loss = PD × EAD × LGD
Where:
- **PD** = Probability of Default (from model)
- **EAD** = Exposure at Default (loan amount)
- **LGD** = Loss Given Default (fixed at 90%)
  ---

## Dependencies

-python
-pandas
-numpy
-scikit-learn
-matplotlib

---

