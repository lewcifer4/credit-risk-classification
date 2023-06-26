# credit-risk-classification

# Introduction

Use various techniques to train and evaluate a model based on loan risk. You’ll use a dataset of historical lending activity from a peer-to-peer lending services company to build a model that can identify the creditworthiness of borrowers

# Analysis Overview

The dataset was split in to two different sets - training and testing. The training set was used to build an initial logistic regression model using the LogisticRegression module from scikit-learn. This model was then applied to the testing dataset, the purpose being to determine whether a loan to a borrower in the testing set would be low or high risk.

The initial model was drawing from a dataset that had 75,036 low risk loan data points and 2500 high risk data point. The data was resampled to ensure the logistiv regression model had an equal number of data points to draw from, using the RandomOverSampler module from inbalanced-learn. This provided 56,277 data points for both low-risk (0) and high-risk (1) loans, based on the original dataset.

The resampled data was used to build a new logistic regression model, the purpose of which was to determine whether a loan to the borrower in the testing set would be low- or high-risk. The results can be found below:

# Results

Logistic Regression Model 1:

Precision: 93% (an average--in predicting low-risk loans, the model was 100% precise, though the model was only 87% precise in predicting high-risk loans)
Accuracy: 94%
Recall: 95% (an average--the model had 100% recall in predicting low-risk loans, but 89% recall in predicting high-risk loans)

Logistic Regression Model 2:

Precision: 93% (an average--in predicting low-risk loans, the model was 100% precise, though the model was only 87% precise in predicting high-risk loans)
Accuracy: 100%
Recall: 100%

# Summary

Logistic Regression Model 2 is less likely to predict false negative results. However, based on the confusion matrices for each model, Logistic Regression Model 2 predicted slightly more false positives (low-risk when the actual was high-risk).

If the goal of the model is to determine the likelihood of high-risk loans, neither model scores above 90% precision. Logistic Regression Model 2 had fewer false predictions of the testing data overall and would be the best model to use based on the high accuracy and recall of this model.
