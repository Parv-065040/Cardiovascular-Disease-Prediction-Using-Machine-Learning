# Cardiovascular-Disease-Prediction-Using-Machine-Learning

Project Overview

This project focuses on predicting the risk of cardiovascular disease using machine learning techniques on a large-scale healthcare dataset. The objective is to build an interpretable and clinically meaningful model that prioritizes recall, ensuring that high-risk patients are identified early for preventive intervention.

The project was developed as part of an academic curriculum and demonstrates end-to-end application of data preprocessing, class imbalance handling, model building, evaluation, and business-oriented insights.

Problem Statement

Cardiovascular disease is one of the leading causes of death worldwide. Traditional diagnostic methods are often reactive and may fail to detect high-risk individuals early.
The goal of this project is to develop a predictive model that uses demographic, lifestyle, and medical attributes to identify individuals at risk of heart disease, with a strong emphasis on minimizing false negatives.

Dataset

Source: Kaggle – Cardiovascular Disease Risk Prediction Dataset

Total Records: 308,854

Features: 19

Target Variable: Heart_Disease (Yes / No)

Class Distribution:

No Heart Disease: ~91.9%

Heart Disease: ~8.1%

Data Quality: No missing values

Methodology

Data Inspection & Cleaning

Verified data types, distributions, and completeness

Confirmed absence of missing values

Feature Engineering

One-hot encoding applied to categorical variables

Target variable encoded into binary format

Train–Test Split

80/20 split with stratification to preserve class imbalance

Handling Class Imbalance

Applied SMOTE on training data to balance minority class

Model Development

Logistic Regression (baseline, interpretable model)

Random Forest Classifier (non-linear, feature importance)

Threshold Optimization

Tuned classification threshold to improve recall

Selected threshold = 0.2 for healthcare screening use-case

Model Performance Summary
Model	Accuracy	Recall (Heart Disease)	Key Insight
Logistic Regression	~91.9%	6%	High accuracy but fails to detect positives
Random Forest (Default)	~91.7%	6%	SMOTE alone insufficient
Random Forest + Threshold Tuning	~83.7%	53%	Clinically useful recall improvement

Key Outcome:
Threshold tuning resulted in nearly 9× improvement in recall, significantly reducing missed heart disease cases.

Key Insights

Self-reported general health is one of the strongest predictors

Age remains the most dominant non-modifiable risk factor

Diabetes, BMI, smoking history, and arthritis significantly increase risk

Accuracy alone is misleading for imbalanced medical datasets

Recall-precision trade-off is acceptable in medical screening scenarios

Business & Clinical Relevance

Can be used as a first-level screening tool

Helps healthcare providers prioritize high-risk individuals

Supports preventive healthcare and early intervention strategies

Demonstrates real-world application of machine learning in healthcare analytics

Tools & Technologies

Python

Pandas, NumPy

Scikit-learn

Imbalanced-learn (SMOTE)

Matplotlib / Seaborn

Jupyter Notebook

Authors

Parv

Akshit Kansal

Aman Malhi

Mayank Jha

Rhythmya Bansal

Awantika Kholia

Disclaimer

This project is for academic and educational purposes only and should not be used as a substitute for professional medical diagnosis or treatment.
