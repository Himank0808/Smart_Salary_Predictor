# 💼 SmartSalaryPredictor

### 📊 Predict Salaries from Real-World Survey Data using Machine Learning

SmartSalaryPredictor is an end-to-end machine learning project that predicts developer salaries using real-world survey data.  
It emphasizes **data cleaning, preprocessing, feature engineering**, and **model comparison** to identify the most accurate regression model.

---

## 🗂️ Dataset

The full survey dataset is hosted externally due to file size constraints.  
You can download it here:  
[Survey CSV (Google Drive)](https://drive.google.com/file/d/1CY9ekyUQQwjDjDUTZaAxDYXtog8q_0eH/view?usp=sharing)

---

## 🧠 Objectives
- Clean messy survey data (missing values, duplicates, outliers).  
- Encode categorical variables and manage high-cardinality fields.  
- Engineer meaningful features (skills count, binary flags for high-value tech, etc.).  
- Train and compare multiple regression models to predict salaries.  
- Evaluate model performance using R², MAE, RMSE.

---

## 🧹 Data Cleaning & Preprocessing
- Removed columns with more than 50 % missing values.  
- Filtered salaries to the range \$10,000 – \$500,000 to reduce extreme outliers.  
- Created new numerical features like `Num_Languages`, `Total_Skills`, and binary flags for technologies.  
- Encoded ordinal features (Age, Education) and one-hot encoded categorical columns.  
- Ensured only numerical / boolean features entered modeling.

---

## ⚙️ Machine Learning Models Used
| Model                     | Type              | R² Score |
|---------------------------|-------------------|----------|
| Linear Regression         | Linear            | 0.565    |
| Ridge Regression          | Linear (regularized) | 0.565 |
| Lasso Regression          | Linear (regularized) | 0.565 |
| Random Forest Regressor   | Ensemble Trees     | 0.590   |
| **XGBoost Regressor**     | Gradient Boosting  | **0.608** |

> ✅ *XGBoost achieved the best score (R² ~ 0.61).*

---

## 🧮 Tech Stack
- **Language:** Python  
- **Libraries:** pandas, numpy, scikit-learn, xgboost, matplotlib, seaborn  
- **Environment:** Jupyter Notebook 

---

## 📈 Results & Insights
- Achieved R² ≈ 0.61 on cleaned survey data — a strong result given the noisy, real-world nature of the dataset.  
- Feature importance analysis reveals that tech-skills flags, experience, and country indicators significantly influence salary.  
- Visualizations include predicted vs actual salary plots, residual analysis, and coefficient impact charts.

