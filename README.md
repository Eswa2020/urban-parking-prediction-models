# Urban Parking Prediction Models

## Overview
This repository presents a set of urban parking analytics case studies focused on modelling parking behaviour using temporal, spatial, and operational features. The project brings together multiple parking-related workflows across three contexts:

- Melbourne, with a Docklands-focused modelling workflow
- Colombia-related parking analysis for comparative modelling
- Dubai QGIS-based spatial parking workflows

The repository is positioned at the intersection of urban analytics, predictive modelling, transport systems, GIS, stochastic modelling, and decision support. It is intended to demonstrate applied research capability in feature engineering, model comparison, spatial interpretation, and reproducible urban parking analysis.

## Research Motivation
Urban parking availability is influenced by both time-varying and location-specific factors. Demand fluctuates across hours, days, streets, zones, and activity environments, while operational pressure is shaped by turnover, violations, accessibility, and local land-use intensity. For this reason, parking systems are well suited to spatiotemporal modelling approaches that combine statistical reasoning, machine learning, state-transition analysis, and spatial methods.

This repository investigates how temporal, spatial, and operational signals can be used to estimate parking behaviour, forecast parking pressure, interpret duration and turnover, and support urban parking decision-making.

## Project Objectives
The repository is designed around the following objectives:

- model parking behaviour using temporal, spatial, and operational features
- compare statistical and machine learning approaches for parking prediction
- explore state-transition behaviour using Markov-process logic
- examine GIS and spatial workflows for parking-related analysis
- support urban decision-making through interpretable and reproducible modelling outputs
- develop comparable parking workflows across multiple city contexts

## Case Study Tracks

### 1. Melbourne / Docklands
This is currently the most developed analytical workflow in the repository. It focuses on a Docklands-heavy Melbourne parking dataset and examines whether parking behaviour can be modelled as a structured urban operational system rather than as purely random short-term variation.

The Docklands workflow is organized around four analytical layers:

- short-term occupancy forecasting
- parking-duration regression
- stochastic state-transition modelling
- prescriptive analytics for parking management decision support

### 2. Colombia
This track is intended for comparative parking analysis in a different urban context. It is being organized as an extension of the broader modelling framework so that patterns identified in Melbourne can later be compared with another city-level parking system.

### 3. Dubai QGIS
This track focuses on GIS-based and spatial parking workflows, including QGIS-oriented exploratory and analytical work. It is intended to support spatial interpretation, mapping, and urban parking context analysis, rather than to duplicate the full Docklands modelling pipeline.

## Datasets
This repository draws on urban parking datasets used for modelling and experimentation, including:

- Melbourne parking data, with a strong Docklands concentration
- Colombia-related parking data or parking observations for comparative modelling
- Dubai spatial and GIS parking-related data used in QGIS workflows

Depending on the workflow, the data may include variables such as:

- parking location, street, bay, area, or zone
- arrival and departure timestamps
- occupancy or vehicle presence
- parking duration and turnover indicators
- violation indicators
- temporal attributes such as hour, weekday, weekend, and seasonality
- spatial or GIS context such as zones, streets, and mapped parking environments

## Problem Statement
The central problem explored in this repository is how parking systems can be modelled as structured urban processes using a combination of temporal, spatial, and operational features.

This has practical relevance for:

- urban planners
- parking operators
- smart mobility systems
- traffic and curbside management teams
- GIS-supported urban analysis
- decision-support platforms for monitoring, allocation, and pricing review

## Methodological Approach

### 1. Data Preparation
The workflows begin with data cleaning, timestamp parsing, removal of duplicates, treatment of missing values, and preparation of analysis-ready parking records.

### 2. Feature Engineering
The project emphasizes feature engineering across three categories:

#### Temporal Features
- hour of day
- day of week
- weekday versus weekend
- month and season
- time-of-day groupings
- lagged parking behaviour where applicable

#### Spatial Features
- street, area, bay, or zone grouping
- neighbourhood-level or precinct-level variation
- local parking pressure patterns
- spatial context derived from GIS or mapped parking environments

#### Operational Features
- vehicle presence or occupancy state
- parking duration
- parking violations
- turnover-related proxies
- state-transition behaviour in parking events

### 3. Statistical and Analytical Models
The repository explores analytical approaches to parking behaviour, including:

- descriptive and aggregated parking analysis
- linear regression as an interpretable baseline
- Markov-process modelling of parking state transitions
- clustering-based parking typologies for interpretation
- GIS-based spatial analysis in Dubai workflows

### 4. Machine Learning Models
Machine learning models are used to compare predictive performance against simpler baselines. Depending on the case study, these may include:

- Random Forest forecasting for occupancy prediction
- Random Forest regression for parking-duration prediction
- feature-importance analysis for nonlinear interpretation
- clustering methods for typology analysis

### 5. Evaluation
Models are evaluated using predictive performance, interpretability, and relevance for operational decision-making. Depending on the workflow, outputs may include:

- forecasting MAE and RMSE
- regression MAE, RMSE, and R²
- Markov transition probabilities and steady-state interpretation
- clustering summaries
- GIS-based maps and spatial outputs
- rule-based prescriptive categories for management support

## Current Findings
The strongest completed results currently come from the Docklands, Melbourne workflow. These results indicate that parking behaviour contains meaningful temporal and street-level structure.

Key Docklands findings include:

- Random Forest forecasting outperformed a naive lag baseline for occupancy prediction
  - MAE: 0.2823 to 0.1736
  - RMSE: 0.4011 to 0.2466

- Random Forest regression outperformed linear regression for parking-duration prediction
  - MAE: 51.04 to 37.37
  - RMSE: 81.01 to 64.96
  - R²: 0.1330 to 0.4424

- A two-state Markov model showed frequent switching between empty and occupied states
  - Empty → Occupied: 0.8680
  - Occupied → Empty: 0.8268

These findings suggest that Docklands parking dynamics are structured enough to support forecasting and decision support, while also exhibiting high short-run turnover.

## Repository Structure
```text
urban-parking-prediction-models/
├── README.md
├── requirements.txt
├── .gitignore
├── data/
│   ├── raw/
│   └── processed/
├── notebooks/
│   ├── melbourne/
│   ├── colombia/
│   └── dubai_qgis/
├── src/
├── outputs/
│   ├── figures/
│   ├── tables/
│   └── models/
└── docs/
    └── project_summary.md
