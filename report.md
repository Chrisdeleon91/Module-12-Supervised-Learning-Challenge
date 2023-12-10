# Module-12-Supervised-Learning-Report 

## Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

* Explain the purpose of the analysis

The purpose is to address credit risk. Credit risk poses a classification problem that’s naturally imbalanced. The reason is that healthy loans easily outnumber risky loans. Using my knowledge of the imbalanced-learn library, I’ll use a logistic regression model to compare two versions of the dataset. First, I’ll use the original dataset. Second, I’ll resample the data by using the RandomOverSampler module from the imbalanced-learn library. For both cases, I’ll get the count of the target classes, train a logistic regression classifier, calculate the balanced accuracy score, generate a confusion matrix and generate a classification report. 

* Explain what financial information the data was on, and what you needed to predict.

Using historical lending activity as a dataset, I'll build a model that can identify the creditworthiness of borrowers. This will be accomplished using supervised learning. Supervised learning is the process of building machine learning models on already-known data.  I have a dataset containing loans along with information about these loans. People have defaulted (stopped paying) some of the loans. Fitting a machine learning model to this data is supervised learning—because I already have the answers about this dataset (whether each loan has defaulted). After I fit the model, the benefit of supervised learning is that I can use the model to make predictions about new data. That is, I can predict which loans in the future will be good or bad.
  
* Provide basic information about the variables you were trying to predict (e.g., `value_counts`).

I will check the balance of the labels variable (y, my target values) by using the value_counts function. 
Value_counts is a function in the Pandas library (commonly used for data analysis) that counts the occurrences of each unique value in a Series or DataFrame column. 
It provides a quick way to get a frequency table for your data.

* Describe the stages of the machine learning process you went through as part of this analysis.

I have created, trained, used and evaluated supervised classification models. The data used were spilt into training and testing sets, which will be used
with the Logistic Regression models I have created. The original dataset maintains the original class distribution, in which this imbalance can lead to biased models favoring the majority class and potentially misclassifying risk loans. A resampled dataset is used to artificially balance the number of "0" and "1" classes using techniques like RandomOverSampler, to ensure the model has sufficient data to learn and classify both classes effectively. 


* Briefly touch on any methods you used (e.g., `LogisticRegression`, or any resampling method).

A logistic regression model was created and the training data was fit into it. Predictions were used using the testing data and the balanced_accuracy_score function was used to print the score of the model. A confusion matrix and classification report were also generated for this model,

These steps were repeated, but with the resampled training dataset, by using the RandomOverSampler module. The resampled data had value_counts they there now equal to both "0" and "1" in this case, however. Predictions were created and the model's performance was again emulated by using the balanced_accuracy_score function, a confusion matrix and a classification report.

## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

### Machine Learning Model 1:
  * Description of Model 1 Accuracy, Precision, and Recall scores.
  *  
                           pre       rec       spe        f1       geo       iba       sup
                  0       1.00      0.99      0.91      1.00      0.95      0.91     18765
                  1       0.85      0.91      0.99      0.88      0.95      0.90       619
        avg / total       0.99      0.99      0.91      0.99      0.95      0.91     19384
     
*  Balanced Accuracy Score: 0.91
  
  Precision:
* Class "0": 1.00
* Class "1": 0.85

Recall:
* Class "0": 0.99
* Class "1": 0.91

### Machine Learning Model 2:
  * Description of Model 2 Accuracy, Precision, and Recall scores.
  * 

                         pre       rec       spe        f1       geo       iba       sup

                0       1.00      0.99      0.99      1.00      0.99      0.99     18765
                1       0.84      0.99      0.99      0.91      0.99      0.99       61
      avg / total       0.99      0.99      0.99      0.99      0.99      0.99     19384

* Balanced Accuracy Score: 0.99
  
Precision:

* Class "0": 1.00
* Class "1": 0.84
  
Recall:

* Class "0": 0.99
* Class "1": 0.99

Both models demonstrate high performance, with balanced accuracy scores exceeding 98%. However, the model trained on the resampled dataset performs slightly better, achieving a balanced accuracy score of 0.99 and balanced precision and recall scores. Model 2 performs slightly better with a higher Balanced Accuracy Score and recall for both classes. Model 1 has perfect precision for class "0", meaning all predicted healthy loans were actually healthy. Model 2 has slightly lower precision for class "1" compared to Model 1, indicating a higher chance of falsely classifying risky loans as healthy.

## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:
* Which one seems to perform best? How do you know it performs best?
* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )

Based on the analysis, the model trained on the resampled dataset is recommended due to its superior performance across all metrics. This suggests that addressing the class imbalance through resampling improves the model's ability to accurately predict both healthy and risky loans, which is crucial for credit risk management.

## Glossary

Let's break down the meaning of each column in a classification report for further clarification:

* pre: Precision (also known as positive predictive value) is the ratio of true positives to the sum of true positives and false positives. It measures the proportion of positive predictions that are actually correct.
* rec: Recall (also known as true positive rate or sensitivity) is the ratio of true positives to the sum of true positives and false negatives. It measures the proportion of actual positive cases that are correctly identified.
* spe: Specificity is the ratio of true negatives to the sum of true negatives and false positives. It measures the proportion of actual negative cases that are correctly identified.
* f1: F1 score is a harmonic mean of precision and recall, balancing their importance. It provides a single metric for evaluating classification performance, especially when dealing with imbalanced datasets.
* geo: Geometric mean is the geometric average of sensitivity and specificity. It provides an alternative metric to F1 score, particularly useful when dealing with imbalanced datasets.
* iba: Index balanced accuracy is a metric specifically designed for imbalanced datasets. It takes into account both sensitivity and specificity, penalizing classifiers that perform well on the majority class but poorly on the minority class.
* sup: Support is the total number of samples for each class. It provides information about the class distribution in the dataset.
