# Supervised Learning – Discrete Variable Prediction: Fraud Detection

## Overview
This project focuses on utilizing machine learning algorithms for detecting fraudulent credit card transactions. With the growing sophistication of fraudsters, traditional methods are often inadequate. Our approach leverages data science to develop predictive models capable of identifying fraudulent activities.

## Model Selection
We explore several classification methods to predict whether a transaction is fraudulent or legitimate:

1. Logistic Regression Classifier
2. Support Vector Machine (SVM) Classifier
3. K-Nearest Neighbor (KNN) Classifier
4. Decision Tree Classifier
5. Random Forest Classifier
6. Naive Bayes Classifier

## Dataset
The dataset used is a simulated credit card transaction dataset, containing both legitimate and fraudulent transactions from January 1, 2019, to December 31, 2020. It includes features such as transaction date, credit card number, merchant, transaction amount, and a binary indicator for fraud.

### Dataset Features
- **Unnamed: 0**: Row index
- **trans_date_trans_time**: Timestamp of the transaction
- **cc_num**: Credit card number (masked/encrypted in practice)
- **merchant**: Merchant identifier
- **category**: Transaction category
- **amt**: Transaction amount
- **first, last**: Cardholder's name
- **gender**: Cardholder's gender
- **street, city, state, zip**: Cardholder's address
- **lat, long**: Cardholder's geographical coordinates
- **city_pop**: Population of the city
- **job**: Cardholder's occupation
- **dob**: Date of birth
- **trans_num**: Transaction number
- **unix_time**: Transaction time in Unix format
- **merch_lat, merch_long**: Merchant's geographical coordinates
- **is_fraud**: Fraud indicator (0 = legitimate, 1 = fraudulent)

### Data Imbalance
The dataset is highly imbalanced, with approximately 99.42% of transactions being non-fraudulent (Class 0) and only 0.58% being fraudulent (Class 1). Various techniques such as SMOTE (Synthetic Minority Over-sampling Technique) will be employed to address this imbalance.

## Methodology
### 1. Data Preprocessing
- **Feature Engineering**: Time features are extracted, including hour and day of the week. New features such as transaction frequency over the last 1, 7, and 30 days are created.
- **Imbalance Handling**: SMOTE is applied to ensure a balanced representation of both classes during model training.

### 2. Exploratory Data Analysis (EDA)
EDA is conducted to uncover patterns and relationships in the data, such as transaction trends over time and correlations with features like age and transaction amount.

### 3. Model Training and Evaluation
Models are trained on the training set (80% of the data) and evaluated on the test set (20% of the data). Metrics used for evaluation include accuracy, precision, recall, F1 score, AUC curve, and confusion matrix.

### 4. Implementation of Pipeline
A scikit-learn pipeline is created to streamline the process from preprocessing to model training and evaluation.

## Results
- **Random Forest Classifier** achieved the highest accuracy of 0.9960, with a precision of 0.91 and recall of 0.35.
- **SVM** and **KNN** also performed well, but with slightly lower accuracy.
- The **F1 score** for Random Forest was 0.51, indicating a balance between precision and recall.

## Handwritten Digits Prediction (Extra Credit)
In an additional task, we explored predicting handwritten digits using non-deep learning models. Dimensionality reduction techniques like PCA and t-SNE were utilized to address the challenges posed by high-dimensional image data.

## Conclusion
This project demonstrates the application of various machine learning models for fraud detection in credit card transactions. Through careful data preprocessing, feature engineering, and model evaluation, we aim to improve the accuracy of fraud detection systems, ultimately reducing financial losses for businesses and organizations.

