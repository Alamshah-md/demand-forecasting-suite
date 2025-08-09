# Demand Forecasting Suite

This suite provides time-series forecasting examples using **ARIMA** and **XGBoost** for synthetic datasets:
- Retail demand (UAE)
- Hotel occupancy (AU)
- Seasonal agri supply (NZ)

## Problem → Approach → Results
For each case we:
1. Generate synthetic weekly data capturing trends and seasonality.
2. Split the series into 80% training and 20% test segments.
3. Fit an ARIMA model (1,1,1) and an XGBoost regression with lag features.
4. Evaluate performance using MAPE and SMAPE metrics and visualize forecasts & residuals.

## When to use which model
- **ARIMA**: Best for univariate series with clear linear trends and seasonality.
- **XGBoost**: Handles nonlinear patterns and interactions when provided with lagged features. Useful when seasonality isn’t strictly sinusoidal.

## Results summary
| Dataset | MAPE (ARIMA) | SMAPE (ARIMA) | MAPE (XGBoost) | SMAPE (XGBoost) | Notes |
|--------|--------------|---------------|---------------|-----------------|------|
| retail_demand_uae | 6.29% | 6.26% | 7.92% | 8.28% | synthetic weekly series |
| hotel_occupancy_au | 24.16% | 27.80% | 10.47% | 11.16% | synthetic weekly series |
| agri_supply_nz | 38.75% | 30.84% | 12.58% | 12.86% | synthetic weekly series |

## Files
- `data/`: CSVs for each case
- `charts/`: Forecast & residual plots for each model and dataset
- `notebooks/analysis.ipynb`: Example notebook performing ETL, model fitting, and charting

## Industry relevance and metrics
- **Retail/FMCG (UAE)**: Anticipate weekly demand to optimize inventory and promotions.
- **Tourism/Hospitality (AU)**: Forecast occupancy to set room rates and staffing levels.
- **Agriculture (NZ)**: Project seasonal supply to plan storage and distribution.

Models are evaluated using **MAPE** (Mean Absolute Percentage Error) and **SMAPE** (Symmetric MAPE). Lower values indicate better accuracy.
