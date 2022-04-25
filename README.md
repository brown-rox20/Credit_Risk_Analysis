# Credit_Risk_Analysis

## Overview

### Purpose

Create and recommend machine learning models to predict credit risk using data provided by LendingClub.

## Results

- Oversampling using `RandomOverSampler` gives a balanced accuracy score of 0.67:
- <img src="https://github.com/brown-rox20/Credit_Risk_Analysis/blob/main/assets/images/01_RandomOverSampler.png">

The precision being 0.01 with a recall of 0.74:
<img src="https://github.com/brown-rox20/Credit_Risk_Analysis/blob/main/assets/images/02_precision_and_recall.png">

- Oversampling using `SMOTE` gives a balanced accuracy score of 0.66:
  <img src="https://github.com/brown-rox20/Credit_Risk_Analysis/blob/main/assets/images/03_smote.png">

The precision being 0.01 with a recall of 0.63:
<img src="https://github.com/brown-rox20/Credit_Risk_Analysis/blob/main/assets/images/04_precision_and_recall.png">

- Undersampling using `ClusterCentroids` gives a balanced accuracy score of 0.54:
  <img src="https://github.com/brown-rox20/Credit_Risk_Analysis/blob/main/assets/images/05_ClusterCentroids.png">

The precision being 0.01 with a recall of 0.69:
<img src="https://github.com/brown-rox20/Credit_Risk_Analysis/blob/main/assets/images/06_precision_and_recall.png">

- Over and Undersampling using `SMOTEENN` gives a balanced accuracy score of 0.66:
  <img src="https://github.com/brown-rox20/Credit_Risk_Analysis/blob/main/assets/images/07_SMOTEENN.png">

The precision being 0.01 with a recall of 0.73:
<img src="https://github.com/brown-rox20/Credit_Risk_Analysis/blob/main/assets/images/08_precision_and_recall.png">

- Ensemble classification with BalancedRandomForestClassifier gives a balanced accuracy score of 0.79:
  <img src="https://github.com/brown-rox20/Credit_Risk_Analysis/blob/main/assets/images/09_BalancedRandomForestClassifier.png">

The precision being 0.03 with a recall of 0.70:
<img src="https://github.com/brown-rox20/Credit_Risk_Analysis/blob/main/assets/images/10_precision_and_recall.png">

- Ensemble classification with EasyEnsembleClassifier gives a balanced accuracy score of 0.93:
  <img src="https://github.com/brown-rox20/Credit_Risk_Analysis/blob/main/assets/images/11_EasyEnsembleClassifier.png">

The precision being 0.09 with a recall of 0.92:
<img src="https://github.com/brown-rox20/Credit_Risk_Analysis/blob/main/assets/images/12_precision_and_recall.png">

## Summary

Unfortunately the machine learning models used here are poor in predicting high credit risk. The `EasyEnsembleClassifier` model was the best at predicting risk, identifying high risk applications with a recall of 0.92. However, the precision was at a low 0.09, meaning it would only correctly predict 9% of high risk applications.

### Recommendation

Due to the fact that the best we could do is a low precision rate of 0.09 for predicting high risk applications, when a majority are likely low risk, I would not recommend any of these models. The bank would lose a lot of potential profit by following this model.
