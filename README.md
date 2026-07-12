# Deep Learning for Financial Engineering

### Deep Learning • Financial Machine Learning • Time-Series Forecasting • Tactical Asset Allocation • Walk-Forward Validation

This repository contains two end-to-end deep learning projects completed for  Deep Learning for Finance. Together, they explore the development, evaluation, and practical deployment of deep learning models for financial time-series prediction.


## Overview

Financial markets present unique challenges for machine learning, including
non-stationarity, temporal dependence, regime shifts, and data leakage.

This repository investigates these challenges through two complementary
projects.

Project 1 focuses on building deep learning models for tactical asset
allocation across multiple exchange-traded funds (ETFs).

Project 2 investigates how improper validation protocols can inflate
performance estimates and demonstrates leakage-controlled walk-forward
validation for financial machine learning.


## Repository Highlights

| Feature              | Description             |
| -------------------- | ----------------------- |
| Language             | Python                  |
| Framework            | TensorFlow / Keras      |
| Assets               | SPY, TLT, SHY, GLD, DBO |
| Models               | MLP, CNN-GAF, LSTM      |
| Validation           | Walk-forward + Embargo  |
| Dataset              | Yahoo Finance           |
| Backtesting          | Yes                     |
| Portfolio Allocation | Yes                     |



## Repository Structure & Workflow


```bash
deep-learning-for-financial-engineering/
├── README.md
├── LICENSE
├── requirements.txt
│
├── project_1_tactical_asset_allocation/
│   ├── 01_spy_direction_forecasting.ipynb   # Main notebook (MLP, CNN-GAF, LSTM)
│   ├── outputs/                              # All CSVs, figures, and summary tables
│   └── project1_report___spy_direction_forecasting.pdf
│
├── project_2_leakage_controlled_validation/
│   ├── 02_leakage_controlled_validation.ipynb
│   ├── outputs/
│   └── project2_report___leakage_controlled_validation.pdf
│
└── shared/
    └── assets/

=========================================================================================

Financial Market Data
        │
        ▼
 Feature Engineering
        │
        ▼
 Deep Learning Models
        │
        ├───────────────┐
        ▼               ▼
 Project 1         Project 2
(Return Forecast) (Direction Prediction)
        │               │
        ▼               ▼
 Backtesting      Walk-forward + EmbargoValidation
        │               │
        └───────────────┘
                │
                ▼
      Financial ML Insights
```

## 📊 Project Overview

| Category               | Specification                                       | Key Libraries                         | Core Competencies                                    |
|------------------------|-----------------------------------------------------|---------------------------------------|------------------------------------------------------|
| **Programming & ML**   | Python, TensorFlow / Keras                          | NumPy, Pandas, Scikit‑learn, Matplotlib, Seaborn | Deep Learning, Financial Machine Learning            |
| **Data & Assets**      | SPY, TLT, SHY, GLD, DBO (via Yahoo Finance)        | yfinance, pyts                        | Time‑Series Forecasting, CNN‑GAF                     |
| **Modelling**          | MLP, CNN‑GAF, LSTM (Multi‑output)                  | TensorFlow, Keras                     | Multi‑output Learning, Sequence Modelling            |
| **Validation & Strategy** | Walk‑forward + Embargo, Backtesting, Portfolio Allocation | (Custom backtester)                   | Walk‑forward Validation, Embargo Validation, Tactical Asset Allocation, Quantitative Finance |


## 📊 Project Overview

| Feature              | Description             | Technology / Skill      | Details                                   |
|----------------------|-------------------------|-------------------------|-------------------------------------------|
| **Language**         | Python                  | Core Libraries          | NumPy, Pandas, Scikit‑learn               |
| **Framework**        | TensorFlow / Keras      | Visualization           | Matplotlib, Seaborn                       |
| **Assets**           | SPY, TLT, SHY, GLD, DBO | Data Sources            | yfinance, pyts                            |
| **Models**           | MLP, CNN‑GAF, LSTM      | ML / Deep Learning      | Financial ML, CNN‑GAF, LSTM, Multi‑output |
| **Validation**       | Walk‑forward + Embargo  | Validation Techniques   | Walk‑forward, Embargo                     |
| **Backtesting**      | Yes                     | Quantitative Finance    | Tactical Asset Allocation, Backtesting    |
| **Portfolio Allocation** | Yes                 |                         |                                           |


## Technologies
Python

TensorFlow / Keras

NumPy

Pandas

Scikit-learn

Matplotlib

Seaborn

yfinance

pyts

## Skills Demonstrated

✔ Financial Machine Learning

✔ Deep Learning

✔ Time-Series Forecasting

✔ Tactical Asset Allocation

✔ Multi-output Learning

✔ CNN-GAF

✔ LSTM

✔ Walk-forward Validation

✔ Embargo Validation

✔ Strategy Backtesting

✔ Quantitative Finance
