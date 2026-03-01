# Heart Disease Prediction

## Task Objective
The goal of this task was to build a predictive model that identifies whether a person is at risk of heart disease based on their health data. The project involves data preprocessing, exploratory analysis, model training, evaluation, and feature importance analysis.

## Dataset Used
- **Dataset:** Heart Disease UCI Dataset
- **Source:** Kaggle
- **Description:** The dataset contains health-related attributes such as age, sex, blood pressure, cholesterol, heart rate, and others, along with the target variable `condition` indicating the presence or absence of heart disease.

## Models Applied
1. **Logistic Regression** – A linear model for binary classification.
2. **Decision Tree Classifier** – A non-linear model capturing feature interactions for classification.

## Key Results and Findings
- **Model Accuracy:**
  - Logistic Regression: 91.67%
  - Decision Tree: 80.00%
- **Insights:**
  - Logistic Regression showed high predictive performance with a simple linear relationship between features and heart disease risk.
  - Decision Tree captured non-linear interactions but had lower accuracy, suggesting the dataset may favor linear modeling.
  - Feature importance analysis revealed that factors such as `cp` (chest pain), `thalach` (max heart rate), and `oldpeak` were influential in predicting heart disease.
- Both models provide a strong baseline for further improvements and tuning.
