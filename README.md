# 🛸 Spaceship Titanic - Kaggle Competition

This repository contains my solution to the [Spaceship Titanic](https://www.kaggle.com/competitions/spaceship-titanic) Kaggle competition. The goal of the competition is to predict which passengers were transported to an alternate dimension during a mysterious anomaly on the spaceship *Titanic*.

## 🚀 Overview

- **Task**: Binary classification — predict whether a passenger was *Transported* (`True`/`False`)
- **Evaluation Metric**: Accuracy
- **Best Score Achieved**: **80.874%** 
- **Leaderboard Rank**: 🏅 **Top 5%**

## 📘 Notebook

The notebook [`spaceship-titanic.ipynb`](spaceship-titanic.ipynb) contains the full solution pipeline, including:

- Exploratory Data Analysis (EDA)
- Data preprocessing
- Feature engineering
- Model training using:
  - XGBoost
  - LightGBM
  - LinearSVC (with scaling)
- Model stacking using Logistic Regression as a meta-learner

## 🧠 Model Details

**XGBoost and LightGBM** were hyperparameter-tuned using Optuna, a powerful optimization library, to improve model performance and generalization.
The final model was built by stacking XGBoost, LightGBM and LinearSVC using **Logistic Regression**, which improved the overall predictive performance.

## ⚙️ Preprocessing and Feature engineering

Key preprocessing steps include:

- Handling missing values
- Encoding categorical features
- Feature scaling for SVC
- Splitting cabin information
- Calculate total expenses
- Adding feature "Is family"
- Grouping passenmgers by age to age groups
- Extracting group from passenger ID
- Adding group size
- Adding feature "Is alone" for solo travelers
- Dropping some features

## 📌 Notes

- Tunning hyperparameters using optuna helped boost accuracy.
- The stacking approach significantly improved performance over individual models.
- Feature engineering and feature selection had a strong influence on results.