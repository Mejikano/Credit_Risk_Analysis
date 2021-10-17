# Credit_Risk_Analysis

Data source: Lending Club, 2019 Q1 Loands - LoanStats_2019Q1.csv
Software: Python 3

## Project Overview
The purpose of this analysis is to identify high credit risk loans from Lending Club a peer-to-peer lending services company, using multiple Machine Learning techniques to train many supervised models and compare statitical results for selecting the best performer predictive model. 


## Results


### Logistic Regression 

#### RandomOverSampler
Employing Random Oversampling technique, 

![RandomOverSampling](https://github.com/Mejikano/Credit_Risk_Analysis/blob/main/Resources/RandomOverSampling.png)


#### Synthetic Minority Oversampling Technique (SMOTE)

Employing SMOTE Oversampling technique, 

![SMOTE](https://github.com/Mejikano/Credit_Risk_Analysis/blob/main/Resources/SMOTE.png)

#### ClusterCentroids
Employing Cluster Centroids Undersampling technique, 

![ClusterCentroids](https://github.com/Mejikano/Credit_Risk_Analysis/blob/main/Resources/ClusterCentroids.png)
#### SMOTE and Edited Nearest Neighbors (SMOTEENN)
Employing combination of over and under sampling: SMOTE and Edited Nearest Neighbors technique, 

![SMOTEENN](https://github.com/Mejikano/Credit_Risk_Analysis/blob/main/Resources/SMOTEENN.png)

### Ensemble Learners

#### Balanced Random Forest Classifier
![BalancedRandomForestClassifier](https://github.com/Mejikano/Credit_Risk_Analysis/blob/main/Resources/BalancedRandomForestClassifier.png)


#### Easy Ensemble AdaBoost Classifier
![EasyEnsembleAdaBoostClassifier](https://github.com/Mejikano/Credit_Risk_Analysis/blob/main/Resources/EasyEnsembleAdaBoostClassifier.png)




## Summary



None of the models are recommended to predict high_risk credit loans given the presission metrics 






