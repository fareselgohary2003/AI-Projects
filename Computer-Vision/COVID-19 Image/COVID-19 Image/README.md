# COVID-19 Image Classification using CNN & Transfer Learning

## Overview
Deep Learning project for classifying chest X-ray images into **COVID-19, Normal, and Viral Pneumonia** using CNN and Transfer Learning.

## Dataset
- COVID: 111 Train / 26 Test
- Normal: 70 Train / 20 Test
- Viral Pneumonia: 70 Train / 20 Test
- Total: **251 Train / 66 Test**
- Image Size: **224×224**

## Workflow
**Data Preprocessing → Augmentation → CNN from Scratch → Class Weights → MobileNetV2 Transfer Learning → Evaluation**

## Models
### CNN from Scratch
- Training Accuracy: ~86%
- Validation Accuracy: **44%**
- Result: Severe Overfitting; model predicted almost all validation images as COVID.

### MobileNetV2 Transfer Learning
- ImageNet pretrained weights
- Frozen base model
- Global Average Pooling + Dense + Dropout
- Trainable Parameters: **164,355**

## Final Results 🏆
- Validation Accuracy: **86.00%**
- Test Accuracy: **87.88%**
- Test Loss: **0.3475**
- Macro F1: **0.86**
- Weighted F1: **0.87**

| Class | Precision | Recall | F1 |
|---|---:|---:|---:|
| COVID | 1.00 | 1.00 | 1.00 |
| Normal | 1.00 | 0.60 | 0.75 |
| Viral Pneumonia | 0.71 | 1.00 | 0.83 |

## Key Insights
- CNN from scratch suffered from severe overfitting due to the small dataset.
- Class Weights alone did not solve the generalization problem.
- **MobileNetV2 Transfer Learning significantly improved performance.**
- Main confusion occurred between **Normal and Viral Pneumonia**.
- MobileNetV2 was the **best-performing model** with **87.88% Test Accuracy**.

## Technologies
**Python | TensorFlow | Keras | NumPy | Pandas | Matplotlib | Seaborn | Scikit-learn | Kaggle**

