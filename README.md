# 🛡️ System Threat Forecasting - Malware Infection Prediction

This project was developed as part of the **IIT Madras BS Degree Program**, and it achieved an **A grade** for its thorough approach and performance. The goal was to predict whether a system would be infected by various families of malware using rich telemetry data from antivirus threat reports.

## 📌 Project Overview

This was a classification problem where the task was to predict the **probability of a system getting infected** based on system properties captured through telemetry data. These properties were anonymized and provided in a structured format for training and testing.

- 📊 **Highest Accuracy Achieved**: `0.6295`
- 🏁 **Evaluation Metric**: `accuracy_score` between predicted labels and true labels

## 📂 Dataset Description

The data included:
- Anonymized telemetry attributes of systems
- Target label indicating malware infection
- Diverse and mixed-type features (categorical, ordinal, numerical)

## 🔍 Key Steps in the Pipeline

1. **Data Preprocessing**
   - Missing value imputation using `SimpleImputer`
   - Label encoding and one-hot encoding for categorical features
   - Standardization using `StandardScaler` or `RobustScaler`

2. **Feature Engineering**
   - Target encoding with `category_encoders`
   - Dimensionality reduction with PCA
   - Recursive feature elimination using RFECV

3. **Modeling**
   - Base models used:
     - `Logistic Regression`
     - `Random Forest`
     - `HistGradientBoosting`
     - `LightGBM`
     - `XGBoost`
   - Hyperparameter tuning with `GridSearchCV` and `RandomizedSearchCV`

4. **Evaluation**
   - Accuracy Score
   - Confusion Matrix
   - Classification Report
   - F1-Score

## 📈 Best Performing Model

The **LightGBM Classifier** and **HistGradientBoostingClassifier** yielded the highest accuracy after hyperparameter tuning and feature selection, achieving a final accuracy of **0.6295**.

## 📤 Submission Format

Your predictions should be submitted as a `.csv` file with the following structure:

```csv
Id,Prediction
1,2
2,0
3,1
...
