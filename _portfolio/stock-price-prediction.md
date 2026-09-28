---
title: "Comparing Deep Learning and Statistical Models for Stock Price Prediction"
excerpt: "Empirical time-series forecasting evaluating Long Short-Term Memory (LSTM) recurrent neural networks against classical ARIMA statistical models on historical equity data."
collection: portfolio
date: 2024-06-01
permalink: /portfolio/stock-price-prediction/
---

<div class="project-header-box">
  <span class="badge badge--tools"><i class="fa-solid fa-chart-line"></i> Time-Series Forecasting</span>
  <span class="badge badge--tools"><i class="fa-solid fa-brain"></i> LSTM vs. ARIMA</span>
  <span class="badge badge--code"><i class="fab fa-github"></i> <a href="https://github.com/mohiuddin-khan-shiam/Stock-Price-Prediction" target="_blank" rel="noopener noreferrer">GitHub Repository</a></span>
</div>

### Project Overview

This research project conducts an empirical comparative analysis between deep recurrent neural network architectures and classical statistical econometric methodologies for financial equity forecasting. 

Focusing on historical equity price trends of **HP Inc. (NYSE: HPQ)**, the study evaluates the fundamental trade-offs between model complexity, non-linear feature capture, stationarity transformations, and generalization stability.

### Technical Highlights

- **Data Pipeline**: Cleaned, decomposed, and analyzed daily price action data; assessed stationarity via Augmented Dickey-Fuller (ADF) tests and evaluated autocorrelation/partial autocorrelation (ACF/PACF) profiles.
- **Statistical Modeling (ARIMA)**: Built autoregressive integrated moving average baselines, optimizing $(p, d, q)$ order parameters to model linear autoregressive tendencies and residual variance.
- **Deep Learning (LSTM)**: Implemented recurrent neural network layers with gating units capable of learning long-range temporal dependencies without vanishing gradients across sequences.
- **Model Evaluation**: Compared models using Mean Squared Error (MSE), Root Mean Squared Error (RMSE), and Mean Absolute Percentage Error (MAPE), highlighting the scenarios where recurrent sequence modeling outperforms traditional econometric baselines.

[View Source Code on GitHub](https://github.com/mohiuddin-khan-shiam/Stock-Price-Prediction){: .btn .btn--primary target="_blank" rel="noopener noreferrer"}
