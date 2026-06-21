# Tip Prediction and Restaurant Sales Analysis

## Project Overview

This project analyzes restaurant billing data to understand customer tipping behavior and predict tip amounts using machine learning models. The goal is to identify the key factors that influence tips and generate useful insights for restaurant business decision-making.

## Business Objective

The objective of this project is to:

* Analyze customer tipping patterns
* Predict tip amount based on bill and customer-related features
* Understand factors affecting service-based revenue
* Support restaurant pricing, staffing, and customer service decisions

## Tools & Technologies

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* Random Forest Regressor
* Linear Regression
* Jupyter Notebook

## Dataset

The dataset contains restaurant transaction-level information such as total bill, tip amount, customer gender, smoking status, day, time, and party size. These features were used to analyze tipping behavior and build prediction models.

## Project Workflow

1. **Data Loading & Understanding**
   Loaded the dataset and reviewed its structure, data types, and summary statistics.

2. **Data Preprocessing**
   Checked missing values, encoded categorical variables, and prepared numerical and categorical features for modeling.

3. **Exploratory Data Analysis**
   Analyzed tip distribution, total bill patterns, customer size, day-wise behavior, and relationships between bill amount and tips.

4. **Model Building**
   Built regression models to predict tip amount using Linear Regression and Random Forest Regressor.

5. **Model Evaluation**
   Evaluated models using MAE, RMSE, R² score, and cross-validation.

## Model Performance

| Model                   | R² Score |
| ----------------------- | -------: |
| Linear Regression       |    ~0.44 |
| Random Forest Regressor |    ~0.35 |

## Key Observations

* Total bill amount had a strong relationship with tip amount.
* Larger bills generally resulted in higher tips.
* Customer size, day, and time also influenced tipping behavior.
* Linear Regression performed better than Random Forest on this dataset.
* Random Forest was still useful for understanding feature importance.

## Business Insights

* Restaurants can use tip prediction to understand customer spending and service trends.
* Total bill amount is the most important driver of tip amount.
* Day-wise and time-wise analysis can help with staffing and service planning.
* Understanding tipping behavior can support better customer service and revenue planning.

## Conclusion

This project demonstrates how regression models can be used to analyze and predict restaurant tipping behavior. Although Random Forest was tested, Linear Regression performed better on this dataset, showing that simpler models can sometimes be more effective when the relationship between variables is mostly linear.

From a business analytics perspective, this project highlights how transaction-level data can be used to understand customer behavior, improve service planning, and support revenue-based decision-making.

## Future Improvements

* Add more restaurant-specific features such as server rating, cuisine type, and customer feedback
* Compare additional regression models
* Perform hyperparameter tuning for Random Forest
* Use the model for customer spending and service analysis
