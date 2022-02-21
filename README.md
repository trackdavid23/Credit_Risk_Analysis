# Credit_Risk_Analysis

## Analysis Overview
In this project, we use Python to build and evaluate several machine learning models to predict credit risk.
We adopted the following procedure:
* Oversample the data using the RandomOverSampler and SMOTE algorithms.
* Undersample the data using the ClusterCentroids algorithm.
* Use a combinatorial approach of over- and undersampling using the SMOTEENN algorithm.
* Compare two machine learning models that reduce bias, BalancedRandomForestClassifier and EasyEnsembleClassifier.
* We will evaluate the performance of these models and make a recommendation on whether they should be used to predict credit risk.

## Results (Balanced Accuracy Scores, Confusion Matrixes and Imbalanced Classification Reports)

### RandomOverSampler model![Uploading Screen Shot 2022-02-21 at 5.17.03 PM.png…]()
![Screen Shot 2022-02-21 at 5 19 48 PM](https://user-images.githubusercontent.com/59430635/155032682-86a3c873-8f35-4bad-a7ed-7d8f09b0d61d.png)


![Screen Shot 2022-02-21 at 5 13 27 PM](https://user-images.githubusercontent.com/59430635/155032170-ca8e382b-ab8e-419f-8a2f-880a1cc3e245.png)

The balanced accuracy score is 65%.
The high_risk precision is about 1% only with 62% sensitivity which makes a F1 of 2% only.
Due to the high number of the low_risk population, its precision is almost 100% with a sensitivity of 68%.

### SMOTE model
![Screen Shot 2022-02-21 at 5 21 30 PM](https://user-images.githubusercontent.com/59430635/155032807-d4c227ab-0fba-4c8e-b676-83155e8d2d15.png)

*The results are pretty similar to the previous model.
*The balanced accuracy score is 64%.
*The high_risk precision is about 1% only with 63% sensitivity which makes a F1 of 2% only.
*Due to the high number of the low_risk population, its precision is almost 100% with a sensitivity of 66%.

### ClusterCentroids model
![Screen Shot 2022-02-21 at 5 24 20 PM](https://user-images.githubusercontent.com/59430635/155033028-14466801-10ca-4494-8c61-2822e2ace8c4.png)


Here the balanced accuracy score is down to about 52%.
The high_risk precision is still 1% only with 63% sensitivity which makes a F1 of 1%.
Due to the high number of false positives, the low_risk sensitivity is only 40%.


# Summary
## All the models used to perform the credit risk analysis show weak precision in determining if a credit risk is high.
The Ensemble models brought a lot more improvment specially on the sensitivity of the high risk credits.
The EasyEnsembleClassifier model shows a recall of 92% so it detects almost all high risk credit. On another hand, with a low precision, a lot of low risk credits are still falsely detected as high risk which would penalize the bank's credit strategy and infer on its revenue by missing those business opportunities.
For those reasons I would not recommend the bank to use any of these models to predict credit risk.

