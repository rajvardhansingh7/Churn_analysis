# Churn Analysis and Customer Intelligence

A data analytics project that analyzes customer subscription and support data to understand churn patterns, revenue impact, and key drivers of customer retention.

## Overview

This project explores customer churn for a subscription-based business using SQLite data sources. It covers the full analytics workflow: data import, cleaning, feature engineering, KPI analysis, and visualization.

**Key outcomes:**
- Churn and retention rate calculation
- Revenue-at-risk and ARPU metrics
- Churn breakdown by plan type, geography, and subscription type
- Support metrics (escalations, complaints, CSAT) vs. churn correlation
- Visual dashboards using Matplotlib and Seaborn
- Pivot-table summaries for business reporting

## Project Structure

```
Churn_analysis/
├── churn_analysis.ipynb              # Main analysis notebook
├── customer_churn.db                 # SQLite database (3 tables)
├── customer_churn_data_raw.xlsx      # Raw Excel source data
├── exported_churn_data.csv           # Processed merged dataset (notebook output)
├── Data Analytics Project -Churn Analysis Report.pdf
├── requirements.txt
└── README.md
```

## Dataset

The database contains three tables:

| Table | Description |
|-------|-------------|
| `db_customer` | Customer demographics (name, country, state, gender, DOB) |
| `db_subscription` | Subscription details (plan, contract, charges, CLTV, churn score) |
| `db_support` | Support interactions (complaints, escalations, CSAT) |

## Getting Started

### Prerequisites

- Python 3.9+
- Jupyter Notebook or JupyterLab

### Installation

```bash
git clone https://github.com/rajvardhansingh7/Churn_analysis.git
cd Churn_analysis
pip install -r requirements.txt
jupyter notebook
```

Open `churn_analysis.ipynb` and run all cells.

### Data Setup

The project ships with `customer_churn.db` ready to use. If you need to rebuild it from scratch, the notebook includes a cell that converts `customer_churn_data_raw.xlsx` into the SQLite database.

## Analysis Sections

1. **Data Import** — Load tables from SQLite into pandas DataFrames
2. **Data Cleaning** — Rename columns, fix dtypes, standardize gender, impute missing values
3. **Feature Engineering** — Create churn flag, merge datasets, export CSV
4. **Data Analysis** — Churn rate, retention, ARPU, tenure, revenue at risk, support KPIs
5. **Visualization** — Time-series churn trends, bar charts, correlation heatmaps, pair plots
6. **Pivot Tables** — Multi-dimensional aggregations for reporting

## Tools & Libraries

- **Python** — pandas, NumPy, Matplotlib, Seaborn, SQLite3
- **Jupyter Notebook** — Interactive analysis and visualization

## Author

**Rajvardhan Singh**

## License

This project is for educational and portfolio purposes.
