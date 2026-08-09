# Airline Passenger Satisfaction Prediction using ANN

## Overview

This project uses an Artificial Neural Network (ANN) to predict airline passenger satisfaction based on passenger information, flight details, and service ratings.

The dataset contains separate training and testing files, allowing the model to be trained and evaluated on completely unseen data.

## Dataset

- Training samples: **103,904**
- Testing samples: **25,976**
- Original features: **25 columns**
- Features used for modeling: **27** after One-Hot Encoding
- Target: `satisfaction`

### Target Classes

- `0` → Neutral or Dissatisfied
- `1` → Satisfied

### Target Distribution

| Class | Training Samples |
|---|---:|
| Neutral / Dissatisfied | 58,879 |
| Satisfied | 45,025 |

## Data Preprocessing

The following preprocessing steps were performed:

1. Removed unnecessary identifier columns:
   - `Unnamed: 0`
   - `id`

2. Handled missing values in `Arrival Delay in Minutes` using the median value from the training data.

3. Separated the features and target variable.

4. Applied One-Hot Encoding to categorical features:
   - `Gender`
   - `Customer Type`
   - `Type of Travel`
   - `Class`

5. Used `StandardScaler` to scale the numerical features.

6. Encoded the target:
   - `satisfied` → `1`
   - `neutral or dissatisfied` → `0`

## Artificial Neural Network

A simple ANN architecture was used:

```text
Input Layer
27 Features
     ↓
Dense Layer
32 Neurons + ReLU
     ↓
Dense Layer
16 Neurons + ReLU
     ↓
Output Layer
1 Neuron + Sigmoid
