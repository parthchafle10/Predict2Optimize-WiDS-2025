# Predict2Optimize – WiDS 2025

This repository contains my work for **Predicting Market Dynamics for Data-Driven Portfolio Optimization**, completed as part of **WiDS 2025 (Project ID 48)**.

The project follows an end-to-end quantitative finance pipeline, progressing from financial data analysis and return prediction to portfolio optimization and backtesting under realistic constraints.

---

## Project Structure

The repository is organized by weeks:

- **Week 1:** Exploratory financial data analysis  
  - Price trends, returns, volatility  
  - Return distributions and aggregational Gaussianity  

- **Week 2:** Return prediction and evaluation  
  - Feature engineering using lagged returns and rolling statistics  
  - Baseline models, linear regression, and Random Forest  
  - Time-series-aware evaluation to avoid look-ahead bias  

- **Week 4:** Portfolio optimization  
  - Markowitz mean-variance optimization  
  - Practical constraints (long-only, leverage, position limits)  
  - Robust optimization under return uncertainty  

- **Week 5:** Predict-to-optimize backtesting  
  - Rolling prediction → optimization → rebalance framework  
  - Transaction costs and rebalancing effects  
  - Comparison of equal-weight, Markowitz, and robust portfolios  

---

## Key Concepts

- Financial return analysis and stylized facts  
- Time-series prediction and walk-forward validation  
- Convex optimization using CVXPY  
- Robust portfolio optimization  
- Risk-adjusted performance evaluation  

---

## Notes

- All models and backtests use strictly past data (no look-ahead bias).
- Results are intended for educational purposes only.
