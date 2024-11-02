# DS course project 4 - Classification
The source of the data can be found in https://www.kaggle.com/datasets/shrutimechlearn/churn-modelling/data

![image](https://github.com/user-attachments/assets/f11d5423-6f6c-4a39-a355-15975e2cd92a)

# Churn Prediction in Banking

This repository contains a machine learning model that predicts **customer churn** for a banking institution. 
The model analyzes customer attributes to predict the likelihood of churn, helping the bank implement strategies to retain high-risk customers. 
This project uses various machine learning and ensemble techniques, with hyperparameter tuning and custom threshold adjustments to optimize performance.

## Table of Contents
- [Project Overview](#project-overview)
- [Methods and Techniques](#methods-and-techniques)
  - [Data Preprocessing](#data-preprocessing)
  - [Modeling and Hyperparameter Tuning](#modeling-and-hyperparameter-tuning)
  - [Threshold Adjustment](#threshold-adjustment)
- [Model Evaluation](#model-evaluation)
- [Results](#results)

## Project Overview

Churn prediction helps identify customers likely to leave the bank, allowing the institution to focus retention efforts on high-risk customers. 
The project implements several machine learning techniques, including ensemble models and optimized hyperparameter tuning with Optuna. 
Additionally, threshold tuning and custom ensemble methods were applied to improve performance metrics.

## Methods and Techniques

### Data Preprocessing
- **Feature Engineering**: Several new features were created to enhance model performance.
- **Scaling and Encoding**: Numerical features were standardized using `StandardScaler` within a `Pipeline`, and categorical variables were one-hot encoded.
- **Handling Imbalanced Data**: SMOTE (Synthetic Minority Oversampling Technique) was tested to balance the dataset by oversampling the minority class.

### Modeling and Hyperparameter Tuning
- **Ensemble Models**: A Voting Classifier with soft voting was used, combining a Random Forest and XGBoost model.
- **Hyperparameter Tuning**: Optuna was employed to tune model parameters, with careful configuration to maximize F1 score, focusing on both recall and precision.
- **Custom Thresholds**: After obtaining probabilities from the ensemble, optimal decision thresholds were calculated to maximize F1 score, achieving the best balance between precision and recall.

### Threshold Adjustment
The final model’s threshold was tuned using a custom method:
- **Precision-Recall Curve**: Used to identify an optimal threshold for the best F1 score, allowing fine control over false positives and false negatives.

## Model Evaluation

The model’s performance was evaluated using:
- **Accuracy, Precision, Recall, F1 Score**: Calculated on the test dataset to assess model effectiveness.
- **Confusion Matrix**: Provided a breakdown of true positives, false positives, true negatives, and false negatives.

Additional techniques:
- **Feature Importance Analysis**: Extracted from individual models within the ensemble to identify the most influential features.

## Results

The final model achieved the following results on the test dataset:
- **Accuracy**: `X.XX`
- **Precision**: `X.XX`
- **Recall**: `X.XX`
- **F1 Score**: `X.XX`

The model demonstrated strong performance in identifying customers likely to churn, with a customized threshold to balance precision and recall effectively.
