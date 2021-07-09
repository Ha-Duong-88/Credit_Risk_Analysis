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

### Oversampling with RandomOverSamper Model

Oversampling_RandomOverSampler.png![Oversampling_RandomOverSampler](https://user-images.githubusercontent.com/80140082/124972911-bf975880-dfdf-11eb-81af-edd90318471d.png)

### Oversampling with SMOTE Model

Oversampling_SMOTE.png![Oversampling_SMOTE](https://user-images.githubusercontent.com/80140082/124973262-287ed080-dfe0-11eb-92d3-25903ea4cb92.png)

### Undersampling with ClusterCentroids Model

Undersampling_ClusterCentroids.png![Undersampling_ClusterCentroids](https://user-images.githubusercontent.com/80140082/124973460-6845b800-dfe0-11eb-8c0c-9da80160e8eb.png)


Undersampling_ClusterCentroids.png![Undersampling_ClusterCentroids](https://user-images.githubusercontent.com/80140082/124975171-95936580-dfe2-11eb-89d0-c2936723a490.png)

### Combinatorial with SMOTEEN Model

Combinatorial_SMOTEEEN.png![Combinatorial_SMOTEEEN](https://user-images.githubusercontent.com/80140082/124973588-99be8380-dfe0-11eb-9440-21b94aa4b58e.png)


# Analysis 

### Summary
* The model achieved an accuracy score of 62% (0.6156536172852936). This means that not every single observations in the testing set was predicted correctly by the model. In other words, it predicted correctly 60% of the time. This also suggests that the dataset may be relatively balanced. To contrast this, if the model had achieved an accuracy score of 90% (.90) or 100% (1.0), it can be mis-leading. A score this high would mean that every single observation in the testing set was predicted correctly by the model. It is rare in actual practice to achieve a perfect accuracy score in the real world.  Moreover, an extremely high metric is a sign for potential overfitting. 




Overfitting refers to an instance in which the patterns picked up by a model are too specific to a specific dataset. 

The sole purpose of the next cell is to create a new data point, which shows up as a red dot on the new plot. The logistic regression model will then classify this sample as belonging to class 0 (purple) or class 1 (yellow):


- Notes only -- remove later
1. Logistic Regression is a statistical method for predicting binary outcomes from data.
Examples of this are "yes" vs "no" or "high credit risk" vs "low credit risk".

We can calculate logistic regression by adding an activation function as the final step to our linear model. This converts the linear regression output to a probability. These are categories that translate to probability of being a 0 or a 1

Logistic regression predicts binary outcomes, meaning that there are only two possible outcomes. An example of logistic regression might be to decide, based on personal information, whether to approve a credit card application. Multiple variables, such as an applicant's age and income, are assessed to arrive at one of two answers: to approve or to deny the application.

In other words, a logistic regression model analyzes the available data, and when presented with a new sample, mathematically determines its probability of belonging to a class. If the probability is above a certain cutoff point, the sample is assigned to that class. If the probability is less than the cutoff point, the sample is assigned to the other class.
## Recommendations
