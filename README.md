Data Science & Machine Learning Toolkit
This repository contains a collection of Jupyter notebooks designed for specialized data analysis, model diagnostics, and metric engineering tasks.

Table of Contents
Automated Simpson’s Paradox Detection

Automated Data Leakage Detection System

Feature Stability Monitoring System

Metric Engineering Beyond Accuracy

Model Failure Diagnosis Without Retraining

Olympic Athlete Overperformance Index

1. Automated Simpson’s Paradox Detection
Files: Automated Simpson’s Paradox Detection.ipynb, Automated_Simpson’s_Paradox_Detection.ipynb

Description
These notebooks provide a framework for automatically identifying Simpson's Paradox in datasets. The paradox occurs when a trend appears in several different groups of data but disappears or reverses when these groups are combined.

Key Features
Synthetic Data Generation: Creates datasets simulating classic scenarios (like university admissions) where paradoxes often occur.

Automated Detection Engine: Functions to calculate associations globally and within subgroups to find sign reversals.

Visualization: Generates side-by-side bar plots comparing overall rates against subgroup rates to visually confirm the paradox.

2. Automated Data Leakage Detection System
File: Automated_Data_Leakage_Detection_System.ipynb

Description
A system designed to identify "target leakage"—when information from outside the training dataset is used to create the model, leading to overly optimistic performance.

Key Features
Risk Scoring: Analyzes features for high correlation with the target variable that may indicate leakage.

Leakage Reports: Produces a summary report (e.g., leakage_report) identifying high-risk features and their descriptive statistics.

Correlation Analysis: Specifically looks for features like "account balance at time of fraud" which inherently contain the answer the model is trying to predict.

3. Feature Stability Monitoring System
File: Feature Stability Monitoring System.ipynb

Description
This notebook implements a monitoring tool to ensure that the distribution of features remains consistent over time, which is critical for maintaining model reliability in production.

Key Features
PSI Calculation: Computes the Population Stability Index (PSI) for both categorical and numerical variables.

Stability Reporting: Classifies features as "Stable," "Moderate Shift," or "Unstable" based on their PSI scores.

Categorical Analysis: Specifically handles category distribution shifts by comparing base and new data distributions.

4.Manual Model Explainability Engine

This project implements a manual feature attribution system for classification models without using SHAP, LIME, or similar libraries.
It explains individual predictions by decomposing the model output into feature-level contributions that can be compared across samples.

The implementation uses Logistic Regression, since its linear structure makes the attribution mathematically exact.

Why This Exists

Most explainability tools behave like black boxes themselves.
This project shows how to build an explainability engine from first principles:

No third-party explainability libraries

No approximations

No heuristics

100% mathematically grounded

5. Metric Engineering Beyond Accuracy
File: Metric_Engineering_Beyond_Accuracy.ipynb

Description
Focused on advanced model evaluation, this notebook moves beyond standard accuracy to define metrics that align more closely with business value and risk.

Key Features
Business Risk-Adjusted Profit/Loss (BRAPL): A custom metric that assigns financial values to True Positives, True Negatives, False Positives, and False Negatives.

Custom Cost-Benefit Analysis: Allows users to define a dictionary of benefits and costs to calculate the actual economic impact of a model's predictions.

6. Model Failure Diagnosis Without Retraining
File: Model_Failure_Diagnosis_Without_Retraining.ipynb

Description
Provides tools to diagnose why a model might be failing in production by analyzing feature drift, without the need to immediately retrain the model.

Key Features
Feature Drift Detection: Compares historical "training" distributions to "future" production data.

Drift Ranking: Ranks features by their drift score to help data scientists prioritize which variables are causing performance degradation.

Support for Mixed Data: Handles both numerical and categorical feature sets.

7. Olympic Athlete Overperformance Index (OPI)
File: Olympic Athlete Overperformance Index.ipynb

Description
Uses historical Olympic data to identify athletes who performed significantly better than statistical expectations based on their physical attributes and demographics.

Key Features
Expected Performance Modeling: Utilizes a Ridge regression pipeline (with scaling and one-hot encoding) to predict "expected" performance.

OPI Calculation: Standardizes the residuals (the gap between actual and expected performance) to create an Overperformance Index.

Ranking: Ranks the top K athletes (e.g., top 50) based on their OPI score.

Requirements
Python 3.x

Pandas

NumPy

Scikit-Learn (for OPI and metric notebooks)

Matplotlib / Seaborn (for visualization)
