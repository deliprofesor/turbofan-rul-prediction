# Industrial AI: Predictive Maintenance for Turbofan Engines

<img width="1013" height="567" alt="image" src="https://github.com/user-attachments/assets/d913c681-c581-48aa-aedc-8d9d5be16886" />

## Overview

This project focuses on **predictive maintenance** using the **NASA C-MAPSS Turbofan Engine Degradation Dataset**.  
The main goal is to predict the **Remaining Useful Life (RUL)** of aircraft engines based on sensor time-series data, simulating real-world industrial maintenance scenarios.

The dataset provides run-to-failure data for multiple engines under different operational conditions, making it ideal for testing and benchmarking predictive models.

## Dataset

<img width="823" height="555" alt="image" src="https://github.com/user-attachments/assets/922c64e1-fc7d-4cee-83cf-cf0773a10e5d" />

**Source:** [NASA Ames Prognostics Data Repository](https://www.nasa.gov/intelligent-systems-division/discovery-and-systems-health/pcoe/pcoe-data-set-repository/)  
**License:** U.S. Government Works  
**Citation:** Saxena, A., & Goebel, K. (2008). "Turbofan Engine Degradation Simulation Data Set", NASA Ames Research Center.

**Overview:**  
The NASA C-MAPSS dataset contains run-to-failure sensor data from turbofan engines under multiple operational conditions and fault modes. It is widely used in predictive maintenance research for Remaining Useful Life (RUL) estimation.

**Structure:**  
- **Training files (`train_FD00X.txt`)** – Full run-to-failure sensor readings per engine  
- **Test files (`test_FD00X.txt`)** – Partial sequences for evaluation  
- **RUL files (`RUL_FD00X.txt`)** – Remaining Useful Life for test engines  

**Features:**
- Engine ID, cycle number, operational settings
- 21 sensor measurements (vibration, temperature, pressure, etc.)
- Run-to-failure trajectories

### Sensor Descriptions

| Sensor | Description |
|--------|-------------|
| s1     | High-pressure compressor inlet temperature |
| s2     | High-pressure compressor outlet temperature |
| s3     | Low-pressure turbine temperature |
| s4     | High-pressure turbine temperature |
| s5     | Fan speed |
| s6     | Core speed |
| s7     | Engine pressure ratio |
| s8     | Fuel flow |
| s9     | Oil pressure |
| s10    | Oil temperature |
| s11    | Vibration sensor 1 |
| s12    | Vibration sensor 2 |
| s13    | Vibration sensor 3 |
| s14    | Vibration sensor 4 |
| s15    | Exhaust gas temperature |
| s16    | Turbine inlet temperature |
| s17    | Fan discharge pressure |
| s18    | Low-pressure compressor speed |
| s19    | High-pressure compressor speed |
| s20    | Bleed air temperature |
| s21    | Airflow rate |

### Operational Settings

| Setting | Description |
|---------|-------------|
| op1     | Altitude setting |
| op2     | Mach number |
| op3     | Throttle resolver angle |

> Note: Some sensors may be redundant or correlated. Feature engineering or dimensionality reduction (e.g., PCA) can help improve model performance.

## Problem Definition

**Objective:** Predict the Remaining Useful Life (RUL) of each engine at any given cycle using historical sensor data.  
**Type:** Supervised regression problem.  

**Challenges:**
- High-dimensional multivariate time-series data
- Different operating conditions per engine
- Non-linear degradation patterns

## Methodology

**Steps:**

1. **Data Preprocessing**
   - Normalize sensor readings
   - Handle missing values
   - Feature engineering (rolling statistics, PCA, etc.)

2. **Exploratory Data Analysis**
   - Visualize sensor trends
   - Analyze degradation patterns
   - Identify key sensors influencing RUL

3. **Model Development**
   - **Machine Learning models:** Random Forest, Gradient Boosting
   - **Deep Learning models:** LSTM, GRU
   - **Evaluation metrics:** RMSE, MAE, R²

4. **Model Validation and Testing**
   - Cross-validation with train/test split
   - Compare predictions against actual RUL
   - Tune hyperparameters for optimal performance




