# Demand Forecasting Suite

This repository provides a suite of forecasting tools for weekly retail demand, hotel occupancy, and agricultural supply across the **UAE**, **Australia**, and **New Zealand**. Each notebook demonstrates three models—ARIMA, Exponential Smoothing, and XGBoost—and evaluates accuracy using MAPE.

## Repository Structure
- `notebooks/`: Forecasting notebooks for each use case.
- `charts/`: Forecast comparison plots and residual/backtest visuals.
- Synthetic CSVs: `retail_demand_uae.csv`, `hotel_occupancy_au.csv`, `agri_supply_nz.csv`.

## When to Use Which Model

| Model | Suitable For | Pros | Cons |
|------|--------------|------|------|
| **ARIMA** | Stable demand with seasonality | Interpretability, simple tuning | Assumes linearity |
| **Exponential Smoothing** | Short-term forecasting | Captures trends quickly | May lag on sudden shifts |
| **XGBoost** | Complex, non-linear patterns | Handles exogenous variables | Requires feature engineering |

MAPE and SMAPE metrics are reported within each notebook to guide selection.

## Industry Relevance

- **Retail/FMCG (UAE)**: Forecasting weekly demand helps optimize inventory and reduce stockouts.
- **Tourism/Hospitality (Australia)**: Predicting hotel occupancy supports revenue management and staffing decisions.
- **Agriculture (New Zealand)**: Anticipating seasonal supply ensures efficient logistics and market pricing.

## How to Run

Open any notebook in `notebooks/` and run all cells. Datasets are stored in the repository for convenience.

![UAE Retail Forecast](./charts/uae_retail_forecast.png)

Licensed under the MIT License.
