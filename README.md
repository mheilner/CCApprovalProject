# Credit Card Approval Prediction Project

This project aims to predict credit card approval decisions using machine learning techniques. The dataset used in this project can be downloaded from the [UCI Machine Learning Repository](http://archive.ics.uci.edu/dataset/27/credit+approval). For a detailed description of the dataset's features, you can refer to this [link](http://rstudio-pubs-static.s3.amazonaws.com/73039_9946de135c0a49daa7a0a9eda4a67a72.html).

## Table of Contents

- [Download Data](#download-data)
- [Summary Statistics](#summary-stats)
- [Train Test Split](#train-test-split)
- [Cleaning Missing Values](#cleaning-missing-values)
  - [Numeric Missing Values](#numeric-missing-values)
  - [Non-numeric Missing Values](#non-numeric-missing-values)
- [Data Preprocessing](#data-preprocessing)
- [Logistic Regression Model](#logistic-regression-model)
- [Evaluating Performance](#evaluating-performance)
- [Hyperparameter Tuning](#hyperparameter-tuning)
- [Visualizations](#Visualizations)

## Download Data

The dataset is loaded into a Pandas DataFrame from a file named `cc.data`.

## Summary Statistics

Summary statistics for the dataset, including mean, standard deviation, minimum, and maximum values, are printed. Information about the DataFrame structure is also provided.

## Train Test Split

The dataset is split into training and testing sets using `train_test_split`. Features 11 and 13 are dropped from the dataset.

## Cleaning Missing Values

### Numeric Missing Values

Missing values represented as '?' are replaced with NaN and imputed using mean imputation.

### Non-numeric Missing Values

For non-numeric data columns, missing values are imputed with the most frequent value.

## Data Preprocessing

Categorical features are one-hot encoded using `pd.get_dummies`. Features are scaled using `MinMaxScaler`.

## Logistic Regression Model

A Logistic Regression model is trained on the preprocessed data, and its accuracy is evaluated.

## Evaluating Performance

Performance is assessed using a confusion matrix to measure the model's accuracy.

## Hyperparameter Tuning

GridSearchCV is used to perform hyperparameter tuning for the Logistic Regression model. The best hyperparameters are selected, and the model's accuracy is assessed again.

## Visualizations

This notebook includes several visualizations to better understand the model's performance and the data:

- **Confusion Matrix**: The confusion matrix heatmap illustrates the model's performance in classifying credit card approvals.
- **ROC Curve**: The ROC curve showcases the model's trade-off between true positive rate and false positive rate.

