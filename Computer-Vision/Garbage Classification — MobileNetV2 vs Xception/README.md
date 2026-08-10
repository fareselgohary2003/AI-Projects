#  Garbage Classification — MobileNetV2 vs Xception

A deep learning-based image classification project for automatically classifying household waste into **12 different categories**.

The project compares two state-of-the-art CNN architectures:

- **MobileNetV2** — optimized for lightweight and real-time deployment.
- **Xception** — designed to capture detailed visual and texture features using depthwise separable convolutions.

The main goal is not only to achieve high classification accuracy, but also to compare both models in terms of:

- Classification Accuracy
- Precision, Recall, and F1-Score
- Model Size
- Number of Parameters
- Inference Speed
- Deployment Efficiency

---

##  Project Overview

Waste classification is an important Computer Vision application that can help automate waste sorting and recycling systems.

In this project, a dataset containing **15,515 household-waste images** was used to train deep learning models capable of recognizing different types of waste.

The dataset contains **12 classes**:

| Class | Category | Images |
|------:|----------|-------:|
| 0 | Battery | 945 |
| 1 | Biological | 985 |
| 2 | Brown Glass | 607 |
| 3 | Cardboard | 891 |
| 4 | Clothes | 5,325 |
| 5 | Green Glass | 629 |
| 6 | Metal | 769 |
| 7 | Paper | 1,050 |
| 8 | Plastic | 865 |
| 9 | Shoes | 1,977 |
| 10 | Trash | 697 |
| 11 | White Glass | 775 |
| | **Total** | **15,515** |

---

##  Project Objectives

The main objectives of this project are:

1. Explore and analyze the garbage classification dataset.
2. Perform data validation and cleaning.
3. Prepare the dataset for deep learning.
4. Apply image data augmentation.
5. Train a lightweight **MobileNetV2** model.
6. Fine-tune MobileNetV2 for improved performance.
7. Train an **Xception** model.
8. Fine-tune Xception.
9. Evaluate both models on an unseen test set.
10. Compare classification performance.
11. Compare model size and parameter count.
12. Compare inference speed.
13. Determine which model provides the best balance between accuracy and deployment efficiency.

---

#  Dataset

The project uses the:

**Garbage Classification Dataset**

The dataset contains images belonging to 12 household waste categories.

### Dataset Statistics

- Total Images: **15,515**
- Valid Images: **15,515**
- Corrupted Images: **0**
- Number of Classes: **12**

### Dataset Split

The dataset was divided into:

| Split | Images | Percentage |
|-------|-------:|-----------:|
| Training | 12,412 | ~80% |
| Validation | 1,551 | ~10% |
| Testing | 1,552 | ~10% |
| **Total** | **15,515** | **100%** |

The split was performed while preserving the class distribution across training, validation, and test sets.

---

#  Dataset Exploration

Before training the models, the dataset was extensively explored.

The analysis included:

- Number of images per class
- Class distribution
- Dataset split distribution
- Image dimensions
- Dataset structure
- Corrupted image detection
- DataFrame construction
- Sample image visualization

### Image Dimensions

The dataset contains images with different resolutions.

| Statistic | Width | Height |
|-----------|------:|-------:|
| Count | 120 | 120 |
| Mean | 313.72 | 286.71 |
| Std | 116.15 | 119.15 |
| Minimum | 163 | 142 |
| Median | 273.50 | 225 |
| Maximum | 512 | 712 |

Because the original images have different dimensions, images are resized before being passed to the neural networks.

---

#  Data Validation

A complete validation process was performed before training.

Results:

```text
Total images: 15515
Valid images: 15515
Corrupted images: 0
