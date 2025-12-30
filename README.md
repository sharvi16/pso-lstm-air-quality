# PSO-LSTM Air Quality Prediction

This project implements a hybrid **Particle Swarm Optimization (PSO) - Long Short-Term Memory (LSTM)** model to predict the Air Quality Index (AQI).

## Project Overview

The goal is to optimize the hyperparameters of an LSTM neural network using the PSO algorithm to achieve better prediction accuracy for time-series air quality data.

## Dataset

The project uses the [Air Quality Data Set](https://archive.ics.uci.edu/ml/datasets/Air+Quality) from the UCI Machine Learning Repository. It contains 9358 instances of hourly averaged responses from an array of 5 metal oxide chemical sensors embedded in an Air Quality Chemical Multisensor Device.

## Features

- **Data Preprocessing**: Handling missing values, outlier detection, and feature scaling.
- **AQI Calculation**: Deriving the Air Quality Index from pollutant concentrations (CO, NMHC, C6H6, NOx, NO2).
- **PSO Optimization**: Custom implementation of Particle Swarm Optimization to tune:
  - Number of LSTM Units
  - Dropout Rate
  - Learning Rate
  - Batch Size
- **LSTM Model**: Stacked LSTM architecture for time-series forecasting.

## Results

The optimized model achieves an R² score of approximately **0.767** on the test set.
