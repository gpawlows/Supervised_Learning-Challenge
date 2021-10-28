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

You will be creating and comparing two models on this data: a logistic regression, and a random forests classifier. Before you create, fit, and score the models, make a prediction as to which model you think will perform better. You do not need to be correct! Write down (in markdown cells in your Jupyter Notebook or in a separate document) your prediction, and provide justification for your educated guess.

## Fit a LogisticRegression model and RandomForestClassifier model

Create a LogisticRegression model, fit it to the data, and print the model's score. Do the same for a RandomForestClassifier. You may choose any starting hyperparameters you like. Which model performed better? How does that compare to your prediction? Write down your results and thoughts.

## Revisit the Preprocessing: Scale the data

The data going into these models was never scaled, an important step in preprocessing. Use `StandardScaler` to scale the training and testing sets. Before re-fitting the LogisticRegression and RandomForestClassifier models on the scaled data, make another prediction about how you think scaling will affect the accuracy of the models. Write your predictions down and provide justification.

Fit and score the LogisticRegression and RandomForestClassifier models on the scaled data. How do the model scores compare to each other, and to the previous results on unscaled data? How does this compare to your prediction? Write down your results and thoughts.

## Rubric

[Unit 19 - Supervised Machine Learning Homework Rubric](https://docs.google.com/document/d/1f_eN3TYiGqlaWL9Utk5U-P491OeWqFSiv7FIlI_d4_U/edit?usp=sharing)

### References

LendingClub (2019-2020) _Loan Stats_. Retrieved from: [https://resources.lendingclub.com/](https://resources.lendingclub.com/)

- - -

© 2021 Trilogy Education Services, a 2U, Inc. brand. All Rights Reserved.
