# Predictiong-Credit-Card-Risk

## Overview
The purpose of this analysis is to use loan data in combination with supervised machine learning with imblearn and sklearn python libraries to predict whether a loan would be considered 'high-risk' or 'low-risk' based on multiple other variables for each loan applicant. For this analysis, we tried multiple different sampling techniques to see which ones yielded the highest accuracy based on accuracy scores and confusion matrices. Lastly, we tried repeating our supervised machine learning using ensemble learning models and then evaluating them using the same methods as before.

## Results
The accuracy score, precision score, and recall score for each model is listed below:

**Naive Random Oversampling Model**
-Accuracy Score: 0.6214
-Precision Score: 0.0093
-Sensitivity: 0.5269

**SMOTE Oversampling Model**
-Accuracy Score: 0.6382
-Precision Score: 0.0097
-Sensitivity: 0.5731

**Undersampling Model**
-Accuracy Score: 0.5450
-Precision Score: 0.0061
-Sensitivity: 0.5269

**Combination sampling Model**
-Accuracy Score: 0.6400
-Precision Score: 0.0086
-Sensitivity: 0.6769

**Balanced Random Forest Model**
-Accuracy Score: 0.8621
-Precision Score: 0.0231
-Sensitivity: 0.7905

**Easy Ensemble AdaBoost Model**
-Accuracy Score: 0.8813
-Precision Score: 0.0333
-Sensitivity: 0.8038


## Summary
From the results, it is obvious that the ensemble learning models had much better performance based on their much higher accuracy, precision, and sensitivity. Of the two ensemble learners, the Easy Ensemble AdaBoost model performs slightly better in all three of these score. Of the non-ensemble learners, I would say that the combination sampling model performed the best.

For the purposes of projecting loan risk, sensitivity is a more important measure for our model as we need to minimize the number of false 'low-risk' applicants. This is because this group are the only applicant that seem like safe loanees, but are actually at risk of defaulting on their payments. Every other group in our confusion matrix is either correctly diagnosed as risky loanees or are actually reliable loanees. For this reason, I suggest the EasyEnsemble AdaBoost model is used to project credit risk for loan applicants.



