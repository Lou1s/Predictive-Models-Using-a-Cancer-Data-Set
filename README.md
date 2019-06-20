# Key Features in Predicting The Survivability of Cancer Sufferers: A Malaysian Case Study
## Introduction
This project is utilising a dataset of breast cancer patients in order to develop predictive models. Specifically, we aim to create models that are able to predict the end result for a given cancer patient's diagnoses (essentially, fatal or non-fatal). Each model will use various features to determine the likelihood of fatality, such as which hospital the patient visited, what stage of cancer they have etc. Along with this predictive/classification element the key factors (the features of the dataset) will also be investigated, so as to determine the key elements that lead to a particular ouptuy (fatality or not).

To accomplish this we will utilise and then tune an SVM model to accurately predict the output. An experiment will then be run with a set of random forests to find the most important features. To validate the methods we will employ these techniques on the popular SEER dataset as well as our dataset. 

## Code
At the current point the cleaning and preliminary modelling of the data has been completed. This is reflected in the cleaning and models notebooks. The SVM model has been fine tuned to achieve an accuracy of roughly 79%. This supports the accuracy of the decision tree model which gives an accuracy of roughly 75%.


A random forest model has been run with 1000 estimators, we have utilised random-search and grid-search in order to find the appropriate hyperparameters. The results of this are in line with the SVM prediction accuracy. However, using 1000 estimators may have resulted in severe bias/over-fitting and an inaccurate model. To rectify this:

We run an experiment to find the most important features. To do this we created a set of 1000 random forest models. Each of these models is randomly initiated with 5 estimators (i.e. trees) and a maximum depth of 5. The most important features from each of these trees is taken and then the average is computed to get the overall importances of each feature.


The reason for this experiment design is due to the small size of the data, by only using 5 estimators, but averaging out the result over 1000 forests we are able to avoid over-fitting and bias, yet still be confident in our result. This, also is the purpose of the SVM model, if both the random forest and the SVM model have roughly the same accuracy then we can be confident in our results.

To further verify the result will will also perform this experiment on (https://seer.cancer.gov/data/) dataset.

#### Notebooks:
1. Cleaning: data management and cleaning for the dataset
2. Models: initial testing and modelling: SVM, Decision Tree and Random Forest
3. Experiment: This notebook contains code that implements an SVM, tunes the SVM and then runs the aforementioned experiment utilising the 1000 random forests. This is conducted on both datasets.

## Results
The metrics from the SVM and random forests conducted on the UM dataset are consistent with both eachother as well as with the metrics computed for the SEER dataset. This is a promising result, furhter information on the overall results can be gleaned from the notebook and will be fully explained in the publication.
## Publication
Following the development of these predictive models the results will be documented in an academic paper and published in a journal or conference.






### Note:
The clean_old and models_old notebooks can be ignored, in those two notebooks we attempted to clean and then utilise the DurationofSymptoms column. However, this column is not coherent and required a lot of (possibly incorrect) assumptions to actually clean and use. Therefore, we dropped this completely and created new cleaning and modelling notebooks.

