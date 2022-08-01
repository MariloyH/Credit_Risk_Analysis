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

<img width="824" alt="RANDOM " src="https://user-images.githubusercontent.com/102195803/182008449-f0c636aa-b0f8-4518-bca0-b676c7a85f2d.png">
   
    - Balanced Accuracy 58.75%
    - Precision High Risk  1%
    - Recall High Risk 72%
    
    
### *SMOTE ALgorithm*
The synthetic minority oversampling technique (SMOTE), as the previuous the size of the minority is increased, but these new instances are interpolated. That is, for an instance from the minority class, a number of its closest neighbors is chosen. Based on the values of these neighbors, new values are created.

<img width="821" alt="SMOTE" src="https://user-images.githubusercontent.com/102195803/182008451-42610ccd-5b0a-4192-970e-326070ca273e.png">

    - Balanced Accuracy  69%
    - Precision High Risk  1%   Low Risk 100%
    - Recall High Risk   63%    Low Risk 69%

### *Cluster Centroids*
Cluster centroid undersampling is akin to SMOTE. The algorithm identifies clusters of the majority class, then generates synthetic data points, called centroids, that are representative of the clusters. The majority class is then undersampled down to the size of the minority class.

<img width="837" alt="ClusterCentroids" src="https://user-images.githubusercontent.com/102195803/182008453-7deda868-015e-47f8-bdad-f105f56797da.png">

    - Balanced Accuracy 39.81%
    - Precision High Risk  1%   Low Risk 100 %
    - Recall High Risk 69%      Low Risk 40%
    
    
## Deliverable 2
In this case, I used SMOTEENN, an approach to resampling that combines aspects of both oversampling and undersampling.
SMOTEENN combines the SMOTE and Edited Nearest Neighbors (ENN) algorithms. SMOTEENN is a two-step process:
    1.  Oversample the minority class with SMOTE.
    2.  Clean the resulting data with an undersampling strategy. If the two nearest neighbors of a data point belong to two different classes, that data point is dropped.
    
<img width="826" alt="SMOTEENN" src="https://user-images.githubusercontent.com/102195803/182008445-d34ddc22-aa2d-43bf-8be1-ea068dc04972.png">

    - Balanced Accuracy 57.05%
    - Precision High Risk  1%   Low Risk 100 %
    - Recall High Risk 71%      Low Risk 57%
    
## Deliverable 3: Use Ensemble Classifiers to Predict Credit Risk (25 points)
The concept of ensemble learning is the process of combining multiple models, like decision tree algorithms, to help improve the accuracy and robustness, as well as decrease variance of the model, and therefore increase the overall performance of the model. For this deliverable, I trained and compared two different ensemble classifiers, BalancedRandomForestClassifier and EasyEnsembleClassifier, to predict credit risk and evaluate each model. 

### *BALANCED RANDOM FOREST*
A random forest algorithm will sample the data and build several smaller, simpler decision trees. Each tree is simpler because it is built from a random subset of features:

<img width="853" alt="BalancedRandomForest" src="https://user-images.githubusercontent.com/102195803/182008465-cf72a950-cfa2-4068-b137-6b7f7be48a39.png">

    - Balanced Accuracy 87.31%
    - Precision High Risk  3%   Low Risk 100 %
    - Recall High Risk 70%      Low Risk 87%
  
### *ADAPTATIVE BOOSTING*
In Adaptive Boosting (or AdaBoost) a model is trained then evaluated. After evaluating the errors of the first model, another model is trained. This time, however, the model gives extra weight to the errors from the previous model. The purpose of this weighting is to minimize similar errors in subsequent models. Then, the errors from the second model are given extra weight for the third model. This process is repeated until the error rate is minimized

<img width="852" alt="AdaBoostClassifier" src="https://user-images.githubusercontent.com/102195803/182008480-08913bc4-2e4e-497e-a2ee-585989b67200.png">

    - Balanced Accuracy 94.24%
    - Precision High Risk  9%   Low Risk 100 %
    - Recall High Risk 92%      Low Risk 94%

# Summary
Before recomend a model, we must clarify what is what we want to detect if a future loan´s customer is high risk or not, our model will be the one that prevent the least amount of high risk loans pass through undetected. i. e. our model must be must sensitive or with a recall for high-risk high. For this reason, I wil recomend  *AdaBoost Ensemble Classifier* This model got a the highest balanced accuracy, the highest precision high risk and the highest Recall high risk.
 


