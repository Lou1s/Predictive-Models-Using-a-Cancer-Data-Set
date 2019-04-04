# Predictive Models Using a Cancer Data Set
## Introduction
This project is utilising a dataset of breast cancer patients in order to develop predictive models. Specifically, we aim to create models that are able to predict the end result for a given cancer patient's diagnoses (essentially, fatal or non-fatal). Each model will use various features to determine the likelihood of fatality, such as which hospital the patient visited, what stage of cancer they have etc.

## Code
At the current point the cleaning and preliminary modeling of the data has been completed. This is reflected in the cleaning and models notebooks. As of now we have succesfully run SVM, decision tree and random forest models. Next up is to do cross validation for SVM and DT.

## Publication
Following the development of these predictive models the results will (hopefully) be documented in an academic paper and published in a journal or conference.







### Note:
The clean_old and models_old notebooks can be ignored, in those two notebooks we attempted to clean and then utilise the DurationofSymptoms column. However, this column is not coherent and required a lot of (possibly incorrect) assumptions to actually clean and use. Therefore, we dropped this completely and created new cleaning and modelling notebooks.
