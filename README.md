# Topological Material Classification using Machine Learning

## Overview

This project applies Machine Learning techniques to classify materials as **Topological** or **Non-Topological** using structural and electronic descriptors obtained from the Materials Project database.

The workflow covers the complete ML pipeline, including data collection, preprocessing, feature engineering, model training, evaluation, explainability, and prediction on user-provided chemical formulas.

---

## Problem Statement

Discovering topological materials experimentally is expensive and time-consuming. This project explores whether machine learning models can identify topological materials directly from material descriptors, accelerating the screening process for novel materials.

---

## Dataset

A custom dataset containing approximately **3,500+ materials** was created using the Materials Project API.

### Features Used

* Band Gap
* Density
* Formation Energy
* Volume
* Number of Atomic Sites
* Crystal System
* Space Group

### Target Variable

* Topological Material
* Non-Topological Material

---

## Machine Learning Pipeline

1. Data Collection using Materials Project API
2. Data Cleaning and Preprocessing
3. Feature Engineering
4. Train-Test Split
5. Model Training
6. Model Evaluation
7. Explainability Analysis using SHAP
8. Prediction on New Materials

---

## Models Evaluated

| Model               | Accuracy |
| ------------------- | -------- |
| Logistic Regression | 84.0%    |
| SVM                 | 84.5%    |
| Decision Tree       | 83.4%    |
| Random Forest       | 87.2%    |

### Best Model

**Random Forest Classifier**

* Accuracy: **87.2%**
* ROC-AUC: **0.90**

---

# Results

## Model Accuracy Comparison

The Random Forest model achieved the highest classification accuracy among all evaluated algorithms.

![Accuracy Comparison](images/accuracy_comparison.png)

---

## ROC Curve Comparison

ROC-AUC analysis confirms strong predictive performance, with Random Forest achieving the best discrimination capability.

![ROC Curve](images/roc_curve.png)

---

## Confusion Matrix

The confusion matrix demonstrates effective classification with relatively low false-positive and false-negative rates.

![Confusion Matrix](images/confusion_matrix.png)

---

## Feature Importance

Feature importance analysis indicates that **Band Gap** is the most influential descriptor for predicting topological behavior.

### Most Important Features

1. Band Gap
2. Density
3. Volume
4. Formation Energy

![Feature Importance](images/feature_importance_plot.png)

---

## Explainable AI using SHAP

SHAP (SHapley Additive exPlanations) was used to understand how individual features influence model predictions.

The analysis reveals that electronic properties such as Band Gap and Density strongly impact classification outcomes.

![SHAP Analysis](images/shap_plot.png)

---

## Example Prediction

The trained model can predict the topological nature of a material from its chemical formula.

### Input

```text
SiO2
```

### Extracted Descriptors

| Descriptor       | Value       |
| ---------------- | ----------- |
| Band Gap         | 5.017 eV    |
| Density          | 2.082 g/cm³ |
| Formation Energy | -3.152 eV   |
| Volume           | 1437.58 Å³  |
| Sites            | 90          |
| Crystal System   | Triclinic   |
| Space Group      | P1          |

### Prediction

**Non-Topological**

![Prediction Example](images/prediction_example.png)

---

## Technologies Used

* Python
* Pandas
* NumPy
* Scikit-Learn
* Matplotlib
* SHAP
* Materials Project API
* Google Colab

---



B.Tech Engineering Physics
Delhi Technological University (DTU)
