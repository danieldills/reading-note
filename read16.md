# Machine Learning Intro

## Chapter 1: Bird's Eye View

Machine Learning ≠ Algorithms

Machine learning is a comprehensive approach to solving problems...

...and individual algorithms are only one piece of the puzzle. The rest of the puzzle is how you apply them the right way.

What makes machine learning so special?

Machine learning is the practice of teaching computers how to learn patterns from data, often for making decisions or predictions.

For true machine learning, the computer must be able to learn patterns that it's not explicitly programmed to identify.

Key Terminology

- Model - a set of patterns learned from data.
- Algorithm - a specific ML process used to train a model.
- Training data - the dataset from which the algorithm learns the model.
- Test data - a new dataset for reliably evaluating model performance.
- Features - Variables (columns) in the dataset used to train the model.
- Target variable - A specific variable you're trying to predict.
- Observations - Data points (rows) in the dataset.

## Chapter 2: Exploratory Analysis

- Plot Numberical Distributions

  - Distributions that are unexpected
  - Potential outliers that don't make sense
  - Features that should be binary (i.e. "wannabe indicator variables")
  - Boundaries that don't make sense
  - Potential measurement errors

- Plot Categorical Distributions

  - Categorical features cannot be visualized through histograms. Instead, you can use bar plots.

- Plot Segmentations

  - Segmentations are powerful ways to observe the relationship between categorical features and numeric features.

## Chapter 3: Data Cleaning

The steps and techniques for data cleaning will vary from dataset to dataset. As a result, it's impossible for a single guide to cover everything you might run into.

Better Data > Fancier Algorithms

- In other words... garbage in gets you garbage out. Even if you forget everything else from this course, please remember this point.

Remove Unwanted observations

- The first step to data cleaning is removing unwanted observations from your dataset.

This includes duplicate or irrelevant observations.

Duplicate observations

Duplicate observations most frequently arise during data collection, such as when you:

- Combine datasets from multiple places
- Scrape data
- Receive data from clients/other departments

Irrelevant observations

- Irrelevant observations are those that don’t actually fit the specific problem that you’re trying to solve.

## Chapter 4: Feature Engineering

What is Feature Engineering?

- Feature engineering is about creating new input features from your existing ones.

- In general, you can think of data cleaning as a process of subtraction and feature engineering as a process of addition.

- Infuse Domain Knowledge

- Create Interaction Features

- Combine Sparse Classes

- Add Dummy Variables

- Remove Unused Features

## Chapter 5: Algorithm Selection

How to Pick ML Algorithms

- In applied machine learning, individual algorithms should be swapped in and out depending on which performs best for the problem and the dataset. Therefore, we will focus on intuition and practical benefits over math and theory.

Why Linear Regression is Flawed

- To introduce the reasoning for some of the advanced algorithms, let's start by discussing basic linear regression. Linear regression models are very common, yet deeply flawed.

- Simple linear regression models fit a "straight line" (technically a hyperplane depending on the number of features, but it's the same idea). In practice, they rarely perform well. We actually recommend skipping them for most machine learning problems.

- Their main advantage is that they are easy to interpret and understand. However, our goal is not to study the data and write a research report. Our goal is to build a model that can make accurate predictions.

- In this regard, simple linear regression suffers from two major flaws:

  - It's prone to overfit with many input features.
  - It cannot easily express non-linear relationships.

Regularization in Machine Learning

- This is the first "advanced" tactic for improving model performance. It’s considered pretty "advanced" in many ML courses, but it’s really pretty easy to understand and implement.

- The first flaw of linear models is that they are prone to be overfit with many input features.

## Chapter 6: Model Training

Model Training

How to Train ML Models

It might seem like it took us a while to get here, but professional data scientists actually spend the bulk of their time on the steps leading up to this one:

1. Exploring the data.
2. Cleaning the data.
3. Engineering new features.

Split Dataset

Think of your data as a limited resource.

- You can spend some of it to train your model (i.e. feed it to the algorithm).
- You can spend some of it to evaluate (test) your model.
- But you can’t reuse the same data for both!

What are Hyperparameters?

There are two types of parameters in machine learning algorithms.

The key distinction is that model parameters can be learned directly from the training data while hyperparameters cannot.

Model parameters

Model parameters are learned attributes that define individual models.

- e.g. regression coefficients
- e.g. decision tree split locations
- They can be learned directly from the training data

Hyperparameters

Hyperparameters express "higher-level" structural settings for algorithms.

- e.g. strength of the penalty used in regularized regression
- e.g. the number of trees to include in a random forest
- They are decided before fitting the model because they can't be learned from the data

What is Cross-Validation?

Cross-validation is a method for getting a reliable estimate of model performance using only your training data.

There are several ways to cross-validate. The most common one, 10-fold cross-validation, breaks your training data into 10 equal parts (a.k.a. folds), essentially creating 10 miniature train/test splits.
