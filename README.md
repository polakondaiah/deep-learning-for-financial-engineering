# Leakage-Controlled Walk-Forward Validation for Deep Learning Models in SPY Direction Forecasting

## Financial Machine Learning | Deep Learning | Quantitative Finance | Backtesting

This repository investigates how different validation protocols influence the apparent performance of deep learning models for financial time-series forecasting.

The project compares Multi-Layer Perceptron (MLP), Long Short-Term Memory (LSTM), and Convolutional Neural Networks using Gramian Angular Fields (CNN-GAF) under progressively stricter validation protocols, culminating in leakage-controlled walk-forward validation with an embargo period.

Rather than maximizing predictive accuracy, the primary objective is to demonstrate how improper validation can substantially overestimate model performance in financial machine learning.



## Motivation

Financial machine learning models often report impressive prediction accuracy due to hidden data leakage.

Traditional train/test splits violate the temporal structure of financial markets and allow future information to indirectly influence model training.

This project evaluates how model performance changes as progressively stricter validation protocols are introduced, ultimately using embargoed walk-forward validation inspired by López de Prado's methodology.





## Dataset

- Asset: SPY ETF
- Source: Yahoo Finance (yfinance)
- Period: 2016-01-21 to 2023-12-29
- Observations: ~2,000 trading days
- Prediction Horizon: 20 trading days
