# Leakage-Controlled Walk-Forward Validation for Deep Learning Models in SPY Direction Forecasting

## Overview

Financial machine learning models often report optimistic performance due to hidden temporal data leakage. This project investigates how progressively stricter validation protocols affect the apparent predictive ability of deep learning models for financial time-series forecasting.

Three architectures—Multi-Layer Perceptron (MLP), Long Short-Term Memory (LSTM), and Convolutional Neural Networks using Gramian Angular Fields (CNN-GAF)—are evaluated under multiple validation strategies, culminating in leakage-controlled walk-forward validation with a 20-day embargo period.

The objective is not to maximize prediction accuracy, but to demonstrate how proper validation provides a more realistic estimate of model performance.


## Key Features

- SPY ETF daily market data (2016–2023)
- 24 engineered financial features
- 20-day directional prediction
- MLP, LSTM and CNN-GAF architectures
- Walk-forward validation
- Purged 20-day embargo
- Strategy backtesting
- Performance comparison with Buy-and-Hold

## Highlights

- Compared three deep learning architectures under four validation protocols.
- Demonstrated that temporal leakage substantially inflates apparent model performance.
- CNN-GAF achieved the highest AUC-ROC (0.5709) under the strictest leakage-free evaluation.
- Under embargo validation, none of the models consistently outperformed the buy-and-hold benchmark.
- Showed that validation methodology is as important as model architecture in financial machine learning.

## Technologies

- Python
- TensorFlow / Keras
- NumPy
- Pandas
- Scikit-learn
- Matplotlib
- yfinance
- pyts


├── notebooks/
├── report/
├── figures/
├── results/
├── requirements.txt
└── README.md



## Key Findings

✔ Conventional train/test splits can produce misleadingly optimistic results.

✔ Walk-forward validation provides a more realistic estimate of model performance.

✔ Introducing a 20-day embargo removes temporal label leakage.

✔ Higher returns do not necessarily imply better predictive skill.

✔ Under leakage-free evaluation, none of the tested architectures demonstrated statistically meaningful directional forecasting ability.



## Future Work

- Transformer-based time-series models
- Regime-aware feature engineering
- Alternative labeling methods
- Cross-asset validation
- Portfolio optimization
- Risk-aware position sizing
