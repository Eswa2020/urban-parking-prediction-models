# Urban Parking Prediction Models

## Overview
This repository presents a spatiotemporal urban parking modelling project focused on predicting parking availability and parking pressure using temporal, spatial, and operational features. The work draws on urban parking datasets including Melbourne and Colombia-related parking data to explore how statistical and machine learning approaches can support parking prediction, decision support, and smart mobility planning.

The project is positioned at the intersection of urban analytics, predictive modelling, transport systems, and decision support. It is intended to demonstrate applied research capability in feature engineering, modelling design, and interpretation of parking dynamics in urban environments.

## Research Motivation
Urban parking availability is influenced by both time-varying and location-specific factors. Demand fluctuates across hours, days, zones, and land-use contexts, while supply pressure is affected by turnover, traffic patterns, and local accessibility conditions. As a result, parking systems are well suited to spatiotemporal modelling approaches that combine statistical reasoning with predictive analytics.

This project investigates how temporal and spatial signals can be used to estimate future parking space availability and better understand parking behaviour in cities.

## Project Objectives
The project is designed around the following objectives:

- model parking availability using temporal and spatial features
- compare statistical and machine learning approaches for parking prediction
- explore operational interpretations using Markov-process and queueing-inspired perspectives
- evaluate how feature engineering improves predictive usefulness
- support urban decision-making through interpretable modelling outputs

## Datasets
This repository draws on urban parking datasets used for modelling and experimentation, including:

- Melbourne parking dataset
- Colombia-related parking dataset or urban parking observations used for comparative modelling

Depending on the experimental workflow, the data may include variables such as:
- parking location or zone
- timestamp
- occupancy or available spaces
- parking duration or turnover indicators
- temporal attributes such as hour, weekday, or seasonality
- spatial context or zone-based identifiers

## Problem Statement
The central modelling problem is to estimate future parking availability or parking demand pressure using a combination of temporal patterns, spatial features, and operational behaviour.

This has practical relevance for:
- urban planners
- parking operators
- smart mobility systems
- traffic management teams
- decision-support platforms for access and pricing

## Methodological Approach

### 1. Data Preparation
The workflow begins with data cleaning, temporal parsing, location-based structuring, and preparation of analysis-ready parking records.

### 2. Feature Engineering
The project emphasizes high-value feature engineering across three categories:

#### Temporal Features
- hour of day
- day of week
- weekday vs weekend
- time-window demand patterns
- lagged parking behaviour where applicable

#### Spatial Features
- parking zone or location grouping
- neighborhood-level differences
- local parking pressure patterns
- spatial clustering or segment behavior

#### Operational Features
- transition behavior in parking state changes
- turnover-related proxies
- queueing-inspired system interpretations
- state-based dynamics for availability estimation

### 3. Statistical and Analytical Models
The project explores statistical and system-based approaches to parking prediction, including:
- baseline descriptive or rule-based models
- Markov-process inspired modelling of parking state transitions
- queueing-oriented interpretations of parking turnover and future availability

### 4. Machine Learning Models
Machine learning models are used to compare predictive performance against statistical baselines. Depending on the data formulation, these may include:
- classification models for parking state prediction
- regression models for future availability estimation
- tree-based models for nonlinear feature interactions

### 5. Evaluation
Models are evaluated using predictive performance, interpretability, and relevance for operational decision-making.

## Repository Structure
```text
urban-parking-prediction-models/
├── README.md
├── requirements.txt
├── data/
│   ├── raw/
│   └── processed/
├── notebooks/
│   ├── 01_data_preparation.ipynb
│   ├── 02_feature_engineering.ipynb
│   ├── 03_statistical_baseline.ipynb
│   ├── 04_markov_queueing_analysis.ipynb
│   ├── 05_ml_prediction.ipynb
│   └── 06_results_and_visualization.ipynb
├── src/
│   ├── preprocess.py
│   ├── features.py
│   ├── markov_model.py
│   ├── queueing_analysis.py
│   ├── train_ml.py
│   └── evaluate.py
├── outputs/
│   ├── figures/
│   └── tables/
└── docs/
    └── methodology.md
