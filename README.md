# road-accident-classification

## Introduction
With the increasing of road traffic infrastructures, motor vehicles, drivers, and traffic flow, the role of road traffic in supporting and guiding economic and social development is becoming more and more obvious. As a result, road traffic safety has increasingly become a key issue in concerning the safety of people’s lives and property, as well as affecting the quality and efficiency of economic and social development. Road traffic accidents are the process of simultaneous damage of people or things, which caused by the coupling imbalance of dynamic and static factors such as human, vehicle, road, and environment. Therefore, it is necessary to study the influencing factors, as well as the classification and identification model of the severity of road traffic accident, so as to pave the way for improving the safety level of road traffic.

## Executive Summary:

This data science project aims to develop a model for predicting the severity of road accidents based on various features. The severity classification is crucial for understanding the factors influencing accidents and for implementing targeted interventions to improve road safety.

## Objective:

The primary goal of this project is to build a predictive model that classifies the severity of road accidents into different categories, such as minor, moderate, and severe. This model can assist in identifying high-risk areas and implementing preventive measures to reduce the frequency and severity of accidents.

## Data Collection:

Source: 
The dataset used for this project was obtained from **Addis Ababa Sub-city Police Departments**. It includes information about various factors associated with road accidents, such as weather conditions, road type, time of day, and more. All the sensitive information has been excluded during data encoding and finally it has 32 features and 12316 instances of the accident.

## Features:

Independent Variables: These include features like weather conditions, road type, lighting conditions, time of day, number of vehicles involved, and more.
Dependent Variable: The severity of the accident, categorized as minor, moderate, or severe.
Data Exploration:

## Descriptive Statistics:

Summary statistics for each feature.
Distribution of accident severity classes.

## Data Cleaning:

Handling missing values.
Dealing with outliers.
Data Visualization:

## Univariate and bivariate visualizations to understand the distribution and relationships among variables.
Heatmaps and correlation plots to identify feature importance.
Data Preprocessing:

## Feature Scaling:

Normalization or standardization of numerical features.
Categorical Variable Encoding:

Transformation of categorical variables into numerical format (one-hot encoding, label encoding, etc.).

### Model Training:
* On training my model using several classification algorithms, the model trained with **ExtraTreesClassifier** gave best results. 

* Used **RepeatedStratifiedKFold** with 5 splits cross validation with hyper-parameter tuning on ExtraTreesClassifier (baseline model) using **GridSearchCV**.

* Also, I found that my baseline model (ExtraTreesClassifier) was overfitting the dataset. On investigation I found that the dataset was affected by **Curse of Dimensionality**. So I reduced the dimensions and trained my model again.

* After retraining my model, I found that it was generalizing well with an accuracy of **92.23%**.

* As per the problem statement I used **F1 Score** as the evaluation metric for my model.