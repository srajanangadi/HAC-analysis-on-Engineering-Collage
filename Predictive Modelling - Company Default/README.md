# Twitter Sentiment Analysis / Hate Speech Classification

## Project Overview

This project performs text classification on a Twitter dataset to identify whether a tweet is **normal/non-hate speech** or **hate/offensive speech**. The analysis uses Natural Language Processing (NLP) techniques and machine learning models to clean tweet text, convert it into numerical features, and classify the tweet label.

Although the file is named as a sentiment analysis project, the dataset is more specifically focused on **hate speech or offensive tweet classification**, where the model predicts whether a tweet belongs to class `0` or class `1`.

## Objective

The main objective of this project is to build a machine learning model that can classify tweets into two categories:

- **Class 0:** Non-hate / normal tweet
- **Class 1:** Hate / offensive tweet

The project also compares multiple classification models and identifies the best-performing model based on evaluation metrics such as accuracy, precision, recall, F1-score, and ROC-AUC.

## Dataset

The dataset used in this project is:

```text
tweet.csv
```

The dataset contains **31,962 tweet records** with the following columns:

```text
id
label
tweet
```

### Target Variable

```text
label
```

The target variable contains two classes:

| Label | Meaning |
|---|---|
| 0 | Non-hate / normal tweet |
| 1 | Hate / offensive tweet |

## Tools and Libraries Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Regular Expressions
- Jupyter Notebook

## Methodology

The project follows the below steps:

1. Imported the required Python libraries.
2. Loaded the Twitter dataset.
3. Checked dataset structure, missing values, and class distribution.
4. Cleaned the tweet text using text preprocessing techniques.
5. Removed Twitter handles such as `@user`.
6. Removed URLs, special characters, numbers, and extra spaces.
7. Converted all text into lowercase.
8. Split the dataset into training and testing sets using stratified sampling.
9. Converted tweet text into numerical features using TF-IDF vectorization.
10. Built machine learning pipelines for different models.
11. Trained and evaluated multiple classification models.
12. Compared model performance using classification metrics.
13. Selected the best model based on ROC-AUC and class-wise performance.
14. Added observations and conclusion based on model results.

## Models Used

The following machine learning models were compared:

1. **Multinomial Naive Bayes**
2. **Logistic Regression**
3. **Random Forest Classifier**

## Evaluation Metrics

The models were evaluated using:

- Accuracy
- Precision
- Recall
- F1-score
- Confusion Matrix
- ROC-AUC Score
- ROC Curve

Since the dataset is imbalanced, accuracy alone is not enough. More importance is given to **recall, F1-score, and ROC-AUC**, especially for class `1`, which represents hate/offensive tweets.

## Key Results

| Metric | Result |
|---|---|
| Total records | 31,962 |
| Target column | label |
| Text column | tweet |
| Best model | Logistic Regression |
| Best ROC-AUC | Around 0.94 |
| Class 1 recall | Around 0.79 |

## Key Observations

- The dataset is imbalanced, with a much larger number of normal tweets compared to hate/offensive tweets.
- Logistic Regression performed better overall compared to Naive Bayes and Random Forest.
- TF-IDF vectorization was effective for converting tweet text into machine-readable features.
- Class `1` recall is important because missing hate/offensive tweets can reduce the practical usefulness of the model.
- ROC-AUC is a better evaluation metric than accuracy for this project because of class imbalance.

## Business / Real-World Use Case

This type of model can be useful for:

- Social media content moderation
- Hate speech detection
- Brand safety monitoring
- Online community management
- Automatic flagging of offensive content
- Reducing manual review workload

A platform can use this model to automatically flag tweets that are likely to contain offensive or harmful content, allowing moderators to review them more efficiently.

## Conclusion

This project demonstrates how Natural Language Processing and machine learning can be used to classify tweets as normal or hate/offensive content. After cleaning the tweet text and applying TF-IDF vectorization, multiple models were trained and compared.

Among the tested models, **Logistic Regression** achieved the best overall performance with a ROC-AUC score of around **0.94** and strong recall for the hate/offensive tweet class. This makes it a suitable baseline model for text classification tasks involving social media content moderation.

The project highlights the importance of proper text preprocessing, handling class imbalance, and using suitable evaluation metrics beyond accuracy.
