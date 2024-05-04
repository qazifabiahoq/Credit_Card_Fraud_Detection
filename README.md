# Credit Card Fraud Detection

## Overview

This project aims to develop a machine learning model to detect fraudulent credit card transactions. The dataset used in this project contains transactions made by credit cards in September 2013 by European cardholders. It is highly unbalanced, with the positive class (frauds) accounting for 0.172% of all transactions.

## Dataset

The dataset can be downloaded from Kaggle. https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud

## Steps Taken

### Data Preparation:
The dataset contains only numerical input variables which are the result of a PCA transformation. Features V1 to V28 are the principal components obtained with PCA, while 'Time' and 'Amount' are the original features.
### Data Splitting: 
The dataset was split into training and testing sets using an 80/20 ratio.
### Model Building: 
Implemented and evaluated the following models:

Logistic Regression

Random Forest

XGBoost

### Model Evaluation: 
Evaluated models using accuracy, precision, recall, and F1 score. Used cross-validation to ensure model robustness.

### Parameter Tuning: 
Used Randomized Search to find the best parameters for the XGBoost model.

### Final Model: 
Selected the XGBoost model with the best parameters for the final prediction.

## Results

### Logistic Regression:
Accuracy: 99.92%
Precision: 87.67%
Recall: 63.37%
F1 Score: 73.56%

### Random Forest:
Accuracy: 99.95%
Precision: 91.67%
Recall: 76.24%
F1 Score: 83.24%
### XGBoost:
Accuracy: 99.95%
Precision: 92.13%
Recall: 81.19%
F1 Score: 86.32%

### XGBoost (Final Model):
Accuracy: 99.96%
Precision: 92.22%
Recall: 82.18%
F1 Score: 86.91%

## Conclusion

The XGBoost model with optimized parameters performed the best among the models tested, achieving an accuracy of 99.96% and an F1 score of 86.91%. This model is recommended for credit card fraud detection tasks due to its high performance.

## Course Information

This project is part of the Udemy course Machine Learning Projects for Beginners in Python. It demonstrates the application of machine learning techniques to detect fraudulent credit card transactions. https://www.udemy.com/course/machine-learning-projects-for-beginners-in-python/learn/lecture/25516790?start=90#questions
