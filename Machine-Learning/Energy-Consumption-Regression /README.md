# Energy Consumption Prediction using Linear Regression

## Overview

This project uses **Linear Regression** to predict building energy consumption based on building characteristics, occupancy, appliance usage, temperature, and day of the week.

The project covers a complete Machine Learning workflow, including data exploration, preprocessing, model training, evaluation, and interpretation.

## Dataset

The dataset contains 7 columns:

- `Building Type`
- `Square Footage`
- `Number of Occupants`
- `Appliances Used`
- `Average Temperature`
- `Day of Week`
- `Energy Consumption` — Target

The dataset is divided into separate training and testing files.

## Workflow

```text
Data Loading
     ↓
Data Exploration
     ↓
Data Cleaning
     ↓
EDA & Visualization
     ↓
One-Hot Encoding
     ↓
Linear Regression
     ↓
Test Set Evaluation
     ↓
Residual Analysis
     ↓
Feature Interpretation
