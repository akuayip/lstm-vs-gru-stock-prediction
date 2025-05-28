# LSTM vs GRU for Stock Market Prediction

This project compares the performance of Long Short-Term Memory (LSTM) and Gated Recurrent Unit (GRU) neural networks for predicting stock market movements, specifically for the LQ45 index.

## Project Overview

This repository contains the implementation of both LSTM and GRU models for time-series prediction of stock prices. The models are built using PyTorch and trained on historical stock price data to predict future price movements.

## Repository Structure

- LQ45_GRU_Models.ipynb - Implementation of GRU models for stock prediction
- sahamlstm.ipynb - Implementation of LSTM models for stock prediction
- predictiongru.ipynb - Predictions using trained GRU models
- predictgrulstmplot.ipynb - Comparison and visualization of LSTM vs GRU predictions
- GRU RESULT.xlsx - Evaluation results for GRU models
- LSTM Result.xlsx - Evaluation results for LSTM models

## Model Architecture

### GRU Model
The GRU model is implemented in the `GRUNet` class with:
- Multiple stacked GRU layers with configurable hidden dimensions
- Layer normalization after each GRU layer
- Dropout for regularization
- Dense layers for final prediction

### LSTM Model
The LSTM model is implemented in the `LSTMModel`/`LSTMNet` class with:
- Multiple stacked LSTM layers with configurable hidden dimensions
- Layer normalization after each LSTM layer
- Dropout for regularization
- Dense layers for final prediction

## Model Hyperparameters

### GRU Hyperparameters
- Window Size: 10
- GRU Units: [64, 32]
- Dense Units: 16
- Dropout Rate: 0.2
- Learning Rate: 0.001
- Batch Size: 8
- Epochs: 200

### LSTM Hyperparameters
- Window Size: 10
- LSTM Units: [64, 32]
- Dense Units: 16
- Dropout Rate: 0.2
- Learning Rate: 0.001
- Batch Size: 32
- Epochs: 200

## Usage

To run the comparison between LSTM and GRU models:
1. Execute predictgrulstmplot.ipynb to load pre-trained models and generate prediction plots

## Results

The project compares the performance of LSTM and GRU models using metrics such as:
- Visual comparison of predictions against actual stock prices
- Quantitative metrics for model evaluation

Detailed results can be found in the Excel files:
- GRU RESULT.xlsx
- LSTM Result.xlsx

## Contributors

| Name                    | ID        | Role                                  | GitHub ID                       |
|-------------------------|-----------|---------------------------------------|----------------------------------|
| M. Arief Rahman Hakim   | 122140083 | Project Leader & Design Researcher    | [Arief](https://github.com/akuayip) |
| Rizki Alfariz Ramadhan  | 122140061 | Data Analyst & Data Engineer         | [Rizki](https://github.com/Alfariz11)|
| Rahmat Aldi Nasda       | 122140077 | ML Engineer                           | [Rahmat](https://github.com/urbaee)|
| Dito Rifki Irawan       | 122140153 | ML Engineer                           | [Dito](https://github.com/Caseinn)|
| Zidan Raihan            | 122140100 | Evaluator & Visualization           | [zidbytes](https://github.com/zidbytes) |
| Fathan Andi Kartagama   | 122140055 | Documentation & GitHub Manager        | [Fathan](https://github.com/pataanggs)|
| Cici Tri Fadila .As     | 122140086 | Documentation & GitHub Manager        | [Cici](https://github.com/ceceyeolie)|

## Technologies Used
- PyTorch
- NumPy
- Pandas
- Matplotlib
- yfinance (Yahoo Finance API)