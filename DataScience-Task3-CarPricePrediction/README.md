# Task 3: Car Price Prediction with Machine Learning

## 📌 Overview
Predicting the selling price of used cars is a classic supervised regression task in Machine Learning. This project builds an automated valuation pipeline using vehicle attributes including original showroom price, vehicle age, total distance driven, fuel type, transmission system, and seller status.

---

## 📂 Files Included
- `Car_Price_Prediction.ipynb`: Fully executed Jupyter Notebook featuring data preprocessing, feature engineering, exploratory data plots, regression model training, metric evaluations, and feature importance charts.
- `car_data.csv`: Used car price dataset (CarDekho schema).
- `README.md`: Project summary, model metrics, and key valuation drivers.

---

## 🔬 Methodology & Pipeline
1. **Data Preprocessing & Cleaning**:
   - Identified and removed 5 duplicate rows.
   - Handled missing values (0 nulls found).
   - **Feature Engineering**: Engineered `Car_Age` ($2026 - \text{Year}$) and dropped redundant high-cardinality metadata (`Car_Name`, `Year`).
2. **Categorical Encoding**:
   - One-Hot Encoding applied to `Fuel_Type`, `Seller_Type`, and `Transmission` (`drop_first=True`).
3. **Model Training & Evaluation**:
   - 80/20 Train/Test Split (`random_state=42`).
   - Standardized features using `StandardScaler`.
   - Trained 5 regressors: Linear Regression, Lasso, Ridge, Random Forest Regressor, and Gradient Boosting Regressor.
   - Metrics calculated: Mean Absolute Error (MAE), Root Mean Squared Error (RMSE), and $R^2$ Score.

---

## 📊 Benchmark Model Performance

| Regressor Model | MAE (Lakhs) | RMSE (Lakhs) | $R^2$ Score |
|---|---|---|---|
| **Random Forest Regressor** | **0.5421** | **0.9104** | **0.9325** |
| **Gradient Boosting Regressor** | **0.5891** | **0.9652** | **0.9241** |
| **Ridge Regression** | **1.1402** | **1.7115** | **0.7618** |
| **Linear Regression** | **1.1458** | **1.7230** | **0.7586** |
| **Lasso Regression** | **1.1824** | **1.7845** | **0.7412** |

---

## 🔑 Feature Importance Breakdown
From the **Random Forest Regressor** importance analysis:
- **`Present_Price` (Showroom Original Price):** Contributes **> 72%** of total predictive weight.
- **`Car_Age` (Vehicle Age in Years):** Contributes **~16%** of predictive weight.
- **`Kms_Driven` (Total Mileage):** Contributes **~7%** of predictive weight.

---
*Completed for Oasis Infobyte Data Science Internship (OIBSIP)*
