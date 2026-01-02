# PSO-LSTM Air Quality Index (AQI) Prediction

A hybrid **Particle Swarm Optimization (PSO) + Long Short-Term Memory (LSTM)** model for **Air Quality Index (AQI) prediction** using multivariate time-series sensor data.
PSO is used to automatically optimize LSTM hyperparameters and improve performance over a baseline LSTM model.

## Overview

Air quality forecasting plays a critical role in environmental monitoring and public health. While LSTM networks are well-suited for time-series prediction, their performance depends heavily on hyperparameter selection.

This project:

* Trains a **baseline stacked LSTM** for AQI prediction
* Applies **Particle Swarm Optimization (PSO)** for automated hyperparameter tuning
* Compares **baseline vs PSO-optimized** model performance

## Dataset

* **Source:** [UCI Machine Learning Repository – Air Quality Data Set](https://archive.ics.uci.edu/ml/datasets/Air+Quality)
* **Samples:** 9,358 hourly observations
* **Sensors:** Metal oxide chemical sensors
* **Key Pollutants:** CO, NMHC, C6H6, NOx, NO2

## Methodology

### Data Preprocessing

* Missing value handling
* Feature scaling
* Sequence generation for time-series modeling

### AQI Calculation

* AQI values computed from pollutant concentrations using standard AQI formulas

### Baseline Model

* **Stacked LSTM architecture**
* Manually selected hyperparameters
* Used as a reference for comparison

### PSO Optimization

A custom **Particle Swarm Optimization (PSO)** algorithm was implemented to tune:

* Number of LSTM units
* Dropout rate
* Learning rate
* Batch size

## Results

### Model Performance Comparison

| Model                 | R² Score  | MAE       |
| --------------------- | --------- | --------- |
| Baseline Stacked LSTM | ***0.693***   | ***17.95***   |
| PSO-Optimized LSTM    | **0.767** | **14.38** |

The PSO-optimized model outperforms the baseline LSTM by achieving **higher R²** and **lower MAE**, demonstrating the effectiveness of PSO for deep learning hyperparameter optimization.

## Tech Stack

* Python
* TensorFlow / Keras
* Particle Swarm Optimization (custom)
* NumPy, Pandas, Scikit-learn

## Key Insights

* LSTM performance is highly sensitive to hyperparameters
* PSO provides an efficient alternative to manual and grid search tuning
* Swarm intelligence can significantly enhance deep learning models for time-series forecasting
