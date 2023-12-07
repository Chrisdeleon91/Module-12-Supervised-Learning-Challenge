# Module-12-Timed-Supervised-Learning-Challenge

In this assignment, I’ll use various techniques to train and evaluate models with imbalanced classes. I’ll use a dataset of historical lending activity froma peer-to-peer lending services company to build a model that can identify the creditworthiness of borrowers.
In this module, I’ll learn about supervised learning and how it can be used to build models on both balanced and imbalanced datasets.
Supervised learning is the process of building machine learning models on already-known data. For instance, suppose that I have a dataset containing loans along with information about these loans. People have defaulted (stopped paying) some of the loans. Fitting a machine learning model to this data is supervised learning—because I already have the answers about this dataset (whether each loan has defaulted). Once I fit the model, the benefit of supervised learning is that I can use the model to make predictions about new data. That is, I can predict which loans in the future will be good or bad.


Credit risk poses a classification problem that’s inherently imbalanced. The reason is that healthy loans easily outnumber risky loans. 
Using my knowledge of the imbalanced-learn library, I’ll use a logistic regression model to compare two versions of the dataset. First, I’ll use the original dataset. Second, I’ll resample the data by using the RandomOverSampler module from the imbalanced-learn library.
For both cases, I’ll get the count of the target classes, train a logistic regression classif er, calculate the balanced accuracy score, generate aconfusion matrix and generate a classification report.
As part of the README.md file in my GitHub repository, I’ll create a credit risk analysis report based on the provided template in my Starter_Code folder.

* Split the Data into Training and Testing Sets
* Create a Logistic Regression Model with the Original Data
* Predict a Logistic Regression Model with Resampled Training Data

## Instructions on how to use 

### 1. Launch credit_risk_resampling.ipynb from JuypterLab
* Run through each line of code to view the output
### 2. Open report-template.md in the repository
* view my credit risk analysis report

![Picture](https://www.columbia.edu/content/themes/custom/columbia/assets/img/cu-header.svg)


