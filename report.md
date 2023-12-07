# Module-12-Supervised-Learning-Report 

## Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

* Explain the purpose of the analysis

The purpose is to address credit risk. Credit risk poses a classification problem that’s naturally imbalanced. The reason is that healthy loans easily outnumber risky loans. Using my knowledge of the imbalanced-learn library, I’ll use a logistic regression model to compare two versions of the dataset. First, I’ll use the original dataset. Second, I’ll resample the data by using the RandomOverSampler module from the imbalanced-learn library. For both cases, I’ll get the count of the target classes, train a logistic regression classifer, calculate the balanced accuracy score, generate a confusion matrix and generate a classification report. 

* Explain what financial information the data was on, and what you needed to predict.

Using historical lending activity as a dataset, I'll build a model that can identify the creditworthiness of borrowers. This will be accomplished using supervised learning. Supervised learning is the process of building machine learning models on already-known data.  I have a dataset containing loans along with information about these loans. People have defaulted (stopped paying) some of the loans. Fitting a machine learning model to this data is supervised learning—because I already have the answers about this dataset (whether each loan has defaulted). After I fit the model, the benefit of supervised learning is that I can use the model to make predictions about new data. That is, I can predict which loans in the future will be good or bad.
  
* Provide basic information about the variables you were trying to predict (e.g., `value_counts`).
* Describe the stages of the machine learning process you went through as part of this analysis.
* Briefly touch on any methods you used (e.g., `LogisticRegression`, or any resampling method).

## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
  * Description of Model 1 Accuracy, Precision, and Recall scores.



* Machine Learning Model 2:
  * Description of Model 2 Accuracy, Precision, and Recall scores.

## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:
* Which one seems to perform best? How do you know it performs best?
* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )

If you do not recommend any of the models, please justify your reasoning.
