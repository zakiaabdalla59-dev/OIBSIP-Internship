# Task 1: Iris Flower Classification

## 📌 Overview
This project presents an end-to-end Machine Learning solution for the classic **Iris Flower Classification** task. Using sepal and petal measurements (length and width), machine learning models predict the exact species among *Iris-setosa*, *Iris-versicolor*, and *Iris-virginica*.

---

## 📂 Files Included
- `Iris_Classification.ipynb`: Clean, fully executed Jupyter Notebook with EDA charts, code, and benchmark evaluations.
- `README.md`: Project summary and findings.

---

## 🔬 Methodology & Workflow
1. **Data Source**: Scikit-Learn built-in dataset (`sklearn.datasets.load_iris()`).
2. **Exploratory Data Analysis (EDA)**:
   - Checked missing values (0 nulls found).
   - Inspected class balance (50 samples per species).
   - Plotted feature pairplots and boxplots per species.
   - Calculated correlation matrix.
3. **Data Preprocessing**:
   - 80/20 Train/Test Split with stratification (`random_state=42`).
   - Feature standardization using `StandardScaler`.
4. **Machine Learning Models Trained**:
   - Logistic Regression
   - Random Forest Classifier
   - Decision Tree Classifier
   - Support Vector Machine (SVC - RBF Kernel)
   - K-Nearest Neighbors (KNN - k=5)
5. **Model Evaluation Metrics**:
   - Accuracy, Macro Precision, Macro Recall, Macro F1-Score.
   - Confusion Matrix Heatmaps.
   - Classification Reports.
   - Random Forest Feature Importance Analysis.

---

## 📊 Benchmark Results

| Model | Accuracy | Precision | Recall | F1-Score |
|---|---|---|---|---|
| **Logistic Regression** | **100.0%** | **1.0000** | **1.0000** | **1.0000** |
| **Random Forest** | **100.0%** | **1.0000** | **1.0000** | **1.0000** |
| **Support Vector Machine** | **100.0%** | **1.0000** | **1.0000** | **1.0000** |
| **K-Nearest Neighbors** | **100.0%** | **1.0000** | **1.0000** | **1.0000** |
| **Decision Tree** | **96.67%** | **0.9697** | **0.9667** | **0.9665** |

---

## 🏆 Key Takeaways & Best Model
- **Iris-setosa** is linearly separable based on Petal dimensions alone.
- **Petal Length** (44.3%) and **Petal Width** (43.1%) contribute over **87%** of the total decision weight in Random Forest.
- **Winner**: **Logistic Regression / Random Forest Classifier** both achieved perfect 100% accuracy on the test set.

---
*Completed for Oasis Infobyte Data Science Internship (OIBSIP)*
