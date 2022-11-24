# Credit_Risk_Analysis

## Overview:
Credit risk is an inherently unbalanced classification problem, as good loans easily outnumber risky loans. Therefore, you’ll need to employ different techniques to train and evaluate models with unbalanced classes. Jill asks you to use imbalanced-learn and scikit-learn libraries to build and evaluate models using resampling.

Using the credit card credit dataset from LendingClub, a peer-to-peer lending services company, you’ll oversample the data using the RandomOverSampler and SMOTE algorithms, and undersample the data using the ClusterCentroids algorithm. Then, you’ll use a combinatorial approach of over- and undersampling using the SMOTEENN algorithm. Next, you’ll compare two new machine learning models that reduce bias, BalancedRandomForestClassifier and EasyEnsembleClassifier, to predict credit risk. Once you’re done, you’ll evaluate the performance of these models and make a written recommendation on whether they should be used to predict credit risk.

### Resources
Software: Python 3.9, Anaconda NAvigator 1.9.12, Conda 4.8.4, Jupyter Notebook 6.0.3

## Results
### Random Over Sample model

![Screenshot_20221123_105637](https://user-images.githubusercontent.com/107443962/203714939-3ea45c65-42e6-49b3-b543-bd651ff74e29.png)

![Screenshot_20221123_105648](https://user-images.githubusercontent.com/107443962/203714977-a330d730-451e-4db2-b678-834654fa7b48.png)

![Screenshot_20221123_105701](https://user-images.githubusercontent.com/107443962/203714991-68cd503d-9e26-486b-94ed-7e2bfaaf8b60.png)

The balanced accuracy score is 64%. When we look at the classification report the precision at the high risk is low at 1% while low risk precision is at 100%. The F1 score for high risk is 2% while the F1 score for low risk is 81%.

### SMOTE model

![Screenshot_20221123_105934](https://user-images.githubusercontent.com/107443962/203715309-69a299ee-bcda-4205-828c-98276a5e84aa.png)

The balanced accuracy score is 62%. Similar to the random over samole model the low risk precision is 100%, while high risk is only 2%.

### ClusterCentroidsModel

![Screenshot_20221123_105934](https://user-images.githubusercontent.com/107443962/203715489-88626663-e2a5-4f32-b39a-d0ed17fafe93.png)

The blalanced accuracy score is at 52%. The F1 score for low risk is at 60% and for high risk it is at 1%.

### SMOTEEN model

![Screenshot_20221123_105934](https://user-images.githubusercontent.com/107443962/203717324-2e86e27a-d7b9-43e2-b083-a2145e23fcda.png)

As we take a look at the classification report for the BalancedRandomForest we see an increase in the F1 score for both low risk and high. Still high risk score is still low their is improvement with this model.

### EasyEnsembleClassifier

![Screenshot_20221123_111256](https://user-images.githubusercontent.com/107443962/203717512-e643b4f0-72d0-4dc0-ae25-e479f0d07c35.png)

As you an see in this classification report we were able to get even more of an icrease for the F1 score for low risk and high risk!

### Summary
None of the models were able to show strong F1 scores for high risk resulting in precision and sensitivity combined being weak. The best omodel of all with what we had to work with was the EnsembleClassifier. With that being said I would recommend we find a differnet model that will help result in both high F1 scores for both high and low risk. Also try finding another dataset to work on as well.
