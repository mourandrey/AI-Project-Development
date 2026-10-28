# Customer Churn Prediction
Machine Learning · Python · Scikit-learn

## Project Overview
This project aims to predict customer churn in the telecommunications industry using machine learning techniques.
The goal is to identify customers who are more likely to leave the company by analyzing their demographic information, subscribed services, contract types, payment methods, and billing information.

## Objectives
- Perform Exploratory Data Analysis (EDA).
- Clean and preprocess the dataset.
- Identify patterns and factors associated with customer churn.
- Train and compare machine learning classification models.
- Optimize model hyperparameters and evaluate predictive performance.

## Technologies Used
- Python — Programming language.
- Pandas — Data manipulation and analysis.
- NumPy — Numerical operations.
- Matplotlib and Seaborn — Data visualization.
- Scikit-learn — Data preprocessing, model training, hyperparameter tuning, and evaluation.
- Jupyter Notebook — Interactive development environment.

## Dataset
The project uses the Telco Customer Churn dataset, which contains customer information, subscribed services, contract details, billing data, and churn status.
The target variable is Churn, which indicates whether a customer left the company (Yes) or remained (No).

## Project Workflow
1. Data Exploration: Analyzed data types, missing values, duplicate records, distributions, and relationships between customer attributes and churn.
2. Data Preprocessing: Converted TotalCharges to numeric format, handled missing values, standardized numerical features, and encoded categorical variables.
3. Model Training: Implemented Logistic Regression and Random Forest classification models.
4. Hyperparameter Tuning: Used GridSearchCV with 5-fold cross-validation to optimize model parameters.
5. Model Evaluation: Compared models using Accuracy, Precision, Recall, F1-score, ROC-AUC, ROC curves, and confusion matrices.
6. Model Interpretation: Analyzed Logistic Regression coefficients to identify features associated with churn predictions.
7. Final Testing: Evaluated the selected Logistic Regression model on a separate test dataset.

## Machine Learning Models
- Logistic Regression
- Random Forest Classifier

## Evaluation Metrics
The models were evaluated using:
- Accuracy
- Precision
- Recall
- F1-score
- ROC-AUC
These metrics provide different perspectives on model performance, particularly the ability to identify customers likely to churn.

## Key Findings

- Analyzed 7,043 customer records to investigate patterns associated with customer churn.
- Performed data preprocessing, including missing value handling, numerical feature scaling, and categorical feature encoding.
- Trained and compared Logistic Regression and Random Forest models.
- Optimized hyperparameters using GridSearchCV with 5-fold cross-validation.
- Selected Logistic Regression as the final model based on its validation performance.

### Final Model Performance

The Logistic Regression model achieved the following results on the test dataset:

| Metric | Test Result |
|---|---:|
| Accuracy | 80.98% |
| Precision | 68.69% |
| Recall | 52.31% |
| F1-score | 59.39% |
| ROC-AUC | 0.8446 |

The model achieved a ROC-AUC of 0.8446, indicating a good ability to distinguish between customers who churn and those who remain.

### Confusion Matrix

| | Predicted: No Churn | Predicted: Churn |
|---|---:|---:|
| Actual: No Churn | 709 | 67 |
| Actual: Churn | 134 | 147 |

The model correctly identified 147 customers who churned, but missed 134 customers who actually left the company. This highlights an opportunity to improve churn detection.

Overall, Logistic Regression outperformed Random Forest in terms of F1-score and ROC-AUC on the validation dataset and was selected for final testing.

Future Improvements
- Compare additional classification algorithms.
- Optimize the classification threshold based on business requirements.
- Apply explainability techniques such as SHAP.
- Deploy the selected model through a REST API.
Author
Andrey Moura Ferreira
