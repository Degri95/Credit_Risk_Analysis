# Credit_Risk_Analysis
Analyzing machine learning models with Python to predict credit risk.

## Overview

In this project sampling algorithims and supervised machine learning models were applied to credit card data to predict credit risk. Since credit risk is inherently unbalanced, resampling algorithms and machine learning models that reduce bias are used. After our models have been fitted and tested, a recommendation will be made on whether they should be used to predict credit risk. The dataset being used contains credit card stats from LendingClub in Q1 of 2019. Six different algorithms were used in the analysis.

## Results

### Naive Random Oversampling

![Naive Random Oversampling](/Resources/naive_random_oversampling.PNG)

In the Naive Random Oversampling algorithm, instances of the minority class (high risk) are randomly selected and added to the training set until both classes are balanced. A logistic regression model was used with the resampled data.

- **Accuracy Score:** .64
- **Precision Score:** .01
- **Recall:** .72

### SMOTE Oversampling

![SMOTE Oversampling](/Resources/SMOTE_oversampling.PNG)

In the SMOTE Oversampling algorithm, new instances of minority class are interpolated based on values of neighboring data until both classes are balanced. A logistic regression model was used with the resampled data.

- **Accuracy Score:** .66
- **Precision Score:** .01
- **Recall:** .62

### Cluster Centroids

![Cluster Centroids](/Resources/clustercentroids.PNG)

In the Cluster Centroid algorithm, undersampling is used. Clusters of the majority class are identified and synthetic data points are generated. The majority class is then undersampled to the size of the minority class. A logistic regression model was used the with the resampled data.

- **Accuracy Score:** .54
- **Precision Score:** .01
- **Recall:** .69

### SMOTEENN

![SMOTEENN](/Resources/SMOTEENN.PNG)

In the SMOTEENN algorithm, over and undersampling is used. The minority class is first oversampled with SMOTE, and then the resulting data is cleaned with an undersampling stategy until balanced. A logistic regression model was used with the resampled data.

- **Accuracy Score:** .67
- **Precision Score:** .01
- **Recall:** .73

### Balanced Random Forest Classifier

![Balanced Random Forest Classifier](/Resources/balanced_random_forest_classifier.PNG)

### Easy Ensemble AdaBoost Classifier

![Easy Ensemble Classifier](/Resources/easyensemble.PNG)
 