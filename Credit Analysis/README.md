# Credit Risk Analysis using Decision Tree

## Project Overview

This project uses machine learning to analyze customer credit data and predict whether a customer is likely to be a **Good** or **Risky** credit applicant. The goal is to support better lending decisions and reduce potential default risk.

## Business Objective

The main objective is to build a classification model that helps financial institutions:

* Identify high-risk credit applicants
* Improve loan approval decisions
* Reduce default-related losses
* Understand key factors affecting credit risk

## Tools & Technologies

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* Decision Tree
* Random Forest
* AdaBoost
* Gradient Boosting
* Jupyter Notebook

## Dataset

The dataset contains customer credit-related information, including demographic and financial attributes. The target variable classifies customers into credit risk categories.

## Project Workflow

1. **Data Loading & Understanding**
   Loaded the dataset and reviewed data structure, feature types, and target distribution.

2. **Data Preprocessing**
   Handled categorical variables, checked missing values, encoded features, and split the data into training and testing sets.

3. **Exploratory Data Analysis**
   Analyzed customer risk distribution and explored relationships between input features and credit risk.

4. **Model Building**
   Built a Decision Tree model and compared it with ensemble models such as Random Forest, Bagging, AdaBoost, and Gradient Boosting.

5. **Model Evaluation**
   Evaluated models using accuracy, confusion matrix, precision, recall, and F1-score.

## Model Performance

| Model                | Test Accuracy |
| -------------------- | ------------: |
| Full Decision Tree   |           69% |
| Pruned Decision Tree |           72% |
| Bagging Classifier   |           74% |
| AdaBoost Classifier  |           75% |
| Gradient Boosting    |           75% |
| Random Forest        |           75% |

## Key Observations

* The full Decision Tree showed signs of overfitting.
* Pruning improved the model’s generalization.
* Ensemble models performed better than a single Decision Tree.
* Random Forest, AdaBoost, and Gradient Boosting gave the best overall results.
* For credit risk problems, recall and F1-score are important because identifying risky customers is more valuable than accuracy alone.

## Business Insights

* Decision Tree helps explain credit decision logic clearly.
* Ensemble models provide better stability and reduce overfitting.
* The model can support financial institutions in customer risk screening.
* Predictive analytics can help reduce loan default risk and improve credit approval strategies.

## Conclusion

This project demonstrates how Decision Tree and ensemble machine learning models can be used for credit risk classification. While the basic Decision Tree was easy to interpret, it overfitted the training data. Ensemble models such as Random Forest, AdaBoost, and Gradient Boosting performed better and provided more reliable results.

From a business analytics perspective, this project shows how data-driven models can support credit risk assessment, improve decision-making, and reduce financial risk.
