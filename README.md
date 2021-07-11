# Credit_Risk_Analysis

# Project Overview
Using a credit card credit dataset from LendingClub, a peer-to-peer lending services company, the objective of this project was to assess the credit worthiness of applicants by applying machine learning to credit card risk analysis. Since credit risk is an inherently unbalanced classification problem, as good loans easily outnumber risky loans, the scope of the project entailed employing different techniques to train and evaluate models with unbalanced classes using the imbalanced-learn and scikit-learn libraries to build and evaluate models using resampling.

## Project Scope
The analysis involved the following process:

1) Oversample the data using the RandomOverSampler and SMOTE algorithms.
2) Undersample the data using the ClusterCentroids algorithm.
3) Use a combinatorial approach of over and undersampling using the SMOTEENN algorithm.
4) Compare two new machine learning models that reduce bias, BalancedRandomForestClassifier and EasyEnsembleClassifier, to predict credit risk.
5) Finally, evaluate the performance of these models using balanced accuracy, precision, and recall (sensitivity) scores.



## Technologies
Jupyter Notebook, Python, Pandas DataFrame, imbalanced-learn package and libraries including NumPy, version 1.11 or later, SciPy, version 0.17 or later, and Scikit-learn, version 0.21 or later, and six machine learning models. A machine learning environment was also set up with accompanying Anaconda packages.



# Results 
## Balanced Accuracy Scores, Confusion Matrixes and Imbalanced Classification Reports For Credit Resampling and Ensemble Machine Learning

Note - While the term recall is more commonly used in machine learning, the two terms are synonymous and will be used interchangeably in this report.


## Oversampling with RandomOverSamper Model

Oversampling_RandomOverSampler.png![Oversampling_RandomOverSampler](https://user-images.githubusercontent.com/80140082/124972911-bf975880-dfdf-11eb-81af-edd90318471d.png)

* The balanced accuracy score is 65%.
* The high_risk precision is 1% with 61% sensitivity which makes a F1 score of 2%.
* The precision for the low_risk population is 100% with a sensitivity of 68%. 


## Oversampling with SMOTE Model

Oversampling_SMOTE.png![Oversampling_SMOTE](https://user-images.githubusercontent.com/80140082/124973262-287ed080-dfe0-11eb-92d3-25903ea4cb92.png)

* The SMOTE model results are similar to the previous RandomOverSampler model.
* The balanced accuracy score is 62%.
* The high_risk precision is 1% with 64% sensitivity which makes a F1 score of 2%.
* The precision for the low_risk population is 100% with a sensitivity of 64%.


## Undersampling with ClusterCentroids Model

Undersampling_ClusterCentroids.png![Undersampling_ClusterCentroids](https://user-images.githubusercontent.com/80140082/124975171-95936580-dfe2-11eb-89d0-c2936723a490.png)

* The balanced accuracy score is lower at 53%.
* The high_risk precision is still 1% with 61% sensitivity which makes a F1 score of 1%.
* The precision for the low_risk population is 100% with 45% sensitivity due to the high number of false positives.


## Combinatorial with SMOTEEN Model

Combinatorial_SMOTEEN.png![Combinatorial_SMOTEEN](https://user-images.githubusercontent.com/80140082/125140714-fea0d900-e0c7-11eb-8cec-6befb9f5fb9c.png)

* The balanced accuracy score increased to about 62%.
* The high_risk precision is still 1% only with 54% sensitivity which makes a F1 of 2%.
* The precision for the low_risk is 100% with 54% sensitivity due to the high number of false positives.


## Balanced Random Forest Classifier Model

BalancedRandomForestClassifier_model.png![BalancedRandomForestClassifier_model](https://user-images.githubusercontent.com/80140082/125140612-c1d4e200-e0c7-11eb-954f-cf3675640b85.png)

* The balanced accuracy score improved to 79%.
* The high_risk precision is still low at 4% with 67% sensitivity which makes a F1 of only 7%.
* Due to a high number of false positives, the precision for the low_risk is 100% and the sensitivity is now 94%.


## Easy Ensemble AdaBoost Classifier Model

Easy Ensemble AdaBoost Classifier_model.png![Easy Ensemble AdaBoost Classifier_model](https://user-images.githubusercontent.com/80140082/125127849-0190cf00-e0b2-11eb-9a96-c3b6644220a9.png)

* The balanced accuracy score is high to about 93%.
* The high_risk precision is still low at 7% with 91% sensitivity which makes a F1 of only 14%.
* Due to a high number of false positives, the low_risk precision is 100% and the sensitivity is now 94%.



# Analysis 


## Summary

The models used in this analysis demonstrate weak precision in determining if a credit risk is high. There were higher false positives for the RandomOverSamper, SMOTE, and SMOTEEN mdels compared to the Ensemble models. The Ensemble models improved the sensitivity (recall) score to 94% for the high credit risk class which means that they performed better at predicting high credit risk applicants. The downside with the high precision score of 100% is that the models also predict a high number of false positives meaning a high nunber of low credit risk applicants could also be excluded from being offered credit. Therefore, this would penalize the bank and negatively impact the its credit lending strategy and revenue opportunity. 

Perfect precision would mean that applicants declared high credit risk actually are high risk. However, it also means that many low credit risks applicants are falsely predicted as high risk. If the business objective is to detect high credit risk, then ideally, a strong model(s) would be able to predict a high number of true positives or true high credit risk. 

## Recommendation

Given the weak performance of the models evaluated, the recommendation is not to utilize them to predict credit risk. All of the models are inadequately predictive of high credit risk due to the low (<1%) precision and high false positive score of 1.0. Compared to the Oversampling, Underssampling, Combinatorial models, the Balanced Random Forest Classifier and Easy Ensemble AdaBoost Classifier models performed slightly better in precision for high credit risk. However, 

Alternatively, depending on the risk framework and risk tolerance level of the bank offering credit cards, the company may decide to utilize one or several of the models in combination because the trade-off of excluding the high false positives (predicted as high credit risk but are actually low credit risk) and the risk of discriminating against low credit risk applicants outweigh the risk of approving actual high credit risk applicants. In this scenario, the bank may value ensuring equity across demographics in offering credit. Therefore, it is best to explore other models.





