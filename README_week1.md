# Predict2Optimize — WiDS 2025  
**Predicting Market Dynamics for Data-Driven Portfolio Optimization**

## Overview
In this project, you will build a simple end-to-end pipeline:

> **data → features → prediction → optimization → backtesting**

By Week 5, you will be able to produce predicted returns, optimize a portfolio using those predictions, and evaluate performance over time.

---

# Week 1 — Financial Data & Feature Extraction
**Goals**
- Become familiar with NumPy, Pandas, Matplotlib.
- Download daily price data using `yfinance`.
- Compute daily returns and construct basic rolling features.

**Tasks**
- Load and inspect price data.  
- Handle missing values.  
- Compute log returns.  
- Build simple rolling features (5-day return, 20-day volatility, 10-day momentum).  
- Visualize prices, returns, and features.

---

# Week 2 — Baseline Models and Linear Predictors
**Goals**
- Predict next-day returns using simple regression models.
- Establish performance baselines.

**Tasks**
- Use time-ordered train/test splits.  
- Implement:  
  - mean predictor (baseline)  
  - linear or ridge regression  
  - optional tree-based model (e.g., XGBoost)  
- Evaluate using standard regression metrics.

---

# Week 3 — Neural Networks and Walk-Forward Prediction
**Goals**
- Train a small MLP to predict returns.
- Set up a rolling, walk-forward evaluation loop.

**Tasks**
- Implement a small feedforward network in PyTorch.  
- Normalize features; apply early stopping.  
- Perform walk-forward prediction:  
  **train on past → predict next segment → advance window → repeat**.

---

# Week 4 — Portfolio Optimization
**Goals**
- Convert predicted returns into portfolio weights via Markowitz optimization.
- Experiment with different covariance estimates.

**Tasks**
- Estimate covariance of returns.  
- Use `cvxpy` to solve long-only Markowitz optimization.  
- Compare to PyPortfolioOpt’s implementation.  
- Analyze how weights change under different covariance estimators.

---

# Week 5 — Integration and Final Backtest
**Goals**
- Combine your predictor with your optimizer into a full pipeline.
- Evaluate the strategy over time and interpret results.

**Tasks**
- For each period:  
  **predict returns → compute optimal weights → update portfolio value**  
- Plot cumulative returns.  
- Plot an efficient frontier for a chosen date.  
- Write a short summary of results and limitations.

---

# References
- NumPy, Pandas, Matplotlib documentation  
- Scikit-Learn documentation  
- PyTorch quickstart  
- [`cvxpy` documentation](https://www.cvxpy.org/tutorial/index.html)  
- [PyPortfolioOpt documentation](https://pyportfolioopt.readthedocs.io/en/latest/)  
- [The Portfolio Optimization Book](https://portfoliooptimizationbook.com/) — Ch. 1–2–3 (Weeks 1–2), Ch. 6–8 (Weeks 4–5)  
- *Successful Algorithmic Trading* (general reference)  
- JAIR (2024):  
  **Decision-Focused Learning: Foundations, State of the Art, Benchmark and Future Opportunities**  
  — especially p. 40 for the Predict-to-Optimize portfolio framing.
