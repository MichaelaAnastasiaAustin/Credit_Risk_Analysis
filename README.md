# Credit_Risk_Analysis

## Overview

Credit risk is an inherently unbalanced classification problem, as good loans significantly outnumber risky loans. The purpose of this analysis was to employ different techniques to train and evaluate models with unbalanced classes. Specifically, we oversampled the data using the RandomOverSampler and SMOTE algorithms, and undersampled the data using the ClusterCentroids algorithm. We also employed a combinatorial approach of over- and undersampling using the SMOTEENN algorithm. Finally, we compared two new machine learning models that reduce bias, BalancedRandomForestClassifier and EasyEnsembleClassifier, to predict credit risk. 

## Resources
- Data Source: LoanStats_2019Q1.csv
- Software: Python, Jupyter Notebooks


## Results

To evaluate the performance of the six machine learning models, we compared the balanced accuracy, precision, and recall scores of each model:

Naive Random Oversampling
![naive](https://github.com/MichaelaAnastasiaAustin/Credit_Risk_Analysis/blob/main/images/naive.png)

- balanced accuracy: 0.6533977140416822
- precision: high-risk is 0.01, low-risk is 1.00
- recall: high-risk is 0.63, low-risk is 0.67

SMOTE Oversampling
![smote](https://github.com/MichaelaAnastasiaAustin/Credit_Risk_Analysis/blob/main/images/SMOTE.png)

- balanced accuracy: 0.6512291961274883
- precision: high-risk is 0.01, low-risk is 1.00
- recall: high-risk is 0.64, low-risk is 0.66

Undersampling
![under](https://github.com/MichaelaAnastasiaAustin/Credit_Risk_Analysis/blob/main/images/under.png)

- balanced accuracy: 0.6512291961274883
- precision: high-risk is 0.01, low-risk is 1.00
- recall: high-risk is 0.59, low-risk is 0.43

Combination Under-Over Sampling
![combination](https://github.com/MichaelaAnastasiaAustin/Credit_Risk_Analysis/blob/main/images/combination.png)

- balanced accuracy: 0.5103017191018931
- precision: high-risk is 0.01, low-risk is 1.00
- recall: high-risk is 0.70, low-risk is 0.58

Balanced Random Forest Classifier
![forest](https://github.com/MichaelaAnastasiaAustin/Credit_Risk_Analysis/blob/main/images/forest.png)

- balanced accuracy: 0.7877672625306695
- precision: high-risk is 0.04, low-risk is 1.00
- recall: high-risk is 0.67, low-risk is 0.91

Easy Ensemble AdaBoost Classifier
![adaboost](https://github.com/MichaelaAnastasiaAustin/Credit_Risk_Analysis/blob/main/images/AdaBoost.png)

- balanced accuracy: 0.925427358175101
- precision: high-risk is 0.07, low-risk is 1.00
- recall: high-risk is 0.91, low-risk is 0.94

0.0637/.98


## Summary 
All in all, the Easy Ensemble AdaBoost Classifier has the highest balanced accuracy score -- 92.5%. Along with an accuracy rate that is significantly higher than the other models, it's recall rate is high. For high-risk credits, the Easy Ensemble AdaBoost Classifier has a recall of 91%. However, the model's precision rate for high-risk credit is only 7%. This means that it detects nearly all high-risk credit, but falsely detects many low-risk credits as high-risk. Furthermore, the model's F-score for high-risk credit is 0.13. For these reasons, I would not advise the bank to use any of the machine learning models.