# Credit Card Fraud Detection

## Table of Contents
- [Introduction](#introduction)
- [Dataset](#dataset)
- [Usage](#usage)
- [Models](#models)
  - [Logistic Regression](#logistic-regression)
  - [Random Forest](#random-forest)
- [Results](#results)

## Introduction

This project aims to detect fraudulent credit card transactions using machine learning techniques. The dataset used for this analysis contains anonymized features from real-world credit card transactions, including both legitimate and fraudulent transactions. The goal is to build a model that can accurately classify transactions as fraudulent or not.

For more detailed information about the approach, methodology, and analysis, you can also check out the [project paper](CC_Fraud_Detection.pdf) I wrote.


## Dataset

The dataset contains transactions made by European cardholders in September 2013. It is highly imbalanced, with only 0.172% of the transactions being fraudulent.
You can find and download the dataset from [Kaggle's Credit Card Fraud Detection page](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud).

- **Features:**
  - `Time`: The time of the transaction, in seconds from the first transaction.
  - `Amount`: The transaction amount.
  - `V1-V28`: Principal Component Analysis (PCA) transformed features for confidentiality.
  - `Class`: The target variable (1 for fraud, 0 for legit).

The dataset is pre-processed to handle imbalances and scaled to ensure proper training of machine learning models.


## Usage

1. Open the Jupyter notebook:
    ```bash
    jupyter notebook CC_Fraud_Detection.ipynb
    ```

2. Follow the steps in the notebook to:
    - Load and pre-process the dataset.
    - Train the machine learning models.
    - Evaluate the models using accuracy and other performance metrics.

## Models

### Logistic Regression

Logistic Regression is a simple and interpretable model, used to predict the probability of a binary outcome (fraud or not fraud). In this project, logistic regression achieved an accuracy score of **91.4%** on the test data.

### Random Forest

Random Forest is an ensemble learning method that uses multiple decision trees. It is more flexible and capable of capturing complex patterns. The Random Forest model achieved an accuracy score of **89.3%** on the test data, but a higher training accuracy of **98.9%**, indicating potential overfitting.

## Results

- **Logistic Regression**: 
    - Training Accuracy: 94.5%
    - Test Accuracy: 91.4%
  
- **Random Forest**: 
    - Training Accuracy: 98.9%
    - Test Accuracy: 89.3%

While Logistic Regression generalized better on the test data, the Random Forest model had higher performance on the training set, suggesting it can capture more complex patterns in the data.
