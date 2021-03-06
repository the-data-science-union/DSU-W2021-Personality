# Predicting Personality Traits with Classification Models
## The Data Science Union at UCLA
Project Leads: [Karina Santoso](https://github.com/kcsantoso), [Madison Kohls](https://github.com/madisonkohls)

Project Members: [Anish Dulla](https://github.com/AnishDulla), [Elizabeth Gallmeister](https://github.com/elizabethgallmeister), [Ethan Duong](https://github.com/eduong100), [Louis Zhao](https://github.com/louis-zhao101), [Rebecca Chua](https://github.com/beccachua), [Sarah Kosic](https://github.com/sarahkos), [Sean Tjoa](https://github.com/seantjoa), [Tara Jaigopal](https://github.com/tarajaigopal), [Trina Nguyen](https://github.com/Trina152)

# Table of Contents
- [Abstract](#Abstract)
- [Introduction](#Introduction)
- [Conclusion](#Conclusion)

# Abstract
* There are many patterns between a person's personality traits, demographic characteristics, and interests—can we use some of this information to predict others?
* Though there are numerous approaches to go about this, the models we chose to explore were Logistic Regression, Naives Bayes, Stochastic Gradient Descent, Random Forests, and KNN.
* Feature selection, hyperparameter tuning, and SMOTE were added to our models for optimization, efficiency, and to aid in prediction accuracy.
* The biggest challenge we faced in the modeling process was dealing with an unbalanced distribution of classes.
* We were able to achieve an accuracy of 94% for binary prediction with SVM using linear kernels with feature selection, and an accuracy of 71% for multinomial prediction with Naive Bayes classification.

# Introduction
From renowned psychological assessments to Buzzfeed quizzes, predicting aspects of a person from a given set of responses has always been of great interest. These predictions can allow us to understand the behavior of an individual or group, which can: refine clinical diagnoses of psychologists, enhance advertisement strategies for businesses, and bring self-awareness to individuals. For these reasons, our team had two main objectives. First, we wanted to see if we could accurately predict different aspects of a person based on a series of responses ranging from demographic to preference-based. Second, we wanted to determine what classification models were the best predictors for certain questions pertaining to our dataset.

For the full report, see the attached [PDF]().

# Conclusion
Model Conclusions:
* Logistic Regression: RFE was used for feature selection in the binomial model, and sklearn’s SelectFromModel was used in the multinomial model. Binary classification achieved a 68% accuracy rate; multinomial achieved 58%. Uneven distribution in the data created the biggest challenge in prediction accuracy.
* Naive Bayes: Sklearn’s SelectFromModel for feature selection to create more independence among the variables and thus a more accurate model. Our first model predicted a person’s alcohol usage with 71% accuracy, and our second model which predicted one’s willingness to pay for healthy food at 55% accuracy.
* Support Vector Machines: SVM effectiveness varies largely on feature scaling and selection. Our model predicted gender extremely well (94%) but had trouble predicting multiclass variables. Feature selection boosted accuracy immensely for multiclass classification but only marginally improved binomial classification.
* Random Forest: Due to class imbalance and lack of strong relationships between predictors and response variables, our Random Forest model struggled to predict test cases. RFE and SelectKBest produced similar results in baseline accuracy scores, but SelectKBest was significantly faster, making it more efficient.
* KNN: Imbalanced distribution of the classification variable led to a relatively high accuracy but reduced sensitivity. Using SMOTE to alter the distribution of minority and majority classes improved sensitivity; however, this also led to a fall in accuracy, indicating a tradeoff between the two metrics.

Through the results of our different models, we found a pretty wide range in accuracy between models, response variables, and binomial vs multinomial models. The biggest challenge in increasing accuracy in most, if not all, the models was the imbalanced distribution of the dataset used to train the models. Since the dataset was made up of survey data, it was very natural for some outcomes to be more common than others, e.g. having siblings being much more likely than being an only child. This led to many of the models simply predicting the majority class(es) more often to increase its accuracy score, which in turn made it very difficult to increase accurately predicting classes in the minority and led to a “plateau” in accuracy scores.

Despite this challenge, there were models that were able to attain a high level of accuracy—especially with binary classification—which indicates possible relationships between personality traits, interests, and demographic information. In the future, we would look further into exploring these relationships but with a much larger and possibly more diverse dataset, as well as look into the incorporation of other machine learning methods such as xgboost and neural networks.
