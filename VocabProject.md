# 20 Vocabulary Terms in 50 words each

- [20 Vocabulary Terms in 50 words each](#20-vocabulary-terms-in-50-words-each)
  - [1-5](#1-5)
    - [Offline Holdout set](#offline-holdout-set)
    - [Machine Learning Pipeline](#machine-learning-pipeline)
    - [Machine Learning Model](#machine-learning-model)
    - [Decision Tree Classifier](#decision-tree-classifier)
    - [Continuous Integration](#continuous-integration)
  - [6-10](#6-10)
    - [MLFlow Expirement](#mlflow-expirement)
    - [Linear Regression](#linear-regression)
    - [Runtime](#runtime)
    - [Single-node Databrick cluster](#single-node-databrick-cluster)
    - [Hyperparameter](#hyperparameter)
  - [11-15](#11-15)
    - [Pandas library](#pandas-library)
    - [Databricks Cluster API](#databricks-cluster-api)
    - [Supervised learning](#supervised-learning)
    - [Black-box model](#black-box-model)
    - [White-box model](#white-box-model)
  - [16-20](#16-20)
    - [Neural Network Weight Bias](#neural-network-weight-bias)
    - [REST API](#rest-api)
    - [JSON](#json)
    - [Reinforcement learning](#reinforcement-learning)
    - [Unsupervised learning](#unsupervised-learning)

## 1-5

### Offline Holdout set

An Offline Holdout set is a dataset that was set aside locally during runtime. This is also known as a test set, it was originally part of the dataset that was split into training and testing. The offline in the word means that the test set is available locally but not on a cloud.

### Machine Learning Pipeline

A Machine Learning pipeline is the definition of the entire process from getting the dataset to training a model and then delivering it. It consists of different steps that together make an automated process from start to end. Meaning as long as you give it data and start it, it will complete fully on it's own.

### Machine Learning Model

A Machine Learning Model is an expression of a trained algorithm that was trained using data. It can recognize certain types of patterns and predict the result using these patterns.
The specific patterns and what it can predict depends on what algorithm you use.

### Decision Tree Classifier

Is an algorithm that functions by making a pyes/no (e.g., bigger than/less than) condition that continually split the dataset until it finds a sequence of nodes that points to a class in your dataset.
It repeats the process until conditions that point to your classes are done.

### Continuous Integration

Continuous integration is the practice of continuously merging different branches of a source control platform to ensure that the version people are working on are also up to date to eachothers changes.
This helps a lot with making sure you don't get huge amounts of merging conflicts when merging big projects.

## 6-10

### MLFlow Expirement

An experiment is a way to organize different trials and or mlruns.
It allows you to categorize runs and their statistics/metrics and artifacts under one category.
It allows you to have different testing and production experiments, so you can have them seperated.

### Linear Regression

Is a method to predict using a lot of datapoints to form a prediction line.
It does this by modelling the relationship between to variables and estimating the response using a line-of-best-fit.

### Runtime

Is the term for the period in which a computer program is executing.
It is essentially when the program is running.

### Single-node Databrick cluster

It's an Apache Spark driver with no Spark workers.
It can do a lot of the basics that a Standard Cluster can do, but it just can't use as many resources.
So a large-scale data processing job will exhaust the resources and possibly even timeout.

### Hyperparameter

Is a parameter in Machine learning used to control the learning process that the machine learning model is doing.
Things like how many layers in a DecisionTree, or which regularization method to use are hyperparameters.

## 11-15

### Pandas library

Is a data manipulation and analysis tool, that's open source as well. It's used to handle data in both simple and complex ways. E.g. things like reading a dataset, performing data transformations on columns and such.

### Databricks Cluster API

awdad

### Supervised learning

As a sub category of machine learning, supervised learning focuses on classifying data or predicting outcomes using labaled datasets. The given model then needs to figure out how to get the answer that is needed using the labeled dataset

### Black-box model

It's essentially a model where it's harder to understand and fully grasp how the model works inside. It's a challenge to understand how the features interact and which ones are important for the output.

### White-box model

Is the opposite of blackbox model. It's easier to understand and interpret, however therein it lacks the complex understanding of datasets that black box models such as neural networks have.

## 16-20

### Neural Network Weight Bias

Assuming you know what Neural Networks are and weights. The bias is a number meant to offset weights between nodes, this bias can be set by a human or the computer itself when back propogating. Bias is often involved in trying to make a model lean towards a certain result

### REST API

a

### JSON

JavaScript Object Notation is a lightweight format meant for storing and moving data. It's setup specifically to be interpretable for a pc and as such often serves as a way of logging errors. The reason for that is that you can make a pc/algorithm read and categorize the errors by different values. It's format looks alot like dictionaries and can most often be ingested entirely like that.

### Reinforcement learning

a

### Unsupervised learning

a
