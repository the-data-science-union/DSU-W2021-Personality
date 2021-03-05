# Insert Project Title Here
## The Data Science Union at UCLA
Project Leads: [Karina Santoso](https://github.com/kcsantoso), [Madison Kohls](https://github.com/madisonkohls)

Project Members: [Anish Dulla](https://github.com/AnishDulla), [Elizabeth Gallmeister](https://github.com/elizabethgallmeister), [Ethan Duong](https://github.com/eduong100), [Louis Zhao](https://github.com/louis-zhao101), [Rebecca Chua](https://github.com/beccachua), [Sarah Kosic](https://github.com/sarahkos), [Sean Tjoa](https://github.com/seantjoa), [Tara Jaigopal](https://github.com/tarajaigopal), [Trina Nguyen](https://github.com/Trina152)

# Table of Contents
- [Abstract](#Abstract)
- [Introduction](#Introduction)
- [Data Collection and Analysis](#Data-Collection-and-Analysis)
  * [Data Cleaning](#Data-Cleaning)
  * [Data Analysis](#Data-Analysis)
- [Model Analysis](#Model-Analysis)
  * [Logistic Regression](#Logistic-Regression)
  * [Naive Bayes](#Naive-Bayes)
  * [SGD and SVM](#SGD-and-SVM)
    + [Stochastic Gradient Descent](#Stochastic-Gradient-Descent)
    + [Support Vector Machines](#Support-Vector-Machines)
  * [Random Forests](#Random-Forests)
  * [KNN](#KNN)
- [Conclusion](#Conclusion)

# Abstract
* There are many patterns between a person's personality traits, demographic characteristics, and interests—can we use some of this information to predict others?
* Though there are numerous approaches to go about this, the models we chose to explore were Logistic Regression, Naives Bayes, Stochastic Gradient Descent, Random Forests, and KNN.
* Feature selection, hyperparameter tuning, and SMOTE were added to our models for optimization, efficiency, and to aid in prediction accuracy.
* The biggest challenge we faced in the modeling process was dealing with an unbalanced distribution of classes
* We were able to achieve an accuracy of 94% for binary prediction with SVM usings linear kernels with feature selection, and an accuracy of 71% for multinomial prediction with Naive Bayes classification.
# Introduction
From renowned psychological assessments to Buzzfeed quizzes, predicting aspects of a person from a given set of responses has always been of great interest. These predictions can allow us to understand the behavior of an individual or group, which can: refine clinical diagnoses of psychologists, enhance advertisement strategies for businesses, and bring self-awareness to individuals. For these reasons, our team had two main objectives. First, we wanted to see if we could accurately predict different aspects of a person based on a series of responses ranging from demographic to preference-based. Secondly, we wanted to determine what classification models were the best predictors for certain questions pertaining to our dataset.
# Data Collection and Analysis
We chose to fit our models using the [Young People Survey](https://www.kaggle.com/miroslavsabo/young-people-survey) dataset from Kaggle. The dataset has 1010 respondents between the ages of 15 to 30 and recorded their responses to questions regarding their music preferences, movie preferences, hobbies, phobias, health habits, opinions, spending habits, and demographics. The majority of the questions have the respondent indicate their rate of agreement with the statement on a scale from 1-5, and some of them had the respondent pick one of multiple options to describe themselves. So, most of the 150 columns in the dataset are numerical (139), and 11 of the columns are categorical.
## Data Cleaning
We first approached our dataset by dropping rows with more than 3 missing values, removing 33 entries out of 1,010 in total. Then, we imputed the remaining missing values using the median for numerical measures and mode for categorical measures, modifying 303 entries. With all of the missing values removed or imputed, we were able to convert numerical measures from floats into integers, wrapping up our cleaning. For easy accessibility in future analysis, we exported the cleaned dataset to a csv file and pushed it to our GitHub repo.
## Data Analysis
# Model Analysis
## Logistic Regression
### Living Situation Analysis
### Lying Analysis
## Naive Bayes
## SGD and SVM
### Stochastic Gradient Descent
### Support Vector Machines
#### Gender Analysis
#### Happiness Analysis
## Random Forests
## KNN
# Conclusion
