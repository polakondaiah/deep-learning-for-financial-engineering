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


## Section 5 — Project 1: Return Forecasting

### Overview
Forecast 25‑day ETF returns using deep learning models to identify cross‑asset relationships and improve directional accuracy.

### Dataset
- **Assets:** SPY, TLT, SHY, GLD, DBO  
- **Period:** 2007 – 2022  
- **Source:** Yahoo Finance

### Models
- MLP (baseline)
- CNN‑GAF (image‑based)
- Single‑output LSTM
- Multi‑output LSTM (predicts all 5 assets jointly)

### Key Results
- **Multi‑output LSTM** effectively leveraged cross‑asset dependencies, outperforming single‑output variants.
- Achieved positive out‑of‑sample **R²** for **TLT** and **GLD**.
- A long‑short strategy based on model signals **outperformed** the equally weighted buy‑and‑hold benchmark.

---

## Section 6 — Project 2: Leakage‑Controlled Validation

### Problem
Standard walk‑forward validation can leak future information through overlapping training windows, inflating performance.

### Solution
- **Walk‑forward** validation with a strict **embargo** period to exclude overlapping observations.
- Applied to SPY direction forecasting (up/down) using the same three model families.

### Backtesting
Re‑evaluated all strategies under realistic, leakage‑free conditions to ensure generalisability.

### Conclusions
- Embargo validation significantly reduced over‑optimism, especially for high‑capacity models (LSTM).
- Leakage‑controlled backtests provide a **more trustworthy** estimate of real‑world performance.

---

## Section 7 — Comparison

| Feature          | Project 1 (Return Forecasting) | Project 2 (Direction Prediction) |
|------------------|--------------------------------|----------------------------------|
| **Goal**         | Return Forecasting             | Direction Prediction             |
| **Assets**       | 5 ETFs (SPY, TLT, SHY, GLD, DBO) | SPY (single asset)              |
| **Models**       | 4 (MLP, CNN‑GAF, LSTM‑single, LSTM‑multi) | 3 (MLP, CNN‑GAF, LSTM) |
| **Walk‑forward** | ❌ No                           | ✅ Yes                           |
| **Embargo**      | ❌ No                           | ✅ Yes                           |
| **Portfolio**    | ✅ Yes (multi‑asset allocation) | ❌ No (single asset only)        |
| **Backtesting**  | ✅ Yes                          | ✅ Yes                           |



## Repository Highlights

| Category               | Specification                                       | Key Libraries                         | Core Competencies                                    |
|------------------------|-----------------------------------------------------|---------------------------------------|------------------------------------------------------|
| **Programming & ML**   | Python, TensorFlow / Keras                          | NumPy, Pandas, Scikit‑learn, Matplotlib, Seaborn | Deep Learning, Financial Machine Learning            |
| **Data & Assets**      | SPY, TLT, SHY, GLD, DBO (via Yahoo Finance)        | yfinance, pyts                        | Time‑Series Forecasting, CNN‑GAF                     |
| **Modelling**          | MLP, CNN‑GAF, LSTM (Multi‑output)                  | TensorFlow, Keras                     | Multi‑output Learning, Sequence Modelling            |
| **Validation & Strategy** | Walk‑forward + Embargo, Backtesting, Portfolio Allocation | (Custom backtester)                   | Walk‑forward Validation, Embargo Validation, Tactical Asset Allocation, Quantitative Finance |



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







