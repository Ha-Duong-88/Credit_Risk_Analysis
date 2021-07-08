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


# Results (Balanced Accuracy Scores, Confusion Matrixes and Imbalanced Classification Reports)

### Oversampling with RandomOverSamper Results

Oversampling_RandomOverSampler.png![Oversampling_RandomOverSampler](https://user-images.githubusercontent.com/80140082/124972911-bf975880-dfdf-11eb-81af-edd90318471d.png)

### Oversampling with SMOTE Results

Oversampling_SMOTE.png![Oversampling_SMOTE](https://user-images.githubusercontent.com/80140082/124973262-287ed080-dfe0-11eb-92d3-25903ea4cb92.png)

### Undersampling with ClusterCentroids Reults

Undersampling_ClusterCentroids.png![Undersampling_ClusterCentroids](https://user-images.githubusercontent.com/80140082/124973460-6845b800-dfe0-11eb-8c0c-9da80160e8eb.png)

### Combinatorial with SMOTEEN Results

Combinatorial_SMOTEEEN.png![Combinatorial_SMOTEEEN](https://user-images.githubusercontent.com/80140082/124973588-99be8380-dfe0-11eb-9440-21b94aa4b58e.png)


# Analysis 
## Recommendations
