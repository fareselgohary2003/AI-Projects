# Diabetic Foot Ulcer Detection using MobileNetV2

## Overview
This project uses Deep Learning and Computer Vision to classify diabetic foot images into two classes: **Abnormal (Ulcer)** and **Normal (Healthy skin)**. A custom CNN was developed as a baseline, followed by a **MobileNetV2 Transfer Learning** model.

## Dataset
- Binary image classification dataset
- Classes:
  - Abnormal (Ulcer)
  - Normal (Healthy skin)
- Image size: **224 × 224**
- Training/Validation split: **80% / 20%**
- Validation samples: **211 images**

## Methodology
1. Load and preprocess the images.
2. Analyze the class distribution.
3. Build and evaluate a custom CNN baseline.
4. Apply MobileNetV2 using Transfer Learning.
5. Train using Binary Cross-Entropy and Adam optimizer.
6. Use Early Stopping and Model Checkpointing.
7. Evaluate using Accuracy, Precision, Recall, F1-score, Confusion Matrix, and ROC-AUC.
8. Save the best trained model.
9. Test the model on individual images with prediction confidence.

## Results
The MobileNetV2 model achieved:
- **Validation Accuracy: 100%**
- **Validation Precision: 100%**
- **Validation Recall: 100%**
- **Best Validation Loss: 0.0077**

The CNN baseline achieved **93% accuracy** and **0.9593 ROC-AUC** on the validation set.

## Model
The final trained model was saved as:

`DFU_MobileNetV2_Final.keras`

It can be integrated into future applications for image upload or real-time camera-based prediction.

## Future Improvements
- Test on an independent external dataset.
- Fine-tune MobileNetV2.
- Add data augmentation.
- Build a Streamlit web application.
- Integrate real-time camera prediction.
- Add Grad-CAM for model explainability.

## Disclaimer
This project is for **educational and research purposes only** and is not intended to provide medical diagnosis or replace professional medical evaluation.

## Author
**Fares El-Gohary**  
Mechatronics Engineering | AI & Computer Vision
