# Company Default Prediction

## Project Overview

This project focuses on predicting whether a company is likely to default using financial and business-related data. The main objective is to apply machine learning models to identify default risk and compare model performance using suitable classification metrics.

The project uses Logistic Regression as the main interpretable model and also compares it with other models such as Linear Discriminant Analysis and Random Forest.

## Objective

The objective of this project is to:

* Analyze company default-related data
* Build classification models to predict default risk
* Compare model performance
* Identify whether a company is likely to default or not
* Support credit risk and financial decision-making

## Dataset

The dataset used in this project is:

```text
companyDefault.csv
```

The target variable is:

```text
Default
```

It indicates whether a company has defaulted or not.

## Tools and Libraries Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* Statsmodels
* Jupyter Notebook

## Methodology

The project follows these steps:

1. Imported required Python libraries.
2. Loaded and explored the company default dataset.
3. Checked dataset structure, missing values, and target distribution.
4. Cleaned column names for easier analysis.
5. Split the dataset into training and testing data.
6. Built a Logistic Regression model.
7. Compared Logistic Regression with LDA and Random Forest.
8. Evaluated models using accuracy, ROC-AUC, confusion matrix, and classification report.
9. Applied threshold optimization to improve default prediction.
10. Added observations and conclusion based on model performance.

## Models Used

* Logistic Regression
* Linear Discriminant Analysis
* Random Forest Classifier

## Key Results

| Model                         |      Accuracy |                         ROC-AUC |
| ----------------------------- | ------------: | ------------------------------: |
| Logistic Regression           | Around 80.05% |                   Around 0.6938 |
| Optimized Logistic Regression | Around 75.96% | Improved default identification |
| Random Forest                 | Around 83.89% |                   Around 0.8957 |

## Key Observations

* Logistic Regression is useful because it is simple and easy to interpret.
* Random Forest performed better in terms of accuracy and ROC-AUC.
* The default threshold of 0.5 may not always be suitable for credit-risk problems.
* Threshold optimization helped improve the model’s ability to identify possible default cases.
* ROC-AUC is an important metric because it shows how well the model separates default and non-default companies.

## Business Use Case

This project is useful for credit risk analysis, loan approval decisions, financial monitoring, and early warning systems. It can help financial institutions identify companies that may have a higher chance of defaulting.

## Conclusion

This project demonstrates how machine learning can be used for company default prediction. Logistic Regression provides interpretability, while Random Forest gives stronger predictive performance. The analysis shows that model evaluation should not depend only on accuracy, especially in credit-risk problems where identifying possible defaulters is more important.
