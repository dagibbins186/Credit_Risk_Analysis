# Overview
This analysis applies machine learning to examine credit-card risk. The credit card credit dataset comes from LendingClub, a peer-to-peer lending services company. Inherently, the number of good loans surpasses the number of risky loans. This creates an unbalanced classification problem. To address this issue, the project employs different techniques that train and evaluate models with unbalanced classes. For example, imbalanced-learn and scikit-learn libraries build and appraise models using resampling. RandomOverSampler and SMOTE oversample the data. Contarily, a ClusterCentroids algorithm undersamples the data. Next, a SMOTEENN algorithm takes a combinatorial approach of both over and undersampling. Finally, two new machine learning models, BalancedRandomForestClassifier and EasyEnsembleClassifier, reduce bias and serve to predict credit risk.  
# Results
The accuracy and precisions scores vary among the six, maching learning models.
\
\
**1. Oversampling: Naive Random**
\
Confusion Matrix:
|              | Predicted True | Predicted False |
|--------------|----------------|-----------------|
|Actually True | 9789           | 7329            |
|Actually False| 43             | 44              |

\
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
Confusion Matrix:
|              | Predicted True | Predicted False |
|--------------|----------------|-----------------|
|Actually True | 8824           | 8294            |
|Actually False| 42             | 45              |

\
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
Confusion Matrix:
|              | Predicted True | Predicted False |
|--------------|----------------|-----------------|
|Actually True | 4933           | 12185           |
|Actually False| 25             | 62              |

\
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
Confusion Matrix:
|              | Predicted True | Predicted False |
|--------------|----------------|-----------------|
|Actually True | 13068          | 4050            |
|Actually False| 60             | 27              |

\
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
Confusion Matrix:
|              | Predicted True | Predicted False |
|--------------|----------------|-----------------|
|Actually True | 65             | 36              |
|Actually False| 1692           | 15412           |

\
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
Confusion Matrix:
|              | Predicted True | Predicted False |
|--------------|----------------|-----------------|
|Actually True | 65             | 36              |
|Actually False| 1692           | 15412           |

\
\
Balanced Accuracy Score: 1%
\
Precision: 1%
\
Recall: 100%
\
\

# Summary
There are situations in which high recall, also known as sensitivity, is more important than precision. With credit-card risk screening, for example, a high sensitivity is more important than high precision. High sensitivity means that among people who actually have credit-card risk, most of them will be predicted correctly. High precision, on the other hand, means that if the test comes back positive, there's a high likelihood that the person has credit-card risk. It's better to detect everyone who might have credit card risk, even if it means a certain number of false positives, than to miss people who do have credit card risk. After all, those with a positive result for credit card can undergo further testing to confirm or rule out credit card risk. The false positives in a highly sensitive test are accepted as a cost of doing business. 
\
\
Models 1 through 4 have high precision. On the other hand, Models 5 and 6 have high sensitivity. Therefore, models 5 and 6 are the best to use in this scenario. Models 5 and 6 show highly sensitive tests and an aggressive algorthm. They do a good job of detecting the intended targets. Unfortunately, there is also risk of false positives. Conversely, Models 1 through 4 demonstrate a conservative process. The predicted positives are likely true positives. The flip side is that a number of other true positives may not be predicted. If we are choosing models from the perspective of the lender, then Models 5 and 6 are the best bets.
