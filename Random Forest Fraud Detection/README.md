# Fraud Risk Detection using Random Forest

## Project Overview

This project focuses on identifying potentially risky individuals using demographic and financial attributes. The dataset is commonly referred to as the **Fraud Check dataset**, where taxpayers are classified into **Good** or **Risky** categories based on their taxable income.

The main goal of this project is to build a machine learning model that can support risk-based decision-making and help prioritize individuals who may require further review.

## Business Objective

In financial and tax-related operations, identifying high-risk cases early can help organizations reduce losses, improve compliance, and allocate investigation resources more effectively.

This project aims to:

* Classify individuals into **Good** and **Risky** categories
* Support fraud-risk screening and taxpayer risk assessment
* Handle class imbalance using proper sampling techniques
* Compare baseline Random Forest performance with SMOTE-based modeling
* Generate business insights from important risk indicators

## Tools & Technologies

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* imbalanced-learn
* Random Forest Classifier
* SMOTE
* Jupyter Notebook

## Dataset

The dataset contains taxpayer-related information such as:

* Undergrad status
* Marital status
* Taxable income
* City population
* Work experience
* Urban or rural residence

A new target variable was created from taxable income:

* **Risky**: Taxable income less than or equal to 30,000
* **Good**: Taxable income greater than 30,000

This makes the project more suitable as a **taxpayer risk classification** problem rather than direct transaction-level fraud detection.

## Project Workflow

1. **Data Loading & Understanding**
   Loaded the dataset and reviewed the structure, data types, missing values, and target distribution.

2. **Target Variable Creation**
   Created a risk category based on taxable income to classify taxpayers as Good or Risky.

3. **Exploratory Data Analysis**
   Analyzed class distribution, demographic patterns, income distribution, and relationships between features and risk category.

4. **Data Preprocessing**
   Encoded categorical variables and prepared the dataset for machine learning.

5. **Stratified Train-Test Split**
   Used stratified splitting to preserve the same class distribution in both training and testing data.

6. **Model Building**
   Built a baseline Random Forest model and compared it with a Random Forest model trained using SMOTE.

7. **SMOTE Balancing**
   Applied SMOTE only on the training data to balance the minority Risky class without affecting the test set.

8. **Model Evaluation**
   Evaluated the models using accuracy, confusion matrix, precision, recall, F1-score, and cross-validation.

## Model Performance

| Model                 |                         Accuracy |            Macro F1-score | Key Insight                               |
| --------------------- | -------------------------------: | ------------------------: | ----------------------------------------- |
| Random Forest         |                             ~62% |                      ~44% | Baseline model struggled with Risky class |
| Random Forest + SMOTE | Improved minority-class learning | Slightly improved balance | Better for risk-focused analysis          |

## Key Observations

* The dataset is imbalanced, with more Good taxpayers than Risky taxpayers.
* Stratified splitting helped maintain a fair class distribution in train and test data.
* SMOTE helped the model learn more from the minority Risky class.
* Accuracy alone was not enough to judge the model because the business goal is to identify risky individuals.
* Recall and F1-score are more important for this type of risk classification problem.
* The Random Forest model provided useful feature importance insights for business interpretation.

## Business Insights

* Risk classification can help organizations prioritize cases for further review.
* Demographic and financial attributes can be used to identify possible risk patterns.
* SMOTE is useful when the minority class is important from a business perspective.
* In fraud or risk analytics, missing a risky case can be more costly than incorrectly flagging a good case.
* The model can support decision-making, but final fraud investigation should still involve human review and domain expertise.

## Conclusion

This project demonstrates how Random Forest can be used for taxpayer risk classification using structured financial and demographic data. The baseline model provided a starting point, while SMOTE helped address class imbalance and improved the model’s ability to learn from risky cases.

From a business analytics perspective, the project highlights the importance of looking beyond accuracy and focusing on recall, F1-score, and class-level performance when dealing with fraud-risk or compliance-related problems.

The project is best positioned as a **Fraud Risk Screening** or **Taxpayer Risk Classification** solution rather than direct fraud detection, since the dataset does not contain actual transaction-level fraud labels.

## Future Improvements

* Try Logistic Regression, XGBoost, and Gradient Boosting for comparison
* Perform hyperparameter tuning using GridSearchCV or RandomizedSearchCV
* Use class weights along with SMOTE for better minority-class prediction
* Build a simple dashboard for business users to monitor risk patterns
