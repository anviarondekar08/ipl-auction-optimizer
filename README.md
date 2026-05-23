# IPL Auction Budget Optimizer

> Applying financial portfolio optimization logic to IPL auctions —  
> finding undervalued players the same way fund managers find undervalued stocks.

[![Python](https://img.shields.io/badge/Python-3.11-blue)]()
[![PuLP](https://img.shields.io/badge/Optimizer-PuLP-green)]()
[![Status](https://img.shields.io/badge/Status-In%20Progress-orange)]()

## The Core Idea

IPL franchises have a fixed budget (₹90 Cr) and must build 
the highest-performing squad possible. This is identical to 
a portfolio manager's problem — maximize return per rupee 
under capital constraints.

This project applies three financial concepts to cricket auctions:

| Finance Concept       | Cricket Translation                          |
|-----------------------|----------------------------------------------|
| Value investing       | Performance per crore — finding underpriced players |
| Sharpe Ratio          | Consistent performers vs one-season wonders  |
| Portfolio optimization| Constrained LP to build the optimal XI       |

## What It Does

- **Value scoring** — weighted formula for batting/bowling 
  performance, normalized and divided by auction price
- **Constrained optimizer** — PuLP linear programming with 
  real constraints (budget cap, overseas limit, role balance)
- **Risk layer** — consistency score analogous to Sharpe Ratio; 
  compares a high-ceiling team vs a low-variance team
- **Backtesting** — train on 2019–2021, evaluate predictions 
  against actual 2022 performances

## Key Findings
*Will update as analysis is completed*

## Tech Stack

| Tool | Purpose |
|------|---------|
| pandas | Data cleaning, merging, feature engineering |
| PuLP | Linear programming optimizer |
| seaborn / plotly | Visualization |
| scipy | Statistical analysis |
| Streamlit | Interactive dashboard |

## Project Structure
```
ipl-auction-optimizer/
├── data/
│   ├── raw/          # Original Kaggle datasets
│   └── processed/    # Cleaned master_df
├── notebooks/
│   ├── 01_cleaning.ipynb
│   ├── 02_eda.ipynb
│   ├── 03_optimizer.ipynb
│   └── 04_backtesting.ipynb
├── src/
│   ├── value_scorer.py
│   └── optimizer.py
├── app.py            # Streamlit dashboard
└── requirements.txt
```

## Live Demo
*Streamlit dashboard link — coming Week 6*

