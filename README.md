# Bitcoin-Price-Prediction-using-Machine-Learning
This project aims to predict the next-day price movement of Bitcoin using classical machine learning models.
The analysis is based on a comprehensive historical dataset from 2014 to 2022, including daily price and volume features.

**Key components of the project include:**
**Data Exploration:**
Initial statistical summary, visualization of price trends, and inspection of feature correlations to understand data characteristics.

**Feature Engineering:**
Crafting features such as daily price differences (open-close, low-high) and temporal indicators like quarter-end flags to capture market behavior patterns.

**Model Development:**
Implementation and comparison of multiple machine learning classifiers — Logistic Regression, Support Vector Machine (SVC), and XGBoost — to classify whether Bitcoin’s closing price will increase the next day.

**Evaluation:**
Performance assessment using accuracy and ROC-AUC scores. Observed validation results indicate limited predictive power with moderate accuracy slightly above random classification.

**Findings:**
XGBoost exhibited significant overfitting, showing very high accuracy on the training set but poor generalization on validation data, highlighting the challenges in modeling volatile cryptocurrency markets with basic features.

This notebook serves as a foundational exploration for Bitcoin price prediction, demonstrating practical data preprocessing, feature construction, and classical machine learning model application in a financial forecasting context.
