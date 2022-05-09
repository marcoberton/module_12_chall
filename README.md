# Module 12 Challenge

## Overview of the Analysis

The purpose of this analysis is to identify the creditworthiness of borrowers.  Since there is inherent imbalance between the number of healthy loans and high-risk loans, the goal is to use preditive models to maximize accuracy in their performance to correctly identify potential high-risk loans.  The financial information was taken from a peer-to-peer lending services company. Using the value_counts function on the original data it analyzed about 77500 cases, with 2500 of them being high risk. The RandomOversampler module was also important to compare the original dataset to an overfitted model as well.  Using the classification_report_imbalanced function it was also able to determine the precision, recall and f1 score of the dataset, all important categories for determining the accuracy of the models.  The most important steps towards an accurate model were creating a model with the LogisticRegression function, training that model with model.fit, and making predictions using that fitted model with model.predict.

## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
  Balanced accuracy: .952
  Healthy Loan (0):
      * F1 Score: 1.0
      * Precision: 1.0
      * Recall: .99
  High-Risk (1):
      * F1 Score: .88
      * Precision: .85
      * Recall: .91

* Machine Learning Model 2: Overfitted data
  Balanced accuracy: .994
  Healthy Loan (0):
      * F1 Score: 1.0
      * Precision: 1.0
      * Recall: .99
  High-Risk (1):
      * F1 Score: .91
      * Precision: .84
      * Recall: .99

## Summary

In summary it would appear the best model to use would be with the overfitted data (Machine Learning Model 2) as it has a higher balanced accuracy of .994 compared to model 1's .952 accuracy, as well as being more accurate with the potential high-risk loan data with a similar precision while having a greater recall.  Also when looking at the harmonic mean (or the f1 score) it is higher as well, with a .91 score compared to model 1's .88 score, all while keeping greater or equal precision and recall scores.  Performance would matter more when looking at the high-risk row (or the 1's row) since that is the more important data to our problem.
