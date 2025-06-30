## 🧠 Predicting Lead Conversion for an EdTech Startup with Decision Trees and Random Forest

### 📌 Project Overview

This project aims to identify potential customer leads likely to convert into paid users for ExtraaLearn, an emerging EdTech startup. Using classification models like Decision Trees and Random Forests, this end-to-end machine learning pipeline demonstrates how data-driven strategies can support efficient resource allocation in marketing and sales.

---

### 🎯 Objective

- Predict whether a lead will convert into a paid customer.
- Identify key features that influence conversion.
- Provide business insights to improve lead nurturing strategies.

---

### 📂 Dataset Description

The dataset contains 4,612 entries with 15 features, including:

- Demographics (`age`, `current_occupation`)
- Interaction details (`first_interaction`, `time_spent_on_website`, `profile_completed`, `last_activity`)
- Marketing channels (`digital_media`, `referral`, etc.)
- Target variable: `status` (1 = converted, 0 = not converted)

---

### 🔍 Exploratory Data Analysis (EDA)

- No missing or duplicate values
- Most users are professionals; \~30% leads converted
- High profile completion and longer website interaction correlate with higher conversion
- Age group 25–60 (especially unemployed/professionals) shows higher interest

---

### 🧪 Models Built & Evaluated

| Model                                  | Accuracy | Recall (Converted) | Notes                                         |
| -------------------------------------- | -------- | ------------------ | --------------------------------------------- |
| Decision Tree (Default)                | 81%      | 69%                | Overfitting observed                          |
| Decision Tree (Tuned)                  | 80%      | 86%                | Better generalization                         |
| Random Forest (Default)                | 85%      | 69%                | Best accuracy but slight overfitting          |
| Random Forest (Tuned via GridSearchCV) | 83%      | 85%                | Balanced performance with good generalization |

> **Evaluation Metric:** Focused on maximizing **recall for converted leads** to reduce false negatives (i.e., missing potential customers).

---

### 🔧 Techniques Used

- Data preprocessing: Encoding, scaling
- Univariate & Bivariate EDA with `seaborn` and `matplotlib`
- Model tuning with `GridSearchCV`
- Metrics: Accuracy, Precision, Recall, F1-score, Confusion Matrix
- Feature Importance Visualization

---

### 🔑 Key Insights

- Top features influencing conversion:
  - `time_spent_on_website`
  - `first_interaction` (Website preferred over Mobile App)
  - `profile_completed`
  - `age`
- Leads with higher engagement and completed profiles are significantly more likely to convert.

---

### 📈 Business Recommendations

- **Improve Website Experience**: Make it intuitive and informative to boost engagement.
- **Assist Profile Completion**: Auto-fill with resume parsing, simplify forms.
- **Optimize First Contact**: Ensure fast, helpful responses to website inquiries.
- **Age-specific Campaigns**: Tailor marketing based on high-conversion age segments (35–60).

---

### 📁 Folder Structure

```
├── ExtraaLearn.csv
├── classification_model.ipynb
├── README.md
```




