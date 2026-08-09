# Bank Marketing Campaign — Machine Learning

## Overview
Machine learning project for predicting whether a customer will subscribe to a bank term deposit using the Bank Marketing dataset.

## Dataset
- **11,162 customers**
- **17 features** after feature engineering
- Target: `deposit`
  - `0` → No
  - `1` → Yes
- Target distribution: 52.62% No / 47.38% Yes

## Project Workflow
- Data Cleaning & Exploration
- Exploratory Data Analysis (EDA)
- Feature Engineering
- Train/Test Split (80/20)
- One-Hot Encoding
- Feature Scaling
- Model Training & Comparison
- Final Model Evaluation

## Feature Engineering
Created `previous_contact` from `pdays`:

- No previous contact → 40.65% subscription rate
- Previous contact → 67.12% subscription rate

## Models & Results

| Model | Accuracy |
|---|---:|
| XGBoost | **86.48%** |
| Random Forest | 85.45% |
| SVM | 85.13% |
| Logistic Regression | 82.62% |
| Decision Tree | 79.18% |
| KNN | 75.68% |

**Best Model: XGBoost — 86.48% Accuracy**

### Key Insights
- Previous campaign contact was strongly associated with subscription.
- Customers with a successful previous campaign had a **91.32%** subscription rate.
- Customers without a housing loan had a **57.03%** subscription rate.
- Subscription rates varied significantly across campaign months.
- Students and retired customers had among the highest subscription rates.

## Technologies
Python • Pandas • NumPy • Matplotlib • Seaborn • Scikit-learn • XGBoost • Jupyter Notebook

## Files
- `bank_marketing_analysis.ipynb` — Complete analysis and machine learning workflow
- `dataset/` — Dataset used for the project

## Conclusion
XGBoost achieved the best performance among the evaluated models, demonstrating that customer characteristics and campaign history can be useful for predicting bank term-deposit subscriptions.
