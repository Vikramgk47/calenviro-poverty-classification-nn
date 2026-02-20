# calenviro-poverty-classification-nn
CalEnviroScreen Poverty Risk Classification (Neural Network)

Project Overview
This project builds a Neural Network classification model to identify high-poverty census tracts in California using environmental pollution, health burden, and socioeconomic indicators from the CalEnviroScreen dataset.

The objective is to analyze whether environmental exposure and health disparities are associated with economically vulnerable communities.

Business / Policy Motivation
Environmental and socioeconomic inequality are often structurally connected. This model demonstrates how pollution and health indicators can help:

- Identify high-risk communities
- Support data-driven public policy decisions
- Assist environmental justice analysis
- Improve targeted allocation of public resources

This modeling approach can support government agencies, NGOs, and public health planners in prioritizing interventions.

Problem Statement
Original target variable: Poverty (continuous)

Transformation:
1 = Poverty above mean (High Poverty)
0 = Poverty below or equal to mean (Low Poverty)

Problem Type: Binary Classification

Model:
- Neural Network (Sequential API)
- Binary Crossentropy Loss
- Sigmoid Output Activation

Dataset
Source: CalEnviroScreen (California OEHHA)

Each row represents a census tract and includes:
- Environmental indicators (Ozone, PM2.5, Diesel PM, etc.)
- Health metrics (Asthma, Cardiovascular Disease, etc.)
- Socioeconomic measures (Education, Linguistic Isolation, etc.)
- Population data

Total observations: 8035
Total variables: 57

Machine Learning Pipeline
1. Data loading and inspection
2. Feature selection (Population + Environmental + Health indicators)
3. Missing value imputation using median strategy
4. Target recoding (Above/Below Mean Poverty)
5. 90/10 Train-Test Split (Stratified)
6. Feature scaling using StandardScaler
7. Neural Network architecture:
   - Two Dense layers with ReLU activation
   - Dropout regularization
   - Early stopping (patience ≥ 10)
8. Model evaluation:
   - Learning curves
   - Confusion matrices
   - Accuracy and ROC-AUC
9. Baseline comparison using majority-class prediction



Academic Context
Course: OPIM 5509 – Introduction to Deep Learning
University of Connecticut
Instructor: Dr. Dave Wanik
