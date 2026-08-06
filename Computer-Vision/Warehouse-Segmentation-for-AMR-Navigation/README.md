# Warehouse Segmentation for AMR Navigation

## Overview

This project presents a YOLOv8 Segmentation model developed for warehouse environment understanding in Autonomous Mobile Robot (AMR) systems.

The model is trained to detect and segment warehouse racks and storage boxes, enabling robots to better understand their surroundings and support autonomous navigation in industrial environments.

---

## Project Objectives

- Detect warehouse racks in real-time.
- Detect storage boxes in warehouse environments.
- Segment objects with pixel-level accuracy.
- Support AMR localization and navigation.
- Enhance obstacle awareness and warehouse mapping.

---

## Technologies Used

- Python
- YOLOv8 Segmentation
- PyTorch
- OpenCV
- NumPy
- Kaggle
- ONNX Export

---

## Dataset

Custom warehouse dataset containing two classes:

| Class ID | Class Name |
|-----------|------------|
| 0 | Box |
| 1 | Rack |

The dataset was prepared in YOLO Segmentation format and used to train a custom warehouse perception model for AMR applications.

---

## Model Training

### Model
- YOLOv8n-Seg

### Training Configuration
- Epochs: 50
- Image Size: 640 × 640
- Framework: Ultralytics YOLOv8
- Platform: Kaggle GPU

---

## Performance Metrics

### Bounding Box Metrics

| Metric | Value |
|----------|----------|
| Precision | ~0.89 |
| Recall | ~0.45 |
| mAP50 | ~0.55 |
| mAP50-95 | ~0.41 |

### Segmentation Metrics

| Metric | Value |
|----------|----------|
| Precision | ~0.89 |
| Recall | ~0.45 |
| mAP50 | ~0.55 |
| mAP50-95 | ~0.34 |

---

## Training Results

![Training Results](results/results.png)

---

## Sample Predictions

### Prediction 1

![Prediction 1](assets/prediction_1.jpg)

### Prediction 2

![Prediction 2](assets/prediction_2.jpg)

---

## Applications

This model can be integrated into:

- Autonomous Mobile Robots (AMR)
- Smart Warehouses
- Inventory Monitoring Systems
- Warehouse Automation
- Industrial Robotics
- Intelligent Navigation Systems

---

## Use Case in AMR Systems

The segmentation model is designed to support warehouse navigation tasks by enabling the robot to:

- Detect warehouse racks.
- Detect storage boxes.
- Understand warehouse layouts.
- Improve obstacle awareness.
- Assist autonomous navigation and path planning.

This project serves as a perception module that can be integrated with ROS2-based AMR systems and autonomous warehouse robots.

---

## Repository Structure

```text
warehouse-segmentation-for-amr-navigation
│
├── assets
│   ├── prediction_1.jpg
│   └── prediction_2.jpg
│
├── results
│   ├── results.png
│   ├── confusion_matrix.png
│   ├── confusion_matrix_normalized.png
│   ├── BoxF1_curve.png
│   ├── BoxPR_curve.png
│   ├── BoxP_curve.png
│   ├── BoxR_curve.png
│   ├── MaskF1_curve.png
│   ├── MaskPR_curve.png
│   ├── MaskP_curve.png
│   └── MaskR_curve.png
│
├── weights
│   ├── best.pt
│   ├── best.onnx
│   └── last.pt
│
└── warehouse-segmentation-for-amr-navigation.ipynb
```

---

## Model Files

Available trained models:

- best.pt
- best.onnx

The ONNX model can be deployed on edge devices and industrial systems.

---

## Future Improvements

- Increase dataset size.
- Improve segmentation accuracy.
- Train larger YOLOv8 models.
- Deploy on Raspberry Pi.
- Integrate with ROS2 Navigation Stack.
- Perform real-time inference on AMR platforms.

---

## Kaggle Notebook

Full training notebook:

https://www.kaggle.com/code/fareselgohary003/warehouse-segmentation-for-amr-navigation

---

## Author

### Fares Elgohary

AI & Data Science Engineer

Specialized in:

- Machine Learning
- Deep Learning
- Computer Vision
- YOLOv8
- ROS2
- Autonomous Mobile Robots (AMR)
- Python
- PyTorch

### Connect With Me

LinkedIn:
https://www.linkedin.com/in/fares-elgohary-91ba22380/

GitHub:
https://github.com/fareselgohary2003
