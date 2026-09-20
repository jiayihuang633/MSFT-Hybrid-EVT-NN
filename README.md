# Hybrid Gaussian–GPD Neural Network for Conditional MSFT Tail Risk

This project develops a neural-network-based hybrid model for conditional equity tail risk using Microsoft (MSFT) daily losses.

The model combines a Gaussian neural network for the central part of the conditional loss distribution with a generalized Pareto distribution (GPD) for extreme losses above an observation-specific 90% threshold. The resulting conditional distribution is used to estimate prediction intervals, Value-at-Risk (VaR), and Expected Shortfall (ES).

## Methodology

- Neural-network conditional Gaussian location-scale model
- Observation-specific 90% tail threshold
- Neural-network conditional GPD model for threshold exceedances
- Hybrid Gaussian–GPD conditional distribution
- Chronological training, validation, and test samples
- Out-of-sample calibration and residual diagnostics
- Conditional 95% and 99% VaR and Expected Shortfall

Predictors include lagged returns and log trading volumes from ten U.S. equities together with calendar effects.

## Repository Contents

- [`MSFT_Hybrid_EVT_NN_Report.pdf`](MSFT_Hybrid_EVT_NN_Report.pdf) — full research report
- [`MSFT_Hybrid_EVT_NN.Rmd`](MSFT_Hybrid_EVT_NN.Rmd) — complete R analysis and reproducible report source
- [`StockPriceDataset.csv`](StockPriceDataset.csv) — dataset used in the analysis

## Data

`StockPriceDataset.csv` contains the daily stock-market data used in the analysis and is included in this repository for reproducibility.

The dataset contains daily observations for ten U.S. equities from 2014 to 2023, including daily log returns and trading-volume information.
