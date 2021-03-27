#Overview
This analysis applies machine learning to examine credit-card risk. The credit card credit dataset comes from LendingClub, a peer-to-peer lending services company. Inherently, the number of good loans surpasses the number of risky loans. This creates an unbalanced classification problem. To address this issue, the project employs different techniques that train and evaluate models with unbalanced classes. For example, imbalanced-learn and scikit-learn libraries build and appraise models using resampling. RandomOverSampler and SMOTE oversample the data. Contarily, a ClusterCentroids algorithm undersamples the data. Next, a SMOTEENN algorithm takes a combinatorial approach of both over and undersampling. Finally, two new machine learning models, BalancedRandomForestClassifier and EasyEnsembleClassifier, reduce bias and serve to predict credit risk.  
#Results
The accuracy and precisions scores vary among the six, maching learning models.
\
\
**1. Oversampling: Naive Random**
\
Balanced Accuracy Score: 54%
\
Precision: 100%
\
Recall: 57%
\
\
\
**2. Oversampling: SMOTE**
\
Balanced Accuracy Score: 52%
\
Precision: 100%
\
Recall: 52%
\
\
\
**3. Undersampling: ClusterCentroids**
\
Balanced Accuracy Score: 50%
\
Precision: 99%
\
Recall: 29%
\
\
\
**4. Combination (Over & Under) Sampling: SMOTEENN**
\
Balanced Accuracy Score: 54%
\
Precision: 100%
\
Recall: 76%
\
\
\
**5. Balanced Random Forest Classifier**
\
Balanced Accuracy Score: 90%
\
Precision: 4%
\
Recall: 64%
\
\
\
**6. Easy Ensemble Classifier**
\
Balanced Accuracy Score: 1%
\
Precision: 1%
\
Recall: 100%
\
\
\
#Summary

There is a summary of the results 
There is a recommendation on which model to use, or there is no recommendation with a justification 
