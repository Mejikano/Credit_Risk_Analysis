# Credit_Risk_Analysis

Data source: Lending Club, 2019 Q1 Loands - LoanStats_2019Q1.csv
Software: Python 3

## Project Overview
The purpose of this analysis is to identify high credit risk loans from Lending Club a peer-to-peer lending services company, using multiple Machine Learning techniques to train many supervised models and compare statitical results for selecting the best performer predictive model. 


## Results


### Logistic Regression 
A logistic regression model was created evaluating many sampling techniques to balance the loan dataset as  0.5% of the data were hihg_risk loans. 


#### RandomOverSampler
Employing Random Oversampling technique, below statistics show a very low precision 1% meaning that predicting high_risk loans will be very unlikely they are actual high_risk. Sensitivity stats are better than precision but 67% is not too a high number and f1 score is very bad.

![RandomOverSampling](https://github.com/Mejikano/Credit_Risk_Analysis/blob/main/Resources/RandomOverSampling.png)


#### Synthetic Minority Oversampling Technique (SMOTE)

Employing SMOTE Oversampling technique, precision 1% does not improve for high_risk loans and Sensitivity drops to 56% still f1 score is very bad.

![SMOTE](https://github.com/Mejikano/Credit_Risk_Analysis/blob/main/Resources/SMOTE.png)

#### ClusterCentroids
Employing Cluster Centroids Undersampling technique, this undersampling approach does not improve high_risk loans precision nor sensitivity and actually sensitivity for low_risk loans drops to 52% still f1 score is very bad.

![ClusterCentroids](https://github.com/Mejikano/Credit_Risk_Analysis/blob/main/Resources/ClusterCentroids.png)
#### SMOTE and Edited Nearest Neighbors (SMOTEENN)
Employing combination of over and under sampling: SMOTE and Edited Nearest Neighbors technique, precision 1% does not improve for high_risk loans but sensitivity does to 70% however f1 score is still too bad.

![SMOTEENN](https://github.com/Mejikano/Credit_Risk_Analysis/blob/main/Resources/SMOTEENN.png)

### Ensemble Learners

#### Balanced Random Forest Classifier
This model improved so well sensitivity for low_risk predictions however high_risk precision is still poor so predicted high_risk loans will be very likely to be low_risk; f1 score associated to high risk credits is to bad for a good perfomer model.

![BalancedRandomForestClassifier](https://github.com/Mejikano/Credit_Risk_Analysis/blob/main/Resources/BalancedRandomForestClassifier.png)


#### Easy Ensemble AdaBoost Classifier
This model is the best performer from all the previous ones it improved both high_risk and low_risk precision and sensitivity but high risk precision is still low (7%) and f1 score still bad. 

![EasyEnsembleAdaBoostClassifier](https://github.com/Mejikano/Credit_Risk_Analysis/blob/main/Resources/EasyEnsembleAdaBoostClassifier.png)




## Summary

As analyzed in previous results the precision is very poor for all the machine learning models ~0.01 to 0.07 which means that predicted high_risk loans most likely will not be high risk credits. Sensitivity is not well neither and f1 scores are generally very poor for all the models.

The Easy Ensemble AdaBoost Classifier maybe could work for a very conservative investor but given the statistics seems that most of the loans will be classified as high risk where they are not (7% of precision), hence what would be left for investment?

Based on the two previous statements, none of the models are recommended to predict high_risk credit loans given their performance. An exploratory analysis is recommended to identify outliers, high correlated features, and potentially the need of more than one quarter data (2019 Q1) for a comprehensive analysis.



