# Mortgage Default Prediction

## Project Overview

This project focuses on predicting mortgage loan default risk using machine learning. The objective is to identify borrowers who are more likely to default based on mortgage, borrower, and loan-related variables.

The project compares different classification models and evaluates them using suitable credit-risk metrics such as ROC-AUC, recall, precision, F1-score, and confusion matrix.

## Objective

The main objective of this project is to:

* Analyze mortgage loan data
* Predict whether a borrower may default
* Compare multiple machine learning models
* Identify important risk-related features
* Support credit risk monitoring and loan portfolio management

## Dataset

The dataset used in this project is:

```text
mortgage.csv
```

The dataset contains mortgage loan records with borrower, loan, property, and repayment-related variables.

The target variable used for prediction is:

```text
default_time
```

This variable is used to identify whether a mortgage loan default occurred.

## Tools and Libraries Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* XGBoost
* Jupyter Notebook

## Methodology

The project follows these steps:

1. Loaded and explored the mortgage dataset.
2. Checked dataset shape, missing values, and default distribution.
3. Removed leakage columns such as future outcome-related variables.
4. Selected relevant predictor variables for modelling.
5. Split the data into training and testing sets using stratified sampling.
6. Handled missing values using preprocessing pipelines.
7. Built and compared multiple classification models.
8. Evaluated model performance using accuracy, ROC-AUC, recall, precision, F1-score, confusion matrix, ROC curve, and precision-recall curve.
9. Identified the best-performing model based on ROC-AUC and default recall.
10. Added observations and conclusion based on model results.

## Data Leakage Handling

Columns such as `default_time`, `payoff_time`, and `status_time` contain outcome or future information. These columns were removed from the input features to avoid data leakage.

Data leakage can make a model appear highly accurate during testing but fail in real-world prediction. Therefore, only variables that would be available before loan default were used as predictors.

## Models Used

* Logistic Regression
* Random Forest Classifier
* XGBoost Classifier

## Key Results

| Metric                 |        Result |
| ---------------------- | ------------: |
| Total records          |       622,489 |
| Target variable        |  default_time |
| Default rate           |  Around 2.44% |
| Best model             |       XGBoost |
| XGBoost accuracy       | Around 64.11% |
| XGBoost ROC-AUC        | Around 77.58% |
| XGBoost default recall | Around 77.18% |

## Key Observations

* The dataset is highly imbalanced because default cases are very low compared to non-default cases.
* Accuracy alone is not a reliable metric for this project.
* Recall is important because missing an actual default customer can create financial risk.
* ROC-AUC is useful for evaluating how well the model separates default and non-default borrowers.
* XGBoost performed well in identifying higher-risk mortgage borrowers.
* Data leakage handling was important to make the model more realistic.

## Business Use Case

This project can be useful for banks, NBFCs, mortgage lenders, and credit-risk teams. It can support:

* Mortgage default risk prediction
* Early warning systems
* Loan portfolio monitoring
* Credit risk assessment
* Collection prioritization
* Risk-based decision-making

## Conclusion

This project demonstrates how machine learning can be applied to mortgage default prediction. Since mortgage defaults are rare, the model was evaluated using recall, ROC-AUC, and F1-score instead of relying only on accuracy.

Among the models tested, XGBoost provided strong performance in identifying possible default cases. The project also highlights the importance of avoiding data leakage and using proper evaluation metrics in credit-risk modelling.
