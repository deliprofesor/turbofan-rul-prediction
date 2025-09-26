# Industrial AI: Predictive Maintenance for Turbofan Engines

<img width="1002" height="565" alt="image" src="https://github.com/user-attachments/assets/792bda1f-4f29-4819-b87b-2c4ad905c503" />


## Overview

This project focuses on **predictive maintenance** using the **NASA C-MAPSS Turbofan Engine Degradation Dataset**. The goal is to predict the **Remaining Useful Life (RUL)** of aircraft engines based on sensor time-series data, simulating real-world industrial maintenance scenarios.

The dataset provides run-to-failure data for multiple engines under different operational conditions, making it ideal for testing and benchmarking predictive models.

## Dataset

**Source:** [NASA Prognostics Data Repository](https://www.nasa.gov/intelligent-systems-division/discovery-and-systems-health/pcoe/pcoe-data-set-repository/)  
**Files Included:**
- `train_FD001.txt` – Training data (FD001 scenario)
- `test_FD001.txt` – Test data (FD001 scenario)
- `RUL_FD001.txt` – Remaining Useful Life labels for test engines
- Similar files for FD002, FD003, FD004 scenarios

**Features:**
- Multiple sensor readings (vibration, temperature, pressure, etc.)
- Engine operating conditions
- Run-to-failure trajectories

**Reference:** Saxena, A., & Goebel, K. (2008). *Turbofan Engine Degradation Simulation Data Set*, NASA Ames Research Center.

## Problem Definition

**Objective:** Predict the RUL of each engine at any given cycle using historical sensor data.  
**Type:** Supervised regression problem.  
**Challenges:**
- High-dimensional multivariate time-series data
- Different operating conditions per engine
- Non-linear degradation patterns

## Methodology

**Steps:**
1. Data preprocessing:
   - Normalize sensor readings
   - Handle missing values
   - Feature engineering (rolling statistics, PCA, etc.)
2. Exploratory Data Analysis:
   - Visualize sensor trends
   - Analyze degradation patterns
3. Model Development:
   - Machine Learning models: Random Forest, Gradient Boosting
   - Deep Learning models: LSTM, GRU
   - Evaluation metrics: RMSE, MAE
4. Model validation and testing

## Project Structure

