### **Bitcoin Price Prediction using Machine Learning**



This notebook focuses on utilising machine learning techniques for predicting Bitcoin prices.

The workflow covers data preprocessing, feature engineering, exploratory data analysis, and comparison of multiple ML classifiers.



#### **Project Overview**

-The core objective is to develop and compare several machine learning models to classify the direction of Bitcoin price movement based on historical market data.



###### **Data Preparation and Exploration**

The dataset imported contains 2,713 daily records from 2014 to early 2022, with columns including Date, Open, High, Low, Close, Adjusted Close, and Volume.

Initial exploratory data analysis included summary statistics using describe(), type checks, and missing value detection, confirming that the dataset is clean with appropriate data types and no null values.

A line plot visualizes Bitcoin's closing price over the period for trend inspection.

Additional temporal features, such as year, month, day, and a custom "isquarterend" flag, are generated for deeper time-based analysis.



###### 

###### **Feature Engineering**

Feature engineering creates key input variables for prediction:

open-close: The daily change between opening and closing prices.

low-high: The daily price range.

is\_quarter\_end: Binary flag marking quarter-ending days.

Target variable: Classifies if the next day’s closing price is higher (1) or not (0), preparing the data for a binary classification task.





###### **Data Preprocessing**

Features are scaled using StandardScaler.

The dataset is split into training and validation sets (70%/30% split).

Correlation analysis using a heatmap was performed to inspect relationships between features.





###### **Model Training and Evaluation**

Three classifiers were trained and evaluated:

**Logistic Regression**

Simple linear model for binary classification.

**Support Vector Machine (SVC)**

Used with a polynomial kernel and probability outputs enabled.

**XGBoost Classifier**

The Gradient boosting method, known for robust tabular predictive power.





###### **Results (Key Metrics)**

**Classifier**	      **Training Accuracy**	   **Validation Accuracy**

Logistic Regression	~0.53	               ~0.51

Support Vector (SVC)	~0.47	               ~0.47

XGBoost Classifier	~0.94	               ~0.47



Training and validation results are reported for each model.

While XGBoost shows high training accuracy, its validation performance is similar to other models, suggesting possible overfitting or insufficiently informative features.

The notebook uses ROC-AUC score for model evaluation.





###### **Visualization and Reporting**

The notebook includes multiple plots:

Historical price trend, feature distributions, and bar plots of yearly averages for Open, High, Low, and Close prices.

Heatmaps and feature correlation visualizations support feature analysis and model explanation.



**Closing Price Trend:**

The Bitcoin closing price trend over the years 2014 to 2022 shows a clear upward trajectory with significant volatility.

Prices have gradually increased from relatively low levels in early years, reflecting growing adoption and interest, to marked peaks in recent years.

This trend visualization helps contextualise the challenging nature of predicting highly volatile cryptocurrency markets.



**Feature Correlation Heatmap:**

The correlation heatmap shows the relationships between key trading features such as Open, High, Low, Close prices, and Volume.

Strong positive correlations exist among price-related features, indicating that these prices move in tandem during trading days.

Volume shows weaker correlation, highlighting its unique behavior and potential complementary information for modeling.



**Yearly Average Prices:**

Year-wise average plots of Open, High, Low, and Close prices illustrate the incremental growth and yearly variation in Bitcoin price behavior.

These averages help summarize longer-term trends across multiple price points and support feature engineering efforts related to temporal patterns.



###### **Conclusions**

Multiple classical ML models were implemented to predict Bitcoin's next-day price movement.

Feature engineering centred on price differences and quarterly effects.

Validation accuracy for all models hovers just above random, with XGBoost exhibiting significant overfit on training data, suggesting limitations of this approach in its current feature set or that further feature engineering and data enhancement may be needed for improvement.





