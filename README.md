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
* The precision for the low_risk population is 100% with a sensitivity of 68%. 


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

Combinatorial_SMOTEEEN.png![Combinatorial_SMOTEEEN](https://user-images.githubusercontent.com/80140082/124973588-99be8380-dfe0-11eb-9440-21b94aa4b58e.png)

* The balanced accuracy score increased to about 62%.
* The high_risk precision is still 1% only with 54% sensitivity which makes a F1 of 2%.
* Due to the high number of false positives, the low_risk sensitivity is only 54% even though the precision is 100%.


## Balanced Random Forest Classifier¶ Model

BalancedRandomForestClassifier_model.png![BalancedRandomForestClassifier_model](https://user-images.githubusercontent.com/80140082/125127646-ab239080-e0b1-11eb-96c6-50d18e46b0eb.png)


## Easy Ensemble AdaBoost Classifier Model

Easy Ensemble AdaBoost Classifier_model.png![Easy Ensemble AdaBoost Classifier_model](https://user-images.githubusercontent.com/80140082/125127849-0190cf00-e0b2-11eb-9a96-c3b6644220a9.png)


# Analysis 

### Summary



* The model achieved an accuracy score of 0.6456130066757718 (65%). This means that not every single observations in the testing set was predicted correctly by the model. In other words, it predicted correctly 65% of the time. This also suggests that the dataset may be relatively balanced (versus imbalanced). To contrast this, if the model had achieved an accuracy score of .90 (90%) or 1.0 (100%), it can be mis-leading. A score this high would mean that every single observation in the testing set was predicted correctly by the model. It is rare in actual practice to achieve a perfect accuracy score in the real world.  Moreover, an extremely high metric is a sign for potential overfitting. 

* Looking at the Imbalanced Classification Report, the precision ("pre" column) is .01 which is lower than the recall ("rec" column) which is .61 for the high_risk (majority) class, and for the low_risk (minority) class, the precision is high at 1.0 and the recall is .61, comparatively close to recall for the high_risk class.


- Notes only -- remove later
1. Logistic Regression is a statistical method for predicting binary outcomes from data.
Examples of this are "yes" vs "no" or "high credit risk" vs "low credit risk".

We can calculate logistic regression by adding an activation function as the final step to our linear model. This converts the linear regression output to a probability. These are categories that translate to probability of being a 0 or a 1

Logistic regression predicts binary outcomes, meaning that there are only two possible outcomes. An example of logistic regression might be to decide, based on personal information, whether to approve a credit card application. Multiple variables, such as an applicant's age and income, are assessed to arrive at one of two answers: to approve or to deny the application.

In other words, a logistic regression model analyzes the available data, and when presented with a new sample, mathematically determines its probability of belonging to a class. If the probability is above a certain cutoff point, the sample is assigned to that class. If the probability is less than the cutoff point, the sample is assigned to the other class.
## Recommendations
