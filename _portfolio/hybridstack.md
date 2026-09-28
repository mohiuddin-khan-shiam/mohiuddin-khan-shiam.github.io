---
title: "HybridStack: Interpretable Macro-Financial Forecasting Framework"
excerpt: "Multi-tier hybrid ensemble combining gradient-boosted decision trees with regularized meta-regressors, achieving 0.0006 test RMSE with policy-grade SHAP/LIME interpretability on high-frequency indicators."
collection: portfolio
date: 2026-01-01
permalink: /portfolio/hybridstack/
---

<div class="project-header-box">
  <span class="badge badge--tools"><i class="fa-solid fa-chart-pie"></i> Macro-Financial Forecasting</span>
  <span class="badge badge--tools"><i class="fa-solid fa-layer-group"></i> Hybrid Ensembles & Bayesian Optimization</span>
  <span class="badge badge--tools"><i class="fa-solid fa-magnifying-glass-chart"></i> SHAP & LIME Interpretability</span>
  <span class="badge badge--elsevier"><i class="fa-solid fa-book-journal-whills"></i> Published in Elsevier Array (Q1)</span>
</div>

### Project Overview

**HybridStack** is an explainable machine learning forecasting engine engineered to predict macroeconomic indices and high-frequency inflation dynamics with extreme numerical fidelity and transparent attribution.

### Architectural Innovations

- **Multi-Tier Ensemble Architecture**: Blends gradient-boosted decision trees (`XGBoost`, `LightGBM`, `CatBoost`) feeding into regularized meta-regressors (Ridge, ElasticNet) to prevent overfitting across volatile economic regimes.
- **Bayesian Hyperparameter Search**: Multi-dimensional Bayesian tuning evaluating over 10 high-frequency macro-financial time-series sources.
- **Superior Predictive Accuracy**: Recorded an empirical held-out test **RMSE of 0.0006**, outstripping conventional econometric models (ARIMA, VAR) and deep recurrent baselines.
- **Policy-Grade Explainability**: Leverages TreeSHAP, Kernel SHAP, LIME, and Partial Dependence Plots (PDP) to quantify exact marginal feature impacts, providing institutional transparency for central banks and economic policymakers.

[Read Published Journal Paper (Elsevier)](https://doi.org/10.1016/j.array.2026.101003){: .btn .btn--primary target="_blank" rel="noopener noreferrer"}
