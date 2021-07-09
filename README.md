# Credit_Risk_Analysis

Overview of the analysis: Explain the purpose of this analysis.

Results: Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all six machine learning models. Use screenshots of your outputs to support your results.

Summary: Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. If you do not recommend any of the models, justify your reasoning.

There is a title, and there are multiple sections (2 pt)
Each section has a heading and subheading (2 pt)
Links to images are working, and code is formatted and displayed correctly (2 pt).

# Project Overview
Using a credit card credit dataset from LendingClub, a peer-to-peer lending services company, the objective of this project was to assess the credit worthiness of applicants by applying machine learning to credit card risk analysis. Since credit risk is an inherently unbalanced classification problem, as good loans easily outnumber risky loans, the scope of the project entailed employing different techniques to train and evaluate models with unbalanced classes using the imbalanced-learn and scikit-learn libraries to build and evaluate models using resampling.

## Project Scope
The analysis involved the following process:

1) Oversample the data using the RandomOverSampler and SMOTE algorithms.
2) Undersample the data using the ClusterCentroids algorithm.
3) Use a combinatorial approach of over and undersampling using the SMOTEENN algorithm.
4) Compare two new machine learning models that reduce bias, BalancedRandomForestClassifier and EasyEnsembleClassifier, to predict credit risk.
5) Finally, evaluate the performance of these models using balanced accuracy, precision, and recall (sensitivity) scores.

## Technologies Used
Jupyter Notebook, Python, Pandas DataFrame, imbalanced-learn package and libraries including NumPy, version 1.11 or later, SciPy, version 0.17 or later, and Scikit-learn, version 0.21 or later, and six machine learning models. A machine learning environment was also set up with accompanying Anaconda packages.


# Results (Balanced Accuracy Scores, Confusion Matrixes and Imbalanced Classification Reports) For Credit Resampling Machine Learning

## Oversampling with RandomOverSamper Model

Oversampling_RandomOverSampler.png![Oversampling_RandomOverSampler](https://user-images.githubusercontent.com/80140082/124972911-bf975880-dfdf-11eb-81af-edd90318471d.png)

* The balanced accuracy score is 65%
* The high_risk precision is 1% only with 61% sensitivity which makes a F1 score of 2%.
* The precision for the low_risk population is 100% with a sensitivity (recall) of 68%. 


## Oversampling with SMOTE Model

Oversampling_SMOTE.png![Oversampling_SMOTE](https://user-images.githubusercontent.com/80140082/124973262-287ed080-dfe0-11eb-92d3-25903ea4cb92.png)

* The results are similar to the previous RandomOverSampler model.
* The balanced accuracy score is 62%.
* The high_risk precision is 1% with 64% sensitivity which makes a F1 score of 2%.
* The precision for the low_risk population is 100% with a sensitivity of 64%.


## Undersampling with ClusterCentroids Model

Undersampling_ClusterCentroids.png![Undersampling_ClusterCentroids](https://user-images.githubusercontent.com/80140082/124975171-95936580-dfe2-11eb-89d0-c2936723a490.png)

* The balanced accuracy score is lower at 53%.
* The high_risk precision is still 1% with 61% sensitivity which makes a F1 score of 1%.
* The precision for the low_risk population is 100% with 45% sensitivity. This is likely due to the high number of false positives.


## Combinatorial with SMOTEEN Model

Combinatorial_SMOTEEN.png![Combinatorial_SMOTEEN](https://user-images.githubusercontent.com/80140082/125140714-fea0d900-e0c7-11eb-8cec-6befb9f5fb9c.png)

* The balanced accuracy score increased to about 62%.
* The high_risk precision is still 1% only with 54% sensitivity which makes a F1 of 2%.
* Due to the high number of false positives, the precision is 100% and the low_risk sensitivity is only 54%.


## Balanced Random Forest Classifier Model

BalancedRandomForestClassifier_model.png![BalancedRandomForestClassifier_model](https://user-images.githubusercontent.com/80140082/125140612-c1d4e200-e0c7-11eb-954f-cf3675640b85.png)

* The balanced accuracy score improved to about 79%.
* The high_risk precision is still low at 4% with 67% sensitivity which makes a F1 of only 7%.
* Due to a high number of false positives, the precision is 100% and low_risk sensitivity is now 94%.

## Easy Ensemble AdaBoost Classifier Model

Easy Ensemble AdaBoost Classifier_model.png![Easy Ensemble AdaBoost Classifier_model](https://user-images.githubusercontent.com/80140082/125127849-0190cf00-e0b2-11eb-9a96-c3b6644220a9.png)

* The balanced accuracy score is high to about 93%.
* The high_risk precision is still low at 7% with 91% sensitivity which makes a F1 of only 14%.
* Due to a high number of false positives, the precision is 100% and low_risk sensitivity is now 94% with 


# Analysis 

## Summary

All of the models used for this credit risk analysis demonstrate weak precision in determining if a credit risk is high. There were higher false positives for the RandomOverSamper, SMOTE, and SMOTEEN mdels compared to the Ensemble models. The Ensemble models improved the sensitivity score to 91% for the high credit risk class which means that they performed better at predicting high credit risk applicants. The downside with the high precision score of 100% is that the models also predict a high number of false positives meaning a high nunber of low credit risk applicants could also be excluded from being offered credit. Therefore, this would negatively impact the company's credit lending strategy and revenue opportunity. Perfect precision would mean that applicants declared high credit risk actually are high risk. However, it also means that many low credit risks applicants are falsely predicted as high risk. If the business objective is to detect high credit risk, then ideally, a strong model(s) would be able to predict a high nunber of true positives or true high credit risk. 

## Recommendation

Given the weak performance of the models evaluated, the recommendation is not to utilize them to predict credit risk.




