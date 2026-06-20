# Credit Risk Modelling in Python

## Project Overview

This project focuses on predicting credit card default risk using machine learning. The goal is to identify customers who may default on their next payment based on their demographic, credit limit, repayment history, bill amount, and payment amount details.

## Objective

The objective of this project is to:

* Analyze credit card customer data
* Predict payment default risk
* Compare multiple machine learning models
* Evaluate model performance using credit-risk metrics
* Support better risk monitoring and decision-making

## Dataset

The dataset used in this project is:

```text
UCI_Credit_Card.csv
```

The target variable is:

```text
default.payment.next.month
```

It indicates whether a customer defaulted on the next month’s credit card payment.

## Tools and Libraries Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* Imbalanced-learn
* XGBoost
* Jupyter Notebook

## Methodology

The project follows these steps:

1. Loaded and explored the credit card dataset.
2. Checked missing values, data types, and class distribution.
3. Cleaned categorical values in `EDUCATION` and `MARRIAGE`.
4. Split the dataset into training and testing sets using stratified sampling.
5. Applied SMOTE only on training data to handle class imbalance.
6. Built and compared multiple classification models.
7. Evaluated models using accuracy, ROC-AUC, precision, recall, F1-score, confusion matrix, ROC curve, and precision-recall curve.
8. Identified the best-performing model based on ROC-AUC and default detection ability.

## Models Used

* Logistic Regression
* Random Forest Classifier
* XGBoost Classifier

## Key Results

| Model               |      Accuracy |       ROC-AUC |
| ------------------- | ------------: | ------------: |
| Logistic Regression | Around 67.27% | Around 0.7108 |
| XGBoost             | Around 75.33% | Around 0.7412 |
| Random Forest       | Around 77.02% | Around 0.7576 |

## Key Observations

* The dataset is imbalanced, so accuracy alone is not enough.
* Recall and ROC-AUC are important for identifying likely defaulters.
* Random Forest performed best based on ROC-AUC.
* SMOTE helped improve learning from the minority default class.
* Proper preprocessing was important to avoid misleading results.

## Business Use Case

This project can help banks and financial institutions identify customers with higher default risk, improve credit monitoring, prioritize collection efforts, and support better lending decisions.

## Conclusion

This project demonstrates how machine learning can be used for credit risk prediction. Random Forest achieved the strongest overall performance, while Logistic Regression provided a simpler and more interpretable baseline. The project highlights the importance of handling class imbalance and evaluating models using risk-focused metrics.
