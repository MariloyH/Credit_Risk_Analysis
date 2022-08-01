# Credit_Risk_Analysis
BootCamp Week 17. Machine Learning 

# Overview

Personal loans are a highly demanded and profitable product in banking, but also with a high risk that people will not be able to pay their credits. That is why banks have demanded the creation of sophisticated algorithms using Machine Learning to evaluate applicants before granting a loan. These algorithms analyze various factors, such as age, education, and credit history, which can determine if you will be able to pay the credit.
In this challenge, we are going to use Supervised Machine Learning with Logistic Regression to analize wich one could help us predict credit risk. As the data is class imbalanced, first we will use 6 resampling methods to prepare the data before:

    1. Naive Random Oversampling
    2. SMOTE Oversampling
    3. Cluster Centroid Undersampling
    4. SMOTEENN Sampling
    5. Balanced Random Forest Classifying
    6. Easy Ensemble Classifying

# Results
## Deliverable 1 
First I used the oversampling RandomOverSampler and SMOTE algorithms, and the undersampling ClusterCentroids algorithm to resampled the data imbalanced. For each algorithm, I got the count of the target classes, trained a logistic regression classifier, calculated the balanced accuracy score, generated a confusion matrix, and generated  a classification report.

### *Random OverSampling*
In random oversampling, instances of the minority class are randomly selected and added to the training set until the majority and minority classes are balanced. Instances from the minority class are randomly selected and added to the minority class. 
<img width="650" alt="RANDOM" src="https://user-images.githubusercontent.com/102195803/182053591-891e5109-255b-4a54-976d-daa894bef7f5.png">
   
    - Balanced Accuracy 65.47%
    - Precision High Risk  1%       Low Risk 100%
    - Recall High Risk 72%          Low Risk 59%
    
    
### *SMOTE ALgorithm*
The synthetic minority oversampling technique (SMOTE), as the previuous the size of the minority is increased, but these new instances are interpolated. That is, for an instance from the minority class, a number of its closest neighbors is chosen. Based on the values of these neighbors, new values are created.

<img width="650" alt="SMOTE" src="https://user-images.githubusercontent.com/102195803/182053621-b8d0aec0-65b9-4c5b-b97f-df2cdeffca64.png">

    - Balanced Accuracy  66.2%
    - Precision High Risk  1%   Low Risk 100%
    - Recall High Risk   63%    Low Risk 69%

### *Cluster Centroids*
Cluster centroid undersampling is akin to SMOTE. The algorithm identifies clusters of the majority class, then generates synthetic data points, called centroids, that are representative of the clusters. The majority class is then undersampled down to the size of the minority class.

<img width="650" alt="ClusterCentroids" src="https://user-images.githubusercontent.com/102195803/182053656-73939b24-7ea1-4466-bcb8-913dae41494d.png">

    - Balanced Accuracy 54.47%
    - Precision High Risk  1%   Low Risk 100 %
    - Recall High Risk 69%      Low Risk 40%
    
    
## Deliverable 2
### SMOTEENN 
In this case, I usedSMOTEENN, an approach to resampling that combines aspects of both oversampling and undersampling.
SMOTEENN combines the SMOTE and Edited Nearest Neighbors (ENN) algorithms. SMOTEENN is a two-step process:
    1.  Oversample the minority class with SMOTE.
    2.  Clean the resulting data with an undersampling strategy. If the two nearest neighbors of a data point belong to two different classes, that data point is dropped.
    
<img width="650" alt="SMOTEENN" src="https://user-images.githubusercontent.com/102195803/182053735-3df9c555-dae6-4686-b498-be64c25d5b4f.png">

    - Balanced Accuracy 64.13%
    - Precision High Risk  1%   Low Risk 100 %
    - Recall High Risk 71%      Low Risk 57%
    
## Deliverable 3: Use Ensemble Classifiers to Predict Credit Risk (25 points)
The concept of ensemble learning is the process of combining multiple models, like decision tree algorithms, to help improve the accuracy and robustness, as well as decrease variance of the model, and therefore increase the overall performance of the model. For this deliverable, I trained and compared two different ensemble classifiers, BalancedRandomForestClassifier and EasyEnsembleClassifier, to predict credit risk and evaluate each model. 

### *BALANCED RANDOM FOREST*
A random forest algorithm will sample the data and build several smaller, simpler decision trees. Each tree is simpler because it is built from a random subset of features.

<img width="650" alt="BalancedRandomForest" src="https://user-images.githubusercontent.com/102195803/182053855-7b74147c-7a03-4d33-b3e3-4a5700870f45.png">

    - Balanced Accuracy 78.85%
    - Precision High Risk  3%   Low Risk 100 %
    - Recall High Risk 70%      Low Risk 87%
  
### *ADAPTATIVE BOOSTING*
In Adaptive Boosting (or AdaBoost) a model is trained then evaluated. After evaluating the errors of the first model, another model is trained. This time, however, the model gives extra weight to the errors from the previous model. The purpose of this weighting is to minimize similar errors in subsequent models. Then, the errors from the second model are given extra weight for the third model. This process is repeated until the error rate is minimized.

<img width="650" alt="AdaBoost" src="https://user-images.githubusercontent.com/102195803/182053801-5950846b-8a3b-4f4a-9c6e-4d3403143e99.png">

    - Balanced Accuracy 93.16%
    - Precision High Risk  9%   Low Risk 100 %
    - Recall High Risk 92%      Low Risk 94%

# Summary
Before recomend a model, we must clarify what is what we want to detect if a future loan´s customer is high risk or not, our model will be the one that prevent the least amount of high risk loans pass through undetected. i. e. our model must be must sensitive or with a recall for high-risk high. For this reason, I wil recomend  *AdaBoost Ensemble Classifier* This model got a the highest balanced accuracy, the highest precision high risk and the highest Recall high risk.
 


