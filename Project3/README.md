# Assist Covid Patient Placement Decision For Covid Assessment Centre

## Problem Statement
Covid Assessment Centre (CAC) Cheras staff need to manually decide how many patients that are needed to be admitted in the hospital. Due to unpredictable covid-19 cases around, the staff voiced concern with the large value volume of patient registrations which can reach more than 200 patients per day.

## Approach 

This project is done by two approach:  
* To explore trends in CAC's admission on covid cases
* To identify the most suitable model for admission classification

In this project, there is only a notebook use for brief reference and maintain confidentiality of patient's data:
1) Project3_FAIZPUAD_samplecode.ipynb

## Contents:

1. [Datasets Used](#1-Datasets-Used)
2. [Exploratory Data Analysis & Data Cleaning](#2-Exploratory-Data-Analysis-&-Data-Cleaning)
3. [Modeling & Evaluation](#3-Modeling-&-Evaluation)
4. [Conclusion and Recommendations](#4-Conclusion-and-Recommendations)
5. [Python Library Used](#5-Python-Library-Used)
6. [Link to Presentation](#6-Presentation)

### 1. Datasets Used
The following dataset was used during this project:
- covid patients registration data (provided by staff of CAC)
- refer the Dataset Description.pdf to understand better on the data use in this project

### 2. Exploratory Data Analysis & Data Cleaning
Following the features (as mentioned in ) EDA is done to find correlation between the features with the following in mind that results in admission:
* Maternal with age > 40
* Maternal with obesity
* Exhibit any of teh five comorbid
* Category CAT 2B and above (High risk patient)

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

### 6. Presentation
https://express.adobe.com/page/8Vg3Vq9L8DF5t/
