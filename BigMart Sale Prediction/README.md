
# 🧠 Featured Project: BigMart Sales Prediction  
### 📁 *Case_Study_BigMart_Sales_Prediction*

This project is an end-to-end machine learning solution designed to predict **retail item sales** across multiple BigMart outlets.  
It follows a complete DS pipeline: data cleaning → feature engineering → modeling → evaluation.

---

## 📌 **Project Summary**

Retail companies like BigMart collect detailed transactional data. The challenge is to accurately **predict future product sales**, enabling:

- better inventory planning  
- optimized supply chain  
- improved marketing decisions  
- reduction of stockouts and overstock  

This project uses historical sales data to build a **predictive machine learning model** capable of estimating item-level sales across different store types.

---

## 📂 **Dataset Overview**

The dataset (from an open Kaggle challenge) contains:

- **12,852 rows** representing items sold
- **12 features**, including:
  - Item_Identifier  
  - Item_Weight  
  - Item_Fat_Content  
  - Item_Type  
  - Item_MRP  
  - Outlet_Identifier  
  - Outlet_Type  
  - Outlet_Size  
  - Item_Visibility  
  - Outlet_Location_Type  

Target variable:

- **Item_Outlet_Sales**

---

## 🔧 **Technical Workflow**

### **1. Data Cleaning**
✔ Handled missing values (notably in `Item_Weight` and `Outlet_Size`)  
✔ Corrected inconsistent labels (e.g., “LF”, “Low Fat”, “low fat”)  
✔ Replaced zero visibility values  
✔ Converted categorical variables  

### **2. Exploratory Data Analysis (EDA)**
✔ Distribution analysis (MRP, visibility, weight)  
✔ Sales correlation heatmap  
✔ Store-level performance analysis  
✔ Visualization of key drivers of sales  

### **3. Feature Engineering**
✔ Created new engineered features such as:
- **Price_Tier**, **Years_Operating**, **Item_Category**, etc.  
✔ One-hot encoding for categorical variables  
✔ Normalization where needed  

### **4. Modeling**
Tested multiple algorithms:

- Linear Regression  
- Lasso / Ridge  
- Random Forest Regressor  
- XGBoost  
- Gradient Boosting  

**Random Forest & XGBoost** provided the strongest predictive performance.

### **5. Model Evaluation**
Metrics used:

- R² Score  
- RMSE  
- Cross-validation  

The final model achieved:

**High predictive accuracy**, with robust generalization across outlets.

---

## 📈 **Results**

- Successfully predicted item-level sales with strong accuracy  
- Identified major factors influencing sales:
  - Item MRP  
  - Outlet Type  
  - Item Type  
  - Visibility  
  - Store age  

- Delivered a ready-to-use ML pipeline extendable to real-world retail planning.

---

## 🛠 **Technologies Used**

- Python  
- Pandas, NumPy, Scikit-learn  
- Matplotlib, Seaborn  
- Jupyter Notebook  
- XGBoost  
- Feature engineering & ML pipeline design  

---
