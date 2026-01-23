# End-to-End Breast Cancer Survival Classification

## Overview
This project builds an end-to-end machine learning pipeline to predict breast cancer patient survival (`Alive` vs `Dead`) using clinical and demographic features.  
The focus is on correct preprocessing, model comparison, and evaluation for imbalanced medical data.

---

## Dataset
- **Target**: `Status` (Alive = 0, Dead = 1)
- **Type**: Binary classification (imbalanced)
- **Features**:
  - Numerical: Age, Tumor Size, Regional Nodes Examined/Positive, Survival Months
  - Categorical: Race, Marital Status, Hormone Status
  - Ordinal: Tumor/Node Stages, Grade, Differentiation

---

## Approach
1. Data cleaning and column standardization  
2. Exploratory Data Analysis (EDA)  
3. Train–test split with stratification  
4. Preprocessing using `ColumnTransformer`:
   - StandardScaler (numerical)
   - OrdinalEncoder (ordinal features)
   - OneHotEncoder (categorical features)
5. Model training using unified pipelines

---

## Models
- k-Nearest Neighbors (with GridSearchCV)
- Logistic Regression
- Random Forest
- XGBoost

---

## Evaluation
Metrics used:
- Accuracy
- Precision
- Recall
- F1-score
- ROC-AUC

Additional analysis:
- Confusion matrices
- ROC curves

---

## Key Findings
- Tumor size and lymph node involvement are strong predictors.
- Higher clinical stages correlate with worse outcomes.
- Boosting models (XGBoost) perform best overall.
- `Survival Months` is highly predictive but introduces data leakage and should be handled carefully.

---

## Tech Stack
Python, Pandas, NumPy, Matplotlib, Seaborn, scikit-learn, XGBoost


