# Stock Price Forecasting with ARIMAX (Time Series Analysis)

## Author
Suyog Shrestha

Data Science & Business @ Knox College - June 2027

---

## Overview
This project explores stock price forecasting using a classical **ARIMAX (AutoRegressive Integrated Moving Average with eXogenous variables)** model.  
The goal is not to claim accurate stock prediction, but to **build, evaluate, and interpret a statistically sound time-series forecasting pipeline**, and to compare it against a strong baseline model.

The project demonstrates:
- Time-series feature engineering
- Proper train/test splitting for temporal data
- ARIMAX modeling using `pmdarima`
- Baseline comparison using a naive random-walk forecast

---

## How to Run This Project
1. Clone the repository
2. Install dependencies (pip install -r requirements.txt)
3. Launch Jupyter Notebook
4. Run all cells sequentially in the following sequence:
    - Notebooks/01_feature_eng.ipynb
    - Notebooks/02_arimax_model.ipynb

---

## Modeling Approach

### ARIMAX
The ARIMAX model extends ARIMA by incorporating **exogenous variables** such as lagged prices and rolling statistics.

The model order is selected automatically using:
- Stepwise search
- AIC (Akaike Information Criterion)

### Baseline Model
A **naive random-walk baseline** is used:
Forecast(t) = Price(t − 1)

This baseline is intentionally simple but extremely strong for financial price series.

---

## Key Findings

- The naive baseline outperforms ARIMAX when forecasting price levels
- This result aligns with the **Efficient Market Hypothesis**
- ARIMAX struggles to add predictive power for short-horizon stock prices
- The evaluation highlights the importance of:
  - Proper baselines
  - Honest error comparison
  - Understanding model limitations

---

## Future Work

- ARIMA modeling on returns instead of price levels
- Residual diagnostics and stationarity tests
- Comparison with machine learning models
- Walk-forward validation