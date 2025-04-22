---
title: Data Mining Competition Earthquake Classification
type: page
---

![GIF_Page](/images/data_mining_competition_earthquake_classification.gif)

# Problem

We were challenged to predict the phase of an earthquake—a multiclass classification task—within a strict **5-hour time limit**. The results had to be submitted to Kaggle for leaderboard ranking and also presented live to a panel of judges.

# Resolve and Result

We broke the process down into three key stages:

1. Data Cleaning & Transformation
- Applied labeling and One-Hot Encoding to categorical features
- Split into train, validation, and test sets
- Scaling using Standard Scaler
- Handled class imbalance with SMOTE oversampling

2. Exploratory Data Analysis (EDA)
- Used a heatmap to explore correlation between sensor values
- Discovered distribution of earthquake phases pretty different
- No missing values

3. Data Modeling
- Due to limited time and using **only a standard laptop**, we prioritized fast experimentation
- Performed hyperparameter tuning with Randomized Search
- Tried several models:
  - Decision Tree 
  - Random Forest 
  - XGBoost (best-performing)

## 🏆 Results
- Our XGBoost model achieved the highest accuracy of **90%**
- We secured **1st place** on the Kaggle leaderboard for the competition!

## Repository
- [**Github Code**](https://github.com/azharizz/STEADataset_DataMining)
- [**Kaggle**](https://www.kaggle.com/competitions/finaldatamininganforcom20/leaderboard)

