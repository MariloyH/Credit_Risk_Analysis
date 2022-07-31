# Credit_Risk_Analysis
BootCamp Week 17. Machine Learning 

#Overview
Credit risk is an inherently unbalanced classification problem, as good loans easily outnumber risky loans. Therefore, you’ll need to employ different techniques to train and evaluate models with unbalanced classes. Jill asks you to use imbalanced-learn and scikit-learn libraries to build and evaluate models using resampling.

Using the credit card credit dataset from LendingClub, a peer-to-peer lending services company, you’ll oversample the data using the RandomOverSampler and SMOTE algorithms, and undersample the data using the ClusterCentroids algorithm. Then, you’ll use a combinatorial approach of over- and undersampling using the SMOTEENN algorithm. Next, you’ll compare two new machine learning models that reduce bias, BalancedRandomForestClassifier and EasyEnsembleClassifier, to predict credit risk. Once you’re done, you’ll evaluate the performance of these models and make a written recommendation on whether they should be used to predict credit risk.
# Results
## Deliverable 1 
Using your knowledge of the imbalanced-learn and scikit-learn libraries, you’ll evaluate three machine learning models by using resampling to determine which is better at predicting credit risk. First, you’ll use the oversampling RandomOverSampler and SMOTE algorithms, and then you’ll use the undersampling ClusterCentroids algorithm. Using these algorithms, you’ll resample the dataset, view the count of the target classes, train a logistic regression classifier, calculate the balanced accuracy score, generate a confusion matrix, and generate a classification report.
<img width="824" alt="RANDOM " src="https://user-images.githubusercontent.com/102195803/182008449-f0c636aa-b0f8-4518-bca0-b676c7a85f2d.png">

<img width="821" alt="SMOTE" src="https://user-images.githubusercontent.com/102195803/182008451-42610ccd-5b0a-4192-970e-326070ca273e.png">

<img width="837" alt="ClusterCentroids" src="https://user-images.githubusercontent.com/102195803/182008453-7deda868-015e-47f8-bdad-f105f56797da.png">


## Deliverable 2


Using your knowledge of the imbalanced-learn and scikit-learn libraries, you’ll use a combinatorial approach of over- and undersampling with the SMOTEENN algorithm to determine if the results from the combinatorial approach are better at predicting credit risk than the resampling algorithms from Deliverable 1. Using the SMOTEENN algorithm, you’ll resample the dataset, view the count of the target classes, train a logistic regression classifier, calculate the balanced accuracy score, generate a confusion matrix, and generate a classification report.

<img width="826" alt="SMOTEENN" src="https://user-images.githubusercontent.com/102195803/182008445-d34ddc22-aa2d-43bf-8be1-ea068dc04972.png">


## Deliverable 3: Use Ensemble Classifiers to Predict Credit Risk (25 points)

Using your knowledge of the imblearn.ensemble library, you’ll train and compare two different ensemble classifiers, BalancedRandomForestClassifier and EasyEnsembleClassifier, to predict credit risk and evaluate each model. Using both algorithms, you’ll resample the dataset, view the count of the target classes, train the ensemble classifier, calculate the balanced accuracy score, generate a confusion matrix, and generate a classification report.

<img width="853" alt="BalancedRandomForest" src="https://user-images.githubusercontent.com/102195803/182008465-cf72a950-cfa2-4068-b137-6b7f7be48a39.png">

<img width="852" alt="AdaBoostClassifier" src="https://user-images.githubusercontent.com/102195803/182008480-08913bc4-2e4e-497e-a2ee-585989b67200.png">

# Summary

Deliverable 4 Instructions
For this deliverable, you’ll write a brief summary and analysis of the performance of all the machine learning models used in this Challenge.

The report should contain the following:

Overview of the analysis: Explain the purpose of this analysis.

Results: Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all six machine learning models. Use screenshots of your outputs to support your results.

Summary: Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. If you do not recommend any of the models, justify your reasoning.

Deliverable 4 Requirements
Structure, Organization, and Formatting (6 points)
The written analysis has the following structure, organization, and formatting:


There is a title, and there are multiple sections (2 pt)
Each section has a heading and subheading (2 pt)
Links to images are working, and code is formatted and displayed correctly (2 pt).
Analysis (24 points)
The written analysis has the following:

Overview of the loan prediction risk analysis:

The purpose of this analysis is well defined (4 pt)
Results:

There is a bulleted list that describes the balanced accuracy score and the precision and recall scores of all six machine learning models (15 pt)
Summary:

There is a summary of the results (2 pt)
There is a recommendation on which model to use, or there is no recommendation with a justification (3 pt)

