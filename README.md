# Passenger-Survivability-Prediction-Using-Logistic-Regression-and-kNNracy-Accident-Survivors
This project analyzes a dataset containing information about vehicle crash accidents in the USA. The focus is on predicting the survivability of passengers based on their age and vehicle speed using logistic regression and k-Nearest Neighbors (kNN) models. The goal is to compare the performance of these models in predicting passenger outcomes.
# Overview
This project analyzes the survivability of passengers involved in vehicle crashes based on their age and the speed of the vehicle at the time of impact. The dataset used comes from data.gov, focusing on passenger survival (1 = survived, 0 = did not survive). The analysis compares the performance of two machine learning models—Logistic Regression and k-Nearest Neighbors (kNN)—in predicting survivability based on age, speed, and both features.
# Dataset
File: crash.csv
Source: Data.gov Crash Data Portal
# Features:
1. Age: The age of the passenger
2. Speed: The speed of the vehicle at the time of the crash (in mph)
3. Survived: Passenger survival status (1 = survived, 0 = did not survive)
# Objective
The goal is to determine: Which features (age, speed, or both) lead to the most accurate predictions of survivability using Logistic Regression.
The impact of varying the number of neighbors (k) in the kNN algorithm on the accuracy of survivability predictions using the same features.
# Project Workflow
1. Exploratory Data Analysis (EDA)
Load the dataset and inspect its structure using .info() and .describe().
Check for missing values and general data characteristics.
2. Logistic Regression
Train three logistic regression models using the following features:
a. Age only
b. Speed only
c. Age and Speed combined
Split the dataset into training and testing sets (80% training, 20% testing).
Calculate the accuracy of each model and compare their performance.
4. k-Nearest Neighbors (kNN)
Train kNN models using the same features (age, speed, both) and test various values of k (from 1 to 10).
Evaluate the accuracy of each kNN model to see which value of k works best for each feature set.
# Key Results
Logistic Regression
Age: Perfect accuracy (1.0)
Speed: Perfect accuracy (1.0)
Age + Speed: Perfect accuracy (1.0)
These results indicate that the logistic regression models perfectly classified passenger survivability using age, speed, or both.

# kNN Results:
When using both Age and Speed, kNN models with k=1 to k=6 achieved perfect accuracy (1.0), while accuracy dropped slightly for larger values of k (7-10).
When using Age or Speed alone, accuracy varied:
For Age, the highest accuracy was seen at k=3, k=4, and k=5 (1.0), while it dropped at k=2, k=6, and k=8.
For Speed, accuracy was highest for k=3 to k=6 (1.0), while it decreased for other values of k.
