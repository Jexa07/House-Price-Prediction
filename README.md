# 🏠 House Price Prediction – Advanced Regression Techniques

Welcome to my implementation of the **House Prices - Advanced Regression Techniques**. This project leverages data preprocessing, feature engineering, and advanced machine learning techniques to accurately predict housing prices.


## 🚀 Project Overview

This notebook solves a supervised regression problem using the **Ames Housing Dataset**, which contains 79 explanatory variables describing (almost) every aspect of residential homes in Ames, Iowa.

The goal is to predict the **`SalePrice`** of each house in the test set.

---

## 📦 Dataset Details

- `train.csv` – Training dataset with features and `SalePrice` (target)
- `test.csv` – Test dataset without `SalePrice`
- `data_description.txt` – Full metadata for all 79 variables
- `sample_submission.csv` – Format for final Kaggle submission

---

## 🔧 Workflow Summary

### ✅ 1. **Data Loading**
- Loaded `train.csv` and `test.csv` using pandas

### ✅ 2. **Preprocessing**
- Combined train and test for unified cleaning
- Imputed missing values:
  - Mode for categorical
  - Median for numerical

### ✅ 3. **Label Encoding**
- Applied `LabelEncoder` to all object-type columns

### ✅ 4. **Feature Engineering**
Created new features that improved predictive power:
- `TotalSF` = Total livable square footage
- `TotalBath` = Combined bathrooms (full + half)
- `Age` = Years since built
- `RemodAge` = Years since last remodel
- `HasGarage`, `HasPool` = Binary flags

### ✅ 5. **Modeling**
- Used **XGBoost Regressor** (`XGBRegressor`)
- Applied log-transformation to the target (`SalePrice`) for normalization
- Evaluated with **cross-validation RMSE**

### ✅ 6. **Submission**
- Generated final predictions and saved to `submission.csv`

---

## 📈 Model Performance

- **Model Used**: XGBoost
- **Cross-Validation RMSE**: 0.1270
- **Target Transform**: `log1p` + `expm1` for SalePrice


---

## 📁 Files Included

| File | Description |
|------|-------------|
| `House_Price_Prediction.ipynb` | Full Colab notebook |
| `train.csv` / `test.csv` | Dataset files |
| `submission.csv` | Final prediction file |

---

## 🧠 Key Learnings

- Real-world handling of missing data
- Importance of feature engineering in boosting model performance
- How to combine preprocessing and modeling pipelines effectively
- Power of XGBoost in tabular regression tasks

