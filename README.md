# Credit_Risk_Analysis

## Analysis Overview
credit risks are actions that reduce your credit score. These actions include access dept, history, etc. To help predict credit risk, we used several machine learning models.
Through the use of python tools were able to run multiple models,
- oversample the data using the RandomOverSampler and SMOTE algorithms.
- Undersample the data using the ClusterCentroids algorithm.
- Over- and undersampling using the SMOTEENN algorithm.
- Compare two machine learning models that decrease biases, BalancedRandomForestClassifier and EasyEnsembleClassifier.
Through the use of multiple machine learning models, we will be able to best determine the model for predicting credit risk.

## Results 
### (Balanced Accuracy Scores, Confusion Matrixes and Imbalanced Classification Reports)
#### RandomOverSampler model

![diliv1.1](https://github.com/Iffadanwar/Credit_Risk_Analysis/blob/main/Module-17-Challenge-Resources/image/diliv_1.1.png)

- balanced accuracy score = 63%
- high_risk precision is about 1%, with 62% sensitivity
- F1 = 2%
- Due to the high number of the low_risk population, its precision is almost 100% with a sensitivity of 68%.

### SMOTE model

![diliv2.1](https://github.com/Iffadanwar/Credit_Risk_Analysis/blob/main/Module-17-Challenge-Resources/image/diliv_2.1.png)

- similar to previous model
- balanced accuracy score = 63%
- high_risk precision is about 1%, with 62% sensitivity
- F1 = 2%
- Due to the high number of the low_risk population, its precision is almost 100% with a sensitivity of 63%.

### ClusterCentroids model

![diliv2.2](https://github.com/Iffadanwar/Credit_Risk_Analysis/blob/main/Module-17-Challenge-Resources/image/diliv_2.2.png)

- balanced accuracy score has decreased to about 52%.
- high_risk precision is about 1%, with 60% sensitivity
- F1 = 2%
- Due to the high number of false positives, the low_risk sensitivity is only 44%.

### SMOTEENN model

![diliv2.3](https://github.com/Iffadanwar/Credit_Risk_Analysis/blob/main/Module-17-Challenge-Resources/image/diliv_2.3.png)

- balanced accuracy score has incresed to about 62%.
- high_risk precision is about 1%, with 70% sensitivity
- F1 = 2%
- Due to the high number of false positives, the low_risk sensitivity is 54%.

### BalancedRandomForestClassifier model

![diliv3.1](https://github.com/Iffadanwar/Credit_Risk_Analysis/blob/main/Module-17-Challenge-Resources/image/diliv_3.1.png)

- balanced accuracy score has incresed to about 79%.
- high_risk precision is about 4%, with 67% sensitivity
- F1 = 6%
- Due to a lower number of false positives, the low_risk sensitivity is now 91% with 100% presicion.

## EasyEnsembleClassifier model

![diliv3.2](https://github.com/Iffadanwar/Credit_Risk_Analysis/blob/main/Module-17-Challenge-Resources/image/diliv_3.2.png)

- balanced accuracy score has decreased to about 93%.
- high_risk precision is about 7%, with 91% sensitivity
- F1 = 14%
- Due to a lower number of false positives, the low_risk sensitivity is now 94% with 100% presicion.

## Summary
All the models we tested show weak precision to guess if the credit risk is high. The EasyEnsembleClassifier model was an improvement especially on the sensitivity of values at high risk credits. It detects 93% of all high risk credit. However, the model has low precision so low risk credit run a high statistical risk of being detected as high risk credit. This would penalize the bank's credit strategy and infer on its revenue by missing those business opportunities.

the would personally recommend the bank not use any of these models specifically due to the prercision being low. A more robust model must be implemented
