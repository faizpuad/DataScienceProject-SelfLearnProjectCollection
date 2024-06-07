# Yelp Restaurant Review

## Problem Statement
Newly open Restaurant need to face with potential hype of food’s trend of preference by customers, cultural preference and even influence by geographical aspect. Thus, it is most likely to lose significant revenue due to inadequate research for start up.

## Summary 

This project is done for predicting rating by two approach:  
* Multiclass prediction with using attributes of restaurant as input features
* Multiclass prediction using text/comment from reviewer

This project also apply recommender system using content based recommendation to see the relevance of having more features towards relevancy of recommended restaurants list.

The data obtain from https://www.yelp.com/dataset.

In this project, there are a total of four notebooks:
1) EDA
2) preprocessing_and_nlp_model
3) model_Classification
4) recommender_by_attribute


## Contents:

1. [Datasets Used](#1-Datasets-Used)
2. [Exploratory Data Analysis & Data Cleaning](#2-Exploratory-Data-Analysis-&-Data-Cleaning)
3. [Modeling & Evaluation](#3-Modeling-&-Evaluation)
4. [Conclusion and Recommendations](#4-Conclusion-and-Recommendations)
5. [Python Library Used](#5-Python-Library-Used)

### 1. Datasets Used
The following datasets were used during this project:
- business yelp dataset
- review yelp dataset

### 2. Exploratory Data Analysis & Data Cleaning
In this section, we undergo studying, understanding and feature engineering of the datasets. After that, datasets of review and business dataframe were combined. The following actions are taken:
- Examining the data and eliminating features that are not required.
- Remove or replace null values with 'unknown' as cannot simply assumed all null is not important.
- Extract attributes'column values and make them into category. Then dummified the attributes to change it from string to numerical data.
- Text from review dataset is clean by using regex, lemmatization and transform to numerical using tfidf vectorizer and count vectorizer.
- Category variable are converted to numerical using label encoder transformer.

### 3. Modelling & Evaluation
Several classifier models were developed, where the hyperparameters were tuned for each model to obtain the best cross-validated AUC scores,accuracy and F1 score. Because there were imbalances in the data collected in train data (25% of overall data after train test split) an over-sampling method known as SMOTE (Synthetic Minority Over-sampling Technique) was adopted. It was also the reason for optimizing the models on AUC scores instead of accuracy. Comparing the AUC and recall scores, the production model selected was the Gradient Boosting Classifier model. Comparing the train and test accuracy scores of the selected model, there was evidence of slight overfitting for logistic regression model. It is also found that all model perform better as new feature column introduced where:

Models used for attributes input features prediction:
- Logistic Regression
- Random Forest Classifier
- Gradient Boost Classifier

Models used for text input features prediction:
- Multinomial Naive Bayes

Evaluation Metrics used:
- ROC-AUC score
- F1-Score
- Recall
- Precision
- Accuracy

### 4. Conclusion & Recommendation
1. In multiclass classification prediction, gradient bossting classifier perform the best with F1 score of 1 .
2. For binary classification prediction using text input, Multinomial Naive Bayes perform at moderately average.
3. Increasing bag of word could help increasing Multinomial performance but computational heavy.
4. For future work, is a possibility to combine multiclass approach which use attributes and combine with bag of words to further increase model performance to predict rating.
5. This is shown in recommender system too as more variance introduce(attributes introduce), more relevant restaurant are recommended.

### 5. Python Library Used
- Pandas
- Numpy
- Seaborn
- Matplotlib
- Pickle
- Joblib
- Sklearn
- Imblearn
- nltk
- os
- json
- scipy
