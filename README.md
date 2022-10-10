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

In the Cluster Centroid algorithm, under-sampling is used. Clusters of the majority class are identified and synthetic data points are generated. The majority class is then under-sampled to the size of the minority class. A logistic regression model was used the with the resampled data.

- **Accuracy Score:** .54
- **Precision Score:** .01
- **Recall:** .69

### SMOTEENN

![SMOTEENN](/Resources/SMOTEENN.PNG)

In the SMOTEENN algorithm, over and under-sampling is used. The minority class is first over-sampled with SMOTE, and then the resulting data is cleaned with an undersampling strategy until balanced. A logistic regression model was used with the resampled data.

- **Accuracy Score:** .67
- **Precision Score:** .01
- **Recall:** .73

### Balanced Random Forest Classifier

![Balanced Random Forest Classifier](/Resources/balanced_random_forest_classifier.PNG)

The Balanced Random Forest Classifier randomly under-samples the dataset when bootstrapping from the training dataset. Each tree in the forest is provided with a balanced bootstrap sample. the base train_test_split data was used in this model. 

- **Accuracy Score:** .78
- **Precision Score:** .03
- **Recall:** .70

### Easy Ensemble AdaBoost Classifier

![Easy Ensemble Classifier](/Resources/easyensemble.PNG)

The Easy Ensemble Classifier is an ensemble of AdaBoost learners trained on different balanced bootstrap samples. Balancing is achieved by random under-sampling. The base train_test_split data was used in this model.

- **Accuracy Score:** .92
- **Precision Score:** .09
- **Recall:** .92

## Summary

When looking at all of the models, the Easy Ensemble Classifier performs the best. All three scores were higher then the previous models at predicting high risk. While the precision is still very low, it had a recall of 92%, meaning it predicted 92% of the high risk data correctly. The 9% percision of the model means that only 9% of the high risk predictions were actually high risk. I would recommend the model is used to initially detect high risk customers, and then additional research to correctly determine the correct risk level.