# Supervised Machine Learning - Predicting Credit Risk

In this project, I built a machine learning model that predicts whether a loan from LendingClub will become high risk or not. 

## Background

LendingClub is a peer-to-peer lending services company that allows individual investors to partially fund personal loans as well as buy and sell notes backing the loans on a secondary market. LendingClub offers their previous data through an API.

I used this data to create machine learning models to classify the risk level of given loans. Specifically, I compared the Logistic Regression model and Random Forest Classifier.

### Retrieve the data

Utilizing to .csv files in the resource file, I will be using data from 2019 to predict the credit risk of loans in the first quarter of 2020. 

* `2019loans.csv`
* `2020Q1loans.csv`

## Preprocessing: Convert categorical data to numeric

I created a training set from the 2019 loans using `pd.get_dummies()` to convert the categorical data to numeric columns. Similarly, create a testing set from the 2020 loans, also using `pd.get_dummies()`. The data structures in the .csv files were slightly different, so I used code in Jupyter Notebooks to make the dataframes similar so that the prediction model would work on both datasets.  

## Consider the models

After looking at the dataset and considering the two model types, I believe that the logistic regression model 
will perform better for this dataset.  Both Random Forest and Logistic Regression models are good for classification 
problems, but I believe with over 80 variables to consider, the Logistic model will win out.  Based on my research, 
Random Forest is recommended for simpler classification problems.

## Fit a LogisticRegression model and RandomForestClassifier model

Without scaling the data, the random forest classifier model is prodcuing the most accurate model at this point, defying my prediction.  

## Revisit the Preprocessing: Scale the data

Once I scaled the data, the logistic regression became the better classifier. It had an accuracy score of .66.  
The Random Forest model decreased in accuracy from .64 to .5.  From what I understand, this is to be expected as Random Forest modeling
doesn't rely on scaled data to make accurate calculations, while logistic regression models do.  

While I was able to produce a model with a .66 accuracy metric, I would be concerned about employing this out into the wild for credit 
worthiness rating purposes.  There is still far too much inaccuracy, in my opinion, and money would be lost on a consistent basis if 
loan decisions were based on this model.


### References

LendingClub (2019-2020) _Loan Stats_. Retrieved from: [https://resources.lendingclub.com/](https://resources.lendingclub.com/)

- - -

© 2021 Trilogy Education Services, a 2U, Inc. brand. All Rights Reserved.
