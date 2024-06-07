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
4. [Conclusion](#4-Conclusion)
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
The correlation done including relationship:
* Comorbid type and percentage of submission
* Distribution of age of patient admitted/registered
* Vaccine consumed distribution from the patient admitted/registered

### 3. Modelling & Evaluation
Because the subject (healthcare) really heavily on judgment of medical officer, thus careful consideration done was to dig up literature review of past similar case of analysis involving health dataset. From the literature review, few model were identified to be commonly used in this classification area. Afterwards, the evaluation metrics were done to be compared with the academic papers result as a matter of comparison. Refer Project3_FAIZPUAD_samplecode.pdf for said literature review done.

Models used for attributes classification:
- SVM
- Naive Bayes
- Random Forest
- Decision Tree
  
Evaluation Metrics includes:
- F1-Score
- Recall
- Precision

### 4. Conclusion
1. Comorbid respiratory has significant relation for plan admit decision
2. The model achieve f1 score of 100% for every model if respiratory included in the model training
3. SVM performs the best with 10 folds cross-validation
4. SVM achieve the highest accuracy compared to other models at 10 fold cross-validation (after tuning)
5. SVM > Naive Bayes Classifier > Random Forest > Decision Tree

### 5. Python Library Used
- Pandas
- Numpy
- Seaborn
- Matplotlib
- Sklearn

### 6. Presentation
https://express.adobe.com/page/8Vg3Vq9L8DF5t/
