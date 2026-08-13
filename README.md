# Ames-Housing-Price-Prediction
Machine learning project for predicting house prices using Gradient Boosting and a Flask web application
# 📌 Project Overview

## This project is an end-to-end Machine Learning House Price Prediction solution developed using the Ames Housing Dataset.

## The main objective of this project is to analyze residential property data, identify the most important factors influencing house prices, develop a machine learning regression model, and create an interactive application that allows users to predict house prices based on property characteristics.

## The project demonstrates the complete machine learning workflow, starting from data exploration and feature selection and progressing to model development, evaluation, model serialization, and deployment through a Flask web application.

# End-to-End Workflow
- Raw Housing Dataset
        ↓
- Data Understanding & Exploration
        ↓
- Correlation Analysis
        ↓
- Feature Selection
        ↓
- SelectKBest
        ↓
- Lasso Regression
        ↓
- Recursive Feature Elimination (RFE)
        ↓
- Selection of Relevant Features
        ↓
- Train-Test Split
        ↓
- Gradient Boosting Regression
        ↓
- Model Evaluation
        ↓
- Model Serialization using Joblib
        ↓
- Flask Web Application
        ↓
- User Input
        ↓
- Predicted House Price
# 🎯 Business Problem

## House prices are influenced by numerous property characteristics, including location, size, quality, construction year, garage capacity, basement area, and other features.

## For a buyer, seller, or real-estate professional, estimating an appropriate property price can be challenging when many factors influence the final sale price.

## This project addresses the problem by using historical housing data to develop a machine learning model that learns the relationship between property characteristics and their corresponding sale prices.

#🎯 Project Objectives

## The key objectives of this project are:

- Understand and analyze the Ames Housing Dataset.
- Explore relationships between housing features and sale price.
- Identify important features affecting house prices.
- Apply multiple feature-selection techniques.
- Develop a regression-based machine learning model.
- Evaluate the predictive performance of the model.
- Save the trained model for future predictions.
- Develop an interactive house-price prediction interface.
- Integrate the trained model with a Flask web application.
# 📊 Dataset

The project uses the Ames Housing Dataset, which contains residential property information from Ames, Iowa.

Dataset Information
Attribute	Details
Dataset	Ames Housing Dataset
Number of Records	2,930
Number of Original Features	82
Target Variable	SalePrice
Problem Type	Supervised Learning
Machine Learning Task	Regression
Target Variable

The target variable is:

SalePrice

SalePrice represents the final sale price of the residential property.


🔍 Project 1 — Data Analysis & Feature Selection
Notebook
Capstone 1 housing.ipynb

The first stage focuses on understanding the housing dataset and identifying variables that have meaningful relationships with the target variable.

Activities Performed
Imported Python libraries.
Loaded the Ames Housing Dataset.
Examined the dataset structure.
Checked the number of rows and columns.
Explored numerical variables.
Analyzed descriptive statistics.
Examined correlations between numerical features.
Studied relationships between features and SalePrice.
Identified relevant features for machine learning.
Reduced the feature space for model development.
Correlation Analysis

Correlation analysis was performed to understand the relationship between numerical variables and SalePrice.

Features with stronger relationships with the target variable were investigated further for model development.

# 🧠 Feature Selection

## Feature selection was an important part of the project because using relevant variables can help build a more efficient and interpretable machine learning model.

- Several feature-selection techniques were explored.

1. Correlation Analysis

Features were examined based on their correlation with SalePrice.

2. SelectKBest

SelectKBest was used to identify features with strong statistical relationships with the target variable.

3. Lasso Regression

Lasso Regression was explored as a regularization-based feature-selection technique.

Lasso can reduce less important feature coefficients toward zero, helping identify variables that contribute more strongly to prediction.

4. Recursive Feature Elimination — RFE

Recursive Feature Elimination was used to recursively remove less important features and identify a smaller set of relevant predictors.

5. Common Feature Selection

The results from the different feature-selection techniques were compared to identify features that appeared consistently important.

# 🤖 Project 2 — Machine Learning Model Development
Notebook
housing model.ipynb

The second stage focuses on preparing the selected features and developing the machine learning model.

# Selected Features

# The model was developed using important housing characteristics, including:

- Lot Frontage
- Lot Area
- Overall Qual
- Year Built
- Year Remod/Add
- Mas Vnr Area
- BsmtFin SF 1
- Gr Liv Area
- Garage Cars
- Garage Area
- Target
- SalePrice
# ✂️ Train-Test Split

## The dataset was divided into training and testing subsets.

- The training data was used to train the machine learning model, while the testing data was used to evaluate its performance on unseen observations.

- An 80:20 train-test split was used.

- 80% → Training Data
- 20% → Testing Data

## A fixed random state was used to improve reproducibility.

- 🌳 Machine Learning Algorithm
- Gradient Boosting Regressor

# The primary machine learning model used in this project is:

- GradientBoostingRegressor(random_state=42)

- Gradient Boosting is an ensemble learning technique that builds multiple decision trees sequentially. Each subsequent tree attempts to improve the errors made by the previous models.

- The final model combines these learners to produce a stronger predictive model.

  #📏 Model Evaluation

## The regression model was evaluated using standard regression metrics.

- Mean Absolute Error — MAE

- MAE measures the average absolute difference between the actual house prices and the predicted house prices.

- A lower MAE indicates better performance.

- Root Mean Squared Error — RMSE

- RMSE measures the square root of the average squared prediction error.

- RMSE gives greater importance to larger errors.

- A lower RMSE indicates better performance.

- R² Score

- R² measures how much of the variation in the target variable is explained by the model.

- A value closer to 1 generally indicates stronger explanatory performance.

# Model Results

## The final model evaluation results are documented in the machine learning notebook.

- Metric	Result
- MAE	Add your notebook result
- RMSE	Add your notebook result
- R² Score	Add your notebook result

- Note: Replace the three placeholders above with the exact values produced by your notebook. Do not estimate or invent these numbers.

# 🖥️ Project 3 — Interactive House Price Prediction
## Notebook
- User_Interface_Prediction.ipynb

- The third stage focuses on creating an interactive interface for making house-price predictions.

- The interface allows users to provide property information such as:

- Lot Frontage
- Lot Area
- Overall Quality
- Year Built
- Year Remodeled/Added
- Masonry Veneer Area
- Finished Basement Area
- Ground Living Area
- Garage Cars
- Garage Area

- The trained machine learning model processes these values and generates a predicted house price.

# 💾 Model Serialization

- After training, the machine learning model was saved using Joblib.

# housing_model.pkl

- This allows the trained model to be loaded later without retraining it.

- The Flask application loads this saved model and uses it to generate predictions.

# 🌐 Flask Web Application

## A Flask-based web application was developed to provide a user-friendly interface for house-price prediction.

# Backend
- housing_predictor_app.py
- Frontend
- templates/index.html

- The application works through the following process:

- User enters property details
        ↓
- HTML form submits the values
        ↓
- Flask receives the input
        ↓
- Saved ML model is loaded
        ↓
- Model generates prediction
        ↓
- Predicted house price is displayed

## This converts the machine learning model into a usable prediction application rather than keeping it limited to a Jupyter Notebook.
