# Employee Turnover Prediction

## Project Overview
Employee turnover is a significant challenge for organizations, leading to increased recruitment and training costs, loss of institutional knowledge, and disruption of operations. This project aims to predict employee turnover using machine learning models by analyzing employee data to proactively identify employees at risk of leaving the organization.

## Table of Contents
1. [Introduction](#introduction)
2. [Dataset Overview](#dataset-overview)
3. [Data Distribution](#data-distribution)
4. [Data Cleaning](#data-cleaning)
5. [Project Objective](#project-objective)
6. [Model Performance Comparison](#model-performance-comparison)
    - Accuracy
    - Confusion Matrix
7. [Summary & Insights](#summary--insights)
8. [Best Model Selection](#best-model-selection)
9. [Hyperparameter Tuning](#hyperparameter-tuning)
10. [Model Evaluation](#model-evaluation)
11. [Insights](#insights)
    - Evaluate Other Metrics
    - Overall Model Performance
12. [Cross Validation](#cross-validation)
13. [Feature Importance](#feature-importance)
14. [Conclusion](#conclusion)
15. [Recommendation](#recommendation)
16. [Business Impact](#business-impact)

## Introduction
Employee turnover prediction enables organizations to take proactive steps to retain key employees. This project explores the performance of multiple machine learning models in predicting employee turnover.

## Dataset Overview
The dataset contains 14,999 employee records with features like job satisfaction, last evaluation score, time spent at the company, and whether the employee left the company.

### Features:
- **satisfaction_level**: Employee satisfaction (0-1)
- **last_evaluation**: Time since last evaluation
- **average_monthly_hours**: Average hours worked per month
- **time_spent_company**: Time spent at the company (years)
- **work_accident**: Whether the employee had a workplace accident (0 or 1)
- **promotion_last_5years**: Promotion in the last 5 years (0 or 1)
- **department**: Department of the employee
- **salary**: Salary level (low, medium, high)
- **left**: Whether the employee left (0 = No, 1 = Yes)

## Project Objective
To build and compare machine learning models (Logistic Regression, SVM, KNN, and Random Forest) to predict the target variable `left`, which indicates whether an employee has left the company or not.

## Model Performance Comparison
Four machine learning models were used in this project:
- **Random Forest Classifier**
- **Logistic Regression**
- **Support Vector Machine (SVM)**
- **K-Nearest Neighbors (KNN)**

### Accuracy
- **Random Forest**: 98.6%
- **Logistic Regression**: 79.4%
- **SVM**: 78.3%
- **KNN**: 94.2%

### Confusion Matrix
Each model's confusion matrix is used to evaluate its performance across true positive, true negative, false positive, and false negative rates.

## Summary & Insights
- **Random Forest** had the highest accuracy and balanced performance across both classes.
- **Logistic Regression** and **SVM** struggled with class imbalance, performing poorly in predicting the minority class (employees who left).
- **KNN** showed relatively strong performance, but Random Forest was the most robust model overall.

## Best Model Selection
The **Random Forest** model was selected for further analysis based on its excellent performance.

## Hyperparameter Tuning
- **Best Parameters for Random Forest**: `max_depth = None`, `n_estimators = 300`

## Model Evaluation
- **Accuracy**: 98.6%
- **Precision (Class 0)**: 0.99
- **Recall (Class 1)**: 0.95
- **F1-Score (Class 1)**: 0.97
- **ROC-AUC Score**: 0.9915

## Insights
The Random Forest model performed well across all metrics, demonstrating high precision and recall for both classes. This makes it a suitable choice for deployment in predicting employee turnover.

## Cross Validation
- **Mean Accuracy**: 98.58%
The model showed consistently high performance across all cross-validation folds, indicating strong generalization capabilities.

## Feature Importance
- **Top Feature**: Employee satisfaction level
Employee satisfaction was identified as the most significant predictor of turnover, followed by time spent at the company and salary level.

## Conclusion
The **Random Forest** model is the best-performing model for predicting employee turnover. It provides high accuracy, balanced performance across both classes, and handles class imbalance effectively.

## Recommendation
- **Implement Random Forest Model**: Deploy the model in an HR analytics platform to predict employee turnover risk in real-time.
- **Focus on Key Features**: Use feature importance to focus on critical factors such as job satisfaction, time spent at the company, and salary for employee retention strategies.
- **Develop Retention Programs**: Based on predictions, create tailored employee engagement, professional development, and compensation programs.
- **Monitor Model Performance**: Continuously update the model with new data to ensure its accuracy and relevance over time.

## Business Impact
By implementing this model, the organization can significantly reduce employee turnover, resulting in cost savings, improved employee satisfaction, and enhanced productivity.

## Jupyter Notebook

[View the notebook on GitHub](https://github.com/jessicaphamca/Employee_Turnover_Prediction/blob/main/HR_analysis.ipynb)

[Download the presentation PDF](https://github.com/jessicaphamca/Employee_Turnover_Prediction/blob/main/HR%20Analysis%20Presentation.pdf)
