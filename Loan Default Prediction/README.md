# 🧑‍💼 Employee Attrition Prediction — Machine Learning Project  
**Predicting which employees are at risk of leaving the company**

This project builds a machine learning model to predict **employee attrition**, allowing organizations to identify at-risk employees and take proactive HR decisions. It follows a complete data science lifecycle: EDA, data cleaning, feature engineering, modeling, and evaluation.

---

## 📌 Project Overview

Employee turnover is a costly challenge for organizations.  
Using HR analytics, machine learning can help:

- Identify employees at risk of leaving  
- Understand what factors drive attrition  
- Support HR interventions and retention strategies  
- Reduce recruitment and onboarding costs  

This project uses IBM’s open-source HR Attrition dataset to build a predictive model.

---

## 📂 Dataset Description

Key features include:

### **Employee Demographics**
- Age  
- Gender  
- Education  
- Marital Status  

### **Job-Related Features**
- Job Role  
- Years at Company  
- Years in Current Role  
- Job Satisfaction  
- Relationship Satisfaction  
- Environment Satisfaction  
- Performance Rating  

### **Work Conditions**
- Work-Life Balance  
- Overtime  
- Distance From Home  
- Monthly Income  
- Job Level  
- Hourly / Monthly / Daily Rate  

### **Target Variable**
- **Attrition** (Yes/No)

---

## 🔍 Exploratory Data Analysis (EDA)

Key EDA findings include:

### ✔ Overtime is the strongest indicator of attrition  
Employees working overtime show a significantly higher probability of leaving.

### ✔ Younger employees are more likely to leave  
Attrition rates decrease with age.

### ✔ Low satisfaction metrics (Job, Environment, Relationship)  
These strongly correlate with attrition.

### ✔ Low pay + long commute increases attrition  
Income combined with distance-from-home impacts retention.

Visualizations produced:

- Histograms & boxplots  
- Correlation heatmap  
- Attrition distribution across roles  
- Satisfaction vs. attrition analysis  
- Feature importance visualization  

---

## 🔧 Data Preprocessing

Steps performed in the notebook:

- Encoding categorical variables  
- Handling missing values  
- Standardizing numerical features  
- Converting satisfaction scores to numerical values  
- Removing irrelevant columns (EmployeeNumber, EmployeeCount, etc.)  

---

## 🤖 Machine Learning Models

The following models were tested:

| Model | Accuracy | Notes |
|-------|----------|--------|
| Logistic Regression | Good baseline | Interpretable |
| Random Forest | Strong performance | Good feature importance |
| Gradient Boosting | High accuracy | Handles categorical data well |
| XGBoost | Best overall | High precision & recall |

### **Final Model Performance**
- High accuracy on test data  
- Strong recall for "Yes" (avoiding false negatives is crucial)  
- Stable cross-validation score  

---

## 🏆 Key Insights

- **Overtime**, **Job Role**, **Monthly Income**, **Years at Company**, and **Environment Satisfaction** are the most important features.
- A reduction in overtime and improvement in work-life balance can significantly reduce attrition.
- HR policy changes targeting low-satisfaction groups can help retention.

---

## 🛠 Technologies Used

- Python  
- Pandas, NumPy  
- Scikit-learn  
- XGBoost  
- Matplotlib & Seaborn  
- Jupyter Notebook  
