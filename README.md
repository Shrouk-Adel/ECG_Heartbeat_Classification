### What is an ECG?
An Electrocardiogram (ECG) is a test that measures the electrical activity of the heart. It records the heart's rhythm and electrical signals, helping detect various heart conditions.

### How This App Works
This app uses a machine learning model trained to classify different types of heartbeats based on ECG data. It first processes the input data, performs feature scaling, and then applies a trained model to predict the type of heartbeat.

### Types of Heartbeats Classified
1. **Normal Beat**: A healthy heartbeat.
2. **Premature Ventricular Contraction (PVC)**: An early beat originating from the ventricles.
3. **Unclassified beat'**
4. **Supraventricular premature or ectopic beat**
5. **Fusion of ventricular and normal beat**

![Heartbeat](https://github.com/user-attachments/assets/17bd1bbc-6268-46a2-beb6-0e8bb3a6a822)

## Project Goal
Maximize recall in heartbeat classification to ensure comprehensive detection of cardiac abnormalities, prioritizing the identification of potential heart conditions with minimal missed cases.

## Recall Performance Analysis

### 1. Binary Classification (Logistic Regression)
- **Overall Recall**:
  - Class 0: 0.86
  - Class 1: 0.77
- **Key Challenge**: Lower recall for minority class (Class 1)
- **Potential Impact**: Risk of missing critical cardiac events

### 2. Multi-Class Classification: Recall Comparison

#### XGBoost Classifier
- **Recall Performance**:
  - Class 0.0: 0.90
  - Class 1.0: 0.97
  - Class 2.0: 0.81
  - Class 3.0: 0.99
- **Observations**:
  - Excellent recall for Classes 1.0 and 3.0
  - Lowest recall for Class 2.0 (potential area of improvement)

#### Random Forest
- **Recall Performance**:
  - Class 0.0: 0.92
  - Class 1.0: 0.98
  - Class 2.0: 0.80
  - Class 3.0: 0.99
- **Key Insights**:
  - Consistently high recall for majority classes
  - Class 2.0 remains a challenge with 0.80 recall

#### XGBoost Classifier (Alternative Implementation)
- **Recall Performance**:
  - Class 0.0: 0.93
  - Class 1.0: 0.98
  - Class 2.0: 0.89
  - Class 3.0: 0.99
- **Improvement Noted**:
  - Slight increase in recall for Class 2.0
  - Maintained high recall for other classes

### 3. Convolutional Neural Network (1D Conv)
- **Test Accuracy**: 0.9812
- **Recall Focus**: Demonstrates strong overall performance

## Dataset 
https://www.kaggle.com/datasets/shayanfazeli/heartbeat
