# ML-Project

## Project Overview

This project implements a Machine Learning pipeline for data preprocessing, model training, and evaluation. The dataset is prepared and divided into training and testing sets using stratified sampling to maintain the target-class distribution.

## Dataset

- Training samples: 265,340
- Testing samples: 66,335
- Total samples: 331,675
- Target classes: 0 and 1
- Training target distribution:
  - Class 0: 59.61%
  - Class 1: 40.39%
- Testing target distribution:
  - Class 0: 59.61%
  - Class 1: 40.39%

## Train-Test Split

The dataset is divided into training and testing sets using stratified sampling. This ensures that the proportion of target classes remains approximately the same in both datasets.

## Technologies Used

- Python
- NumPy
- Pandas
- Matplotlib
- Seaborn
- Scikit-learn
- KaggleHub

## Project Structure

```text
ML-Project/
│
├── Kickstarter_ML_Project.ipynb
├── requirements.txt
└── README.md
