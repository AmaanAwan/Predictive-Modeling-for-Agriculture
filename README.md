# Predictive-Modeling-for-Agriculture
### Project Description:

This project leverages machine learning to help farmers optimize crop selection based on soil conditions. By tackling multicollinearity, it builds a robust multi-class Logistic Regression model to predict the ideal crop for a given field, considering important soil metrics like nitrogen, phosphorus, potassium, and pH value.

### Problem and Objective:

Assessing soil health through comprehensive measurements can be costly and time-consuming, leading farmers to prioritize certain metrics based on budget constraints. This project aims to empower them with intelligent crop selection by predicting the optimum choice based on available soil data.

### Dataset:
soil_measures.csv: Contains essential soil characteristics for various fields, including:

N: Nitrogen content ratio
P: Phosphorous content ratio
K: Potassium content ratio
pH: Soil pH value
crop: Categorical variable indicating the corresponding optimal crop for each field (target variable)

## Steps:

### Data Preprocessing:

Read the soil_measures.csv dataset into a pandas DataFrame.
Perform data checks:
Number of crops
Missing values
Numeric data in feature columns
Split data into training and test sets (80/20 split, random state 42).
### Individual Feature Prediction:

Loop through each feature individually.
Fit a Logistic Regression model for each feature.
Calculate F1 score for each model.
### Multicollinearity Analysis:

Perform correlation analysis between each pair of features.
Select features without high correlation to avoid multicollinearity.
### Final Model Training and Evaluation:

Train a new Logistic Regression model (log_reg) using the selected features.
Evaluate model performance using F1 score and store the metric in model_performance.
