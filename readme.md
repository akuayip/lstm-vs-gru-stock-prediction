# LSTM vs GRU for Stock Market Prediction

This project compares the performance of Long Short-Term Memory (LSTM) and Gated Recurrent Unit (GRU) neural networks for predicting stock market movements, specifically for the LQ45 index.

## Project Overview

This repository contains the implementation of both LSTM and GRU models for time-series prediction of stock prices. The models are built using PyTorch and trained on historical stock price data from Yahoo Finance to predict future price movements of the LQ45 index (^JKLQ45).

## Repository Structure

- LQ45_GRU_Models.ipynb - Implementation and training of GRU models
- sahamlstm.ipynb - Implementation and training of LSTM models
- predictiongru.ipynb - Predictions using trained GRU models
- lstmtesting.ipynb - Testing and evaluation of trained LSTM models
- predictgrulstmplot.ipynb - Comparison and visualization of LSTM vs GRU predictions
- GRU RESULT.xlsx - Evaluation results for GRU models
- LSTM Result.xlsx - Evaluation results for LSTM models

## Data Source

The project uses historical data for the LQ45 index (^JKLQ45) from 2005 to 2025 (for forecasting), obtained through the Yahoo Finance API. The data includes:
- Daily closing prices
- Training data from 2005 to approximately 2019 (70%)
- Validation data for hyperparameter tuning (20%)
- Test data for final evaluation (10%)

## Model Architecture

### GRU Model
The GRU model is implemented in the `GRUNet` class with:
- Multiple stacked GRU layers with configurable hidden dimensions
- Layer normalization after each GRU layer
- Dropout for regularization
- Dense layers for final prediction

### LSTM Model
The LSTM model is implemented in the `LSTMNet` class with:
- Multiple stacked LSTM layers with configurable hidden dimensions
- Layer normalization after each LSTM layer
- Dropout for regularization
- Dense layers for final prediction

## Model Hyperparameters

### GRU Hyperparameters
- Window Size: 10 (sequence length)
- GRU Units: [64, 32] (two stacked GRU layers)
- Dense Units: 16
- Dropout Rate: 0.2
- Learning Rate: 0.001
- Batch Size: 8
- Epochs: 200

### LSTM Hyperparameters
- Window Size: 10 (sequence length)
- LSTM Units: [64, 32] (two stacked LSTM layers)
- Dense Units: 16
- Dropout Rate: 0.2
- Learning Rate: 0.001
- Batch Size: 32
- Epochs: 200

## Hyperparameter Tuning

Both models underwent extensive hyperparameter tuning with grid search across:
- Learning rates: [0.001, 0.0001]
- Sequence lengths: [5, 10]
- Batch sizes: [8, 16, 32, 64]
- Epochs: [100, 150, 200]

The best models were saved and used for final evaluation and comparison.

## Usage

1. To train LSTM models:
   - Run sahamlstm.ipynb to train and find optimal LSTM configuration

2. To train GRU models:
   - Run LQ45_GRU_Models.ipynb to train and find optimal GRU configuration

3. To test individual models:
   - Run lstmtesting.ipynb for LSTM model evaluation
   - Run predictiongru.ipynb for GRU model evaluation

4. To compare models:
   - Run predictgrulstmplot.ipynb to load pre-trained models and generate comparison plots

## Results

The project compares the performance of LSTM and GRU models using metrics such as:
- Root Mean Squared Error (RMSE)
- Mean Absolute Error (MAE)
- Mean Absolute Percentage Error (MAPE)
- Visual comparison of predictions against actual stock prices

Detailed results can be found in the Excel files:
- GRU RESULT.xlsx
- LSTM Result.xlsx

## Contributors

| Name                    | ID        | Role                                  | GitHub ID                       |
|-------------------------|-----------|---------------------------------------|----------------------------------|
| M. Arief Rahman Hakim   | 122140083 | Project Leader & Design Researcher    | [Arief](https://github.com/akuayip) |
| Rizki Alfariz Ramadhan  | 122140061 | Data Analyst & Data Engineer         | [Rizki](https://github.com/Alfariz11)|
| Rahmat Aldi Nasda       | 122140077 | ML Engineer                          | [Rahmat](https://github.com/urbaee)|
| Dito Rifki Irawan       | 122140153 | ML Engineer                          | [Dito](https://github.com/Caseinn)|
| Zidan Raihan            | 122140100 | Evaluator & Visualization            | [zidbytes](https://github.com/zidbytes) |
| Fathan Andi Kartagama   | 122140055 | Documentation & GitHub Manager        | [Fathan](https://github.com/pataanggs)|
| Cici Tri Fadila .As     | 122140086 | Documentation & GitHub Manager        | [Cici](https://github.com/ceceyeolie)|

## Technologies Used
- PyTorch (neural network implementation)
- NumPy (numerical operations)
- Pandas (data manipulation)
- Matplotlib (visualization)
- yfinance (Yahoo Finance API for data acquisition)
- scikit-learn (metrics and preprocessing)