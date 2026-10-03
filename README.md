# Kickstarter Campaign Success Prediction

## Project Overview

This project focuses on predicting the success of Kickstarter crowdfunding campaigns using Machine Learning.

The objective is to analyze historical Kickstarter campaign data, perform data preprocessing and feature engineering, train multiple machine learning classification models, and evaluate their performance in predicting whether a campaign will be successful or unsuccessful.

The project follows a complete machine learning pipeline from dataset collection and preprocessing to model training and evaluation.

## Problem Statement

Crowdfunding platforms such as Kickstarter host thousands of projects across different categories. However, not every project successfully reaches its funding goal.

The objective of this project is to develop a machine learning-based approach to predict whether a Kickstarter campaign will be successful based on features such as funding goal, campaign duration, category, country, currency, launch information, and project name characteristics.

## Dataset

The dataset used for this project was obtained from Kaggle.

The original dataset contains Kickstarter campaign information such as:

- Project name
- Category
- Main category
- Currency
- Campaign goal
- Launch date
- Deadline
- Amount pledged
- Number of backers
- Country
- Campaign state

After preprocessing and filtering the dataset for the required prediction task, the final dataset contains:

- Total samples: 331,675
- Training samples: 265,340
- Testing samples: 66,335
- Target classes: 0 and 1

Target representation:

- 0 → Failed
- 1 → Successful

### Target Distribution

Training set:

- Class 0: 59.61%
- Class 1: 40.39%

Testing set:

- Class 0: 59.61%
- Class 1: 40.39%

## Data Preprocessing

The following preprocessing steps were performed:

- Converted deadline and launch dates into datetime format.
- Calculated campaign duration.
- Extracted launch year, launch month, and launch day of the week.
- Handled missing project names.
- Checked for missing values.
- Applied logarithmic transformation to the funding goal.
- Created additional numerical features.
- Encoded categorical variables using One-Hot Encoding.
- Standardized numerical features using StandardScaler.

## Feature Engineering

Additional features were created to improve the prediction process.

### Funding Features

- Log-transformed funding goal
- Goal required per campaign day
- Log-transformed goal per campaign day

### Campaign Features

- Campaign duration
- Launch year
- Launch month
- Launch day of the week

### Project Name Features

- Name length
- Number of words in the project name
- Number of exclamation marks
- Number of question marks

### Frequency Features

Frequency-based features were also created for:

- Category
- Main category
- Country
- Currency

## Train-Test Split

The dataset was divided into training and testing sets using an 80:20 stratified split.

```text
Training samples: 265,340
Testing samples: 66,335
