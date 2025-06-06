
# Credit Card Fraud Detection Using Machine Learning

## Overview

This project focuses on building machine learning models to accurately detect fraudulent credit card transactions. The dataset used includes transactions made by European cardholders in September 2013. A key challenge in this problem is the **high class imbalance**, as fraudulent transactions represent only **0.172%** of the total data.

## Who Will Benefit and Why

* **Financial Institutions**: Can use the model to flag and investigate suspicious transactions in real-time, helping reduce monetary losses.
* **Data Scientists & Engineers**: Provides hands-on experience with imbalanced classification, model tuning, and evaluation strategies.
* **Security Analysts**: Can apply the insights to fraud prevention systems and improve alert precision.

## Dataset

The dataset is publicly available on Kaggle:
👉 [Credit Card Fraud Detection Dataset on Kaggle](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud)

* Features V1 to V28 are anonymized principal components obtained through **PCA**.
* The **'Time'** and **'Amount'** features are original and untransformed.

---

## Approach

### 1. Data Preparation

* All features were already numeric, as the dataset had PCA transformation applied during preprocessing by the dataset authors. No additional dimensionality reduction was performed in this project.
* Standardized and prepared the dataset for model training.

### 2. Data Splitting

* The dataset was split into **80% training** and **20% testing** to evaluate model generalization.

### 3. Model Building

Three classification models were implemented and tested:

* **Logistic Regression**
* **Random Forest Classifier**
* **XGBoost Classifier**

### 4. Model Evaluation

Models were assessed using the following metrics to capture performance under class imbalance:

* **Accuracy**
* **Precision**
* **Recall**
* **F1 Score**

Cross-validation was used to validate performance robustness across different data subsets.

### 5. Parameter Tuning

* **Randomized Search** was applied to optimize the hyperparameters of the XGBoost model.

### 6. Final Model Selection

* The **XGBoost model with best-tuned parameters** was selected for final evaluation and prediction.

---

## Results and Performance Comparison

| Model               | Accuracy   | Precision  | Recall     | F1 Score   |
| ------------------- | ---------- | ---------- | ---------- | ---------- |
| Logistic Regression | 99.92%     | 87.67%     | 63.37%     | 73.56%     |
| Random Forest       | 99.95%     | 91.67%     | 76.24%     | 83.24%     |
| XGBoost             | 99.95%     | 92.13%     | 81.19%     | 86.32%     |
| **Final XGBoost**   | **99.96%** | **92.22%** | **82.18%** | **86.91%** |

### Model Insights

* **Logistic Regression**: High accuracy but limited recall, which may result in missing fraudulent cases.
* **Random Forest**: Strong performance across all metrics, offering a balanced detection rate.
* **XGBoost**: Outperformed all other models, particularly in recall and F1 score, indicating better detection of fraudulent transactions.

---

## Conclusion

The **optimized XGBoost model** demonstrated the best overall performance, achieving:

* **Accuracy**: 99.96%
* **F1 Score**: 86.91%
* **Recall**: 82.18%

Its strong balance between identifying fraud (recall) and minimizing false positives (precision) makes it the **most suitable model for credit card fraud detection** in this dataset.

---

## Course Acknowledgement

This project was completed as part of the Udemy course:
🎓 [Machine Learning Projects for Beginners in Python by Vijay Gadhave](https://www.udemy.com/course/machine-learning-projects-for-beginners-in-python/learn/lecture/25516790?start=90#questions)

It showcases practical techniques in handling real-world fraud detection problems using machine learning.

---
