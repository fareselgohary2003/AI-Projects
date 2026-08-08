# Heart Disease Prediction

## Overview

This project uses machine learning to predict the presence of heart disease based on patient health and clinical features.

The project follows a complete machine learning workflow, including data exploration, visualization, preprocessing, model training, evaluation, and model comparison.

---

## Dataset

The dataset contains **270 patient records** with **13 features** and one target variable.

### Features

- Age
- Sex
- Chest pain type
- BP
- Cholesterol
- FBS over 120
- EKG results
- Max HR
- Exercise angina
- ST depression
- Slope of ST
- Number of vessels fluro
- Thallium

### Target

**Heart Disease**

- `0` → Absence
- `1` → Presence

---

## Project Workflow

### 1. Data Exploration

- Inspected the dataset structure and data types
- Checked for missing values
- Examined descriptive statistics
- Analyzed the target distribution
- Studied feature correlations

### 2. Exploratory Data Analysis

Several visualizations were used to understand the data, including:

- Histograms
- Boxplots
- Countplots
- Correlation Heatmap

The analysis helped identify relationships between clinical features and heart disease.

### 3. Data Preprocessing

- Separated features and target
- Split the data into training and testing sets
- Used stratified train-test splitting
- Applied `StandardScaler` for Logistic Regression

### 4. Machine Learning Models

Two classification models were trained:

- Logistic Regression
- Random Forest Classifier

### 5. Model Evaluation

The models were evaluated using:

- Accuracy
- Precision
- Recall
- F1-Score
- Confusion Matrix
- ROC-AUC

---

## Model Performance

| Model | Accuracy | ROC-AUC |
|---|---:|---:|
| Logistic Regression | **85.19%** | **0.901** |
| Random Forest | 83.33% | 0.885 |

### Best Model

**Logistic Regression** achieved the best overall performance on the test set.

- Accuracy: **85.19%**
- Precision (Heart Disease): **79%**
- Recall (Heart Disease): **92%**
- F1-Score (Heart Disease): **85%**
- ROC-AUC: **0.901**

The high recall indicates that the model was able to identify most of the patients with heart disease in the test set.

---

## Confusion Matrix

The Logistic Regression model produced:

| | Predicted No Disease | Predicted Disease |
|---|---:|---:|
| Actual No Disease | 24 | 6 |
| Actual Disease | 2 | 22 |

This resulted in only **2 False Negatives** out of 24 actual heart disease cases in the test set.

---

## Feature Analysis

The Logistic Regression coefficients were analyzed to understand the influence of the features on the predictions.

### Strong Positive Coefficients

- Number of vessels fluro
- Sex
- Chest pain type
- Thallium
- Exercise angina
- Slope of ST

### Negative Coefficients

- Max HR
- FBS over 120

These coefficients provide additional interpretability and help understand how different features contribute to the model's predictions.

---

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook
- Kaggle

---

## Project Structure

```text
Heart-Disease-Prediction/
│
├── Heart-Disease-Prediction.ipynb
└── README.md
