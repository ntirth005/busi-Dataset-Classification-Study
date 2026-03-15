# BUSI-Breast-Ultrasound-Classification

Study on Deep Learning for Medical Image Classification

This repository contains an experimental project exploring deep learning techniques for classifying breast ultrasound images and studying the impact of class imbalance handling methods.

---

## 📂 Project: BUSI Dataset Classification using CNN

### Objective

Classify breast ultrasound images into three categories using a Convolutional Neural Network (CNN) and analyze how class imbalance affects model performance.

### Classes

- Benign
- Malignant
- Normal

---

## Methods

- Baseline CNN
- CNN + SMOTE (Synthetic Minority Oversampling Technique)
- CNN + Class Weighting

---

## Data Preprocessing

- Mask images removed
- Images resized to **128 × 128**
- Pixel normalization to **[0,1]**
- Stratified train–test split

---

## CNN Architecture

- Conv2D (32 filters, 3×3)
- MaxPooling (2×2)
- Conv2D (64 filters, 3×3)
- MaxPooling (2×2)
- Conv2D (128 filters, 3×3)
- MaxPooling (2×2)
- Flatten
- Dense (128 units)
- Dropout (0.5)
- Output Layer (Softmax, 3 classes)

---

## Evaluation Metrics

- Accuracy
- Precision
- Recall
- F1-score

---

## Dataset

Breast Ultrasound Images Dataset (BUSI)

https://www.kaggle.com/datasets/aryashah2k/breast-ultrasound-images-dataset

### Dataset Statistics

- Total Images: 780
- Benign: 437
- Malignant: 210
- Normal: 133

---

## Kaggle Notebook

[(Add your Kaggle notebook link here)](https://www.kaggle.com/code/naumisharanyatirth/busi-dataset-classification-pynb/edit)

---

## Results

| Model | Accuracy | Precision | Recall | F1-score |
|------|------|------|------|------|
| Baseline CNN | 0.72 | 0.74 | 0.72 | 0.69 |
| CNN + SMOTE | **0.77** | **0.77** | **0.77** | **0.76** |
| CNN + Class Weight | 0.74 | 0.75 | 0.74 | 0.74 |

---

## Key Finding

Handling class imbalance significantly improves classification performance.  
The CNN trained with **SMOTE** achieved the best overall results by generating synthetic samples for minority classes.  
Class weighting also improved minority class detection by assigning higher importance to underrepresented classes during training.

---

## Tools and Libraries

- Python
- TensorFlow / Keras
- OpenCV
- Scikit-learn
- Imbalanced-learn
- Matplotlib

---

## Future Work

- Apply transfer learning (ResNet / EfficientNet)
- Use data augmentation techniques
- Explore advanced imbalance handling methods

---

## Author

**Naumisharanya Tirth**  
Indian Institute of Information Technology Raichur  
Email: cs23b1050@iiitr.ac.in
