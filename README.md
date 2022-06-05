
# Supervised Machine Learning Homework - Predicting Credit Risk

## I uploaded my code and associated file to the following location on GitHub: 
    https://github.com/BZNUDS/Supervised-Machine-Learning

## My FINAL Jupyter Notebook can be found at the following location on GitHub: 
    https://github.com/BZNUDS/Supervised-Machine-Learning/blob/main/Credit_Risk_Evaluator_FINAL.ipynb

## My README.md file can be found at the following location on GitHub: 
    https://github.com/BZNUDS/Supervised-Machine-Learning/blob/main/README.md


In this assignment, I will be building a machine learning model that attempts to predict whether a loan from LendingClub will become high risk or not. 

## Background

LendingClub is a peer-to-peer lending services company that allows individual investors to partially fund personal loans as well as buy and sell notes backing the loans on a secondary market. LendingClub offers their previous data through an API.

I will be using this data to create machine learning models to classify the risk level of given loans. Specifically, you will be comparing the Logistic Regression model and Random Forest Classifier.


## Instructions

### Modified code provided and retrieved the data

In the `Generator` folder in `Resources`, I modified the GenerateData.ipynb notebook that was provided and created by own called
    GenerateData_Brian's_Version 
that will download data from LendingClub and output two CSVs: 

* `2019loans.csv`
* `2020Q1loans.csv`

I used the entire year's worth of data (2019) to predict the credit risk of loans from the first quarter of the next year (2020).

Note: these two CSVs have been undersampled to give an even number of high risk and low risk loans. In the original dataset, only 2.2% of loans are categorized as high risk. To get a truly accurate model, special techniques need to be used on imbalanced data. Undersampling is one of those techniques. Oversampling and SMOTE (Synthetic Minority Over-sampling Technique) are other techniques that are also used.


## Preprocessing: Convert categorical data to numeric

Then i created a training set from the 2019 loans using `pd.get_dummies()` to convert the categorical data to numeric columns. Similarly, create a testing set from the 2020 loans, also using `pd.get_dummies()`. Note! There are categories in the 2019 loans that do not exist in the testing set. If you fit a model to the training set and try to score it on the testing set as is, you will get an error. You need to use code to fill in the missing categories in the testing set. 

## Consider the models

I created and compared two models on this data: a logistic regression, and a random forests classifier. Before I created, fit, and scored the models, I made a prediction as to which model you think will perform better. According to the instructions, I do not need to be correct! I wrote down (in markdown cells in your Jupyter Notebook) my prediction, and provided justification for my educated guess. Wish me luck:)

## Fit a LogisticRegression model and RandomForestClassifier model

Created a LogisticRegression model, fit it to the data, and printed the model's score. Did the same for a RandomForestClassifier. Document which model performed better and how that compares to my prediction.

## Revisit the Preprocessing: Scale the data

The data going into these models was never scaled, an important step in preprocessing. So I used `StandardScaler` to scale the training and testing sets. Before re-fitting the LogisticRegression and RandomForestClassifier models on the scaled data, make another prediction about how you think scaling will affect the accuracy of the models. Write your predictions down and provide justification.

Fit and score the LogisticRegression and RandomForestClassifier models on the scaled data. How do the model scores compare to each other, and to the previous results on unscaled data? How does this compare to your prediction? Write down your results and thoughts.

## Rubric

[Unit 19 - Supervised Machine Learning Homework Rubric](https://docs.google.com/document/d/1f_eN3TYiGqlaWL9Utk5U-P491OeWqFSiv7FIlI_d4_U/edit?usp=sharing)

### References

LendingClub (2019-2020) _Loan Stats_. Retrieved from: [https://resources.lendingclub.com/](https://resources.lendingclub.com/)

© 2021 Trilogy Education Services, a 2U, Inc. brand. All Rights Reserved.


Based on the results, I felt me guess were faily accurate:)

If you have any questions, feel free to reach out.

Thank you,

Brian

P.S. I left more print statements in the code than usual just becasue i think it would really help the grader see the data for this assignment. As you can se from all of my past assignmenyts, I usually remove most of the print but I think these help the reader. 
