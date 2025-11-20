# Loan Default Prediction — Machine Learning Project  
**Predicting borrower default risk using machine learning**

This project focuses on building a predictive model to identify whether a loan applicant is likely to **default**. Financial institutions rely heavily on credit scoring models to reduce lending risk, optimize approval decisions, and improve portfolio performance.  
This is a complete machine learning pipeline including EDA, preprocessing, feature engineering, modeling, and evaluation.

---

## Project Objective

The primary goal is to build a model that:

- Accurately predicts if a borrower will default  
- Identifies the strongest risk signals  
- Helps financial institutions reduce credit losses  
- Improves decision-making for approvals, interest rates, and borrower segmentation  

This project simulates a real-world credit risk workflow used in banking and fintech.

---

## Dataset Overview

The dataset includes features related to:

### **Borrower Demographics**
- Age  
- Income  
- Employment type  
- Education level  
- Marital status  

### **Loan Information**
- Loan amount  
- Loan term  
- Interest rate  
- Credit history  
- Existing accounts  

### **Behavior & Risk Indicators**
- Debt-to-Income ratio (DTI)  
- Number of previous defaults  
- Purpose of loan  
- Delinquency history  

### **Target Variable**
- **Default** (1 = borrower defaulted, 0 = fully repaid)

---

## Exploratory Data Analysis (EDA)

Key findings from EDA:

### ✔ High DTI strongly correlates with default  
Borrowers with high debt ratios show higher risk.

### ✔ Lack of credit history increases default probability  
New borrowers are riskier than experienced borrowers.

### ✔ Low income + high loan amount = high default risk  
Income-to-loan ratio is a critical indicator.

### ✔ Applicants with previous delinquencies default significantly more  
Past behavior predicts future behavior.

Visualizations created:

- Correlation heatmaps  
- Distribution plots  
- Boxplots of income, DTI, loan amount  
- Default rate by loan purpose, education, and employment status  

---

## Data Preprocessing

Steps completed:

- Missing value imputation  
- Outlier detection and handling  
- Encoding categorical variables (Label/One-hot encoding)  
- Standardization of numerical features  
- Feature selection and multicollinearity analysis  
- Class imbalance handling with **SMOTE** / undersampling techniques (if used)

---

## Machine Learning Models

The following models were tested and compared:

- Logistic Regression  
- Random Forest Classifier  
- Gradient Boosting  
- XGBoost  
- Support Vector Machine  
- KNN  

### **Evaluation Metrics:**
Because default prediction is a high-risk domain, the focus is on:

- **Recall** (avoiding false negatives — risky borrowers predicted as safe)  
- **Precision**  
- **ROC-AUC score**  
- **Confusion Matrix**  
- **F1-score**  

### Final Model  
Based on your notebook, **XGBoost / Random Forest (depending on scores)** performed the best with:

- Strong recall  
- High AUC score  
- Stable performance with cross-validation  
- Good handling of nonlinear relationships and feature importance  

---

## Key Insights

- Debt-to-Income ratio (DTI), loan amount, and credit history are the most influential factors.  
- Education level and employment stability significantly affect creditworthiness.  
- Loan purpose categories (e.g., personal, small business, debt consolidation) show sharply different default patterns.  
- Tree-based models outperform linear models due to complex interactions between financial variables.

---

## Technologies Used

- Python  
- Pandas, NumPy  
- Scikit-learn  
- XGBoost  
- Matplotlib, Seaborn  
- Jupyter Notebook  
