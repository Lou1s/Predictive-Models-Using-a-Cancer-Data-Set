# Key Features in Predicting The Survivability of Cancer Sufferers: A Malaysian Case Study
## Introduction
This project is utilising a dataset of breast cancer patients in order to develop predictive models. Specifically, we aim to create models that are able to predict the end result for a given cancer patient's diagnoses (essentially, fatal or non-fatal). Each model will use various features to determine the likelihood of fatality, such as which hospital the patient visited, what stage of cancer they have etc. Along with this predictive/classification element the key factors (the features of the dataset) will also be investigated, so as to determine the key elements that lead to a particular ouptuy (fatality or not).

To accomplish this we will utilise and then tune an SVM model to accurately predict the output. An experiment will then be run with a set of random forests to find the most important features. To validate the methods we will employ these techniques on the popular SEER dataset as well as our dataset. 

## Code
All code has been completed, the details of each notebook are presented below: 
#### Cleaning: 
Data management and cleaning for both the UM and SEER datasets.
#### Models: 
Initial testing and modelling. Here we create then fine tune SVM models, using grid search to find the best parameters. Some initial testing was also conducted using decision trees and random forests. However, the random forest here has been overfitted with 1000 estimators. We overcome this problem by runnning an experiment in the Experiment notebook (below).
#### Experiment: 
This notebook contains code that implements an SVM model for each dataset, utilising the optimal parameters found in the model notebook. We also conduct an experiment using 1000 random forests for each dataset. 

Specifically, we create a set of 1000 random forest models. Each of these models is randomly initiated with 5 estimators (i.e. trees) and a maximum depth of 5. The most important features from each of these trees is taken and then the average is computed to get the overall importances of each feature. We also compute the average precision, accuracy, recall and f1-scores of these forests, for both datasets.

## Results
The metrics from the SVM and random forests conducted on the UM dataset are consistent with both eachother as well as with the metrics computed for the SEER dataset. This is a promising result, further information on the overall results can be gleaned from the notebook and will be fully explained in the publication.
## Publication
On it's way...






### Note:
The clean_old and models_old notebooks can be ignored, in those two notebooks we attempted to clean and then utilise the DurationofSymptoms column. However, this column is not coherent and required a lot of (possibly incorrect) assumptions to actually clean and use. Therefore, we dropped this completely and created new cleaning and modelling notebooks.

