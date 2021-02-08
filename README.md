# Credit_Risk_Analysis

## Overview

We are assisting the data scientist at LendingClub to create a predictive model to predict credit risk for prospective clients for the peer-to-peer lending services company.

The following is an analysis of the balanced accuracy score and precision using six different algorithms trained to predict credit risk based on LendingClub credit data: 

* Oversampling using RandomOverSampler and SMOTE algorithms
* Undersampling using the ClusterCentroids algorithm, and SMOTEENN algorithm (over and undersampling).
* Two new machine learning models: BalancedRandomForestClassifier and EasyEnsembleClassifier, models that reduce bias to predict the credit risk. 

Recommendations will be made on which approach is the most effective!

## Results

### Oversampling
As shown below, oversampling demonstrates 0.66 balanced accuracy score, 0.60 recall, and 0.01 precision.

![](https://github.com/pimchanyachitsanga/Credit_Risk_Analysis/blob/main/Resources/oversampling.png)

### SMOTE
As shown below, SMOTE demonstrates 0.64 balanced accuracy score, 0.60 recall, and 0.01 precision.

![](https://github.com/pimchanyachitsanga/Credit_Risk_Analysis/blob/main/Resources/smote.png)

### Cluster Centroid Undersampling
As shown below, Cluster Centroid Undersampling demonstrates 0.41 balanced accuracy score, 0.63 recall, and 0.01 precision.

![](https://github.com/pimchanyachitsanga/Credit_Risk_Analysis/blob/main/Resources/undersampling.png)

### SMOTEENN
As shown below, SMOTEENN Undersampling demonstrates 0.54 balanced accuracy score, 0.69 recall, and 0.01 precision.

![](https://github.com/pimchanyachitsanga/Credit_Risk_Analysis/blob/main/Resources/smoteenn.png)

### Balanced Random Forest
As shown below, Balanced Random Forest demonstrates 0.78 balanced accuracy score, 0.69 recall, and 0.04 precision.

![](https://github.com/pimchanyachitsanga/Credit_Risk_Analysis/blob/main/Resources/balanced.png)

### EasyEnsemble
As shown below, EasyEnsemble demonstrates 0.93 balanced accuracy score, 0.91 recall, and 0.07 precision.
![](https://github.com/pimchanyachitsanga/Credit_Risk_Analysis/blob/main/Resources/esemble.png)

## Summary

Among all the models tested:
* Over/undersampling models and SMOTE and SMOTEENN performed similarly with balanced accuracy scores between 0.41 and 0.66. Start from the lowest accuracy score of 0.41 for Cluster Centroid Undersampling, 0.54 (SMOTEENN), 0.64 for SMOTE, and 0.66 for Random Oversampling. All of these models have a precision of 0.01 and recalls between 0.60 and 0.69. We would not recommend the top 4 models.
* The last two algorithms performed better in all metrics. EasyEnsemble has the best balanced accuracy score of 0.93 and a recall of 0.91. This indicates that 91% of "true" high risk loans would be identified while Balanced Random Forest has the second best balanced accuracy score of 0.78 and a recall of 0.6 which indicates that 78% of "true" high risk loans would be identified. Both also has more precision of 0.04 for Balanced Random Forest and 0.07 for EasyEnsemble.
* We would recommend EasyEnsemble algorithm to predict credit risk as this method outperformed others in all aspects.
