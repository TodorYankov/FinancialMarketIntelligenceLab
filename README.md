# FinancialMarketIntelligenceLab

A Data Science project exploring Bitcoin prices in USD,
the S&P 500 index, and US Treasury yields.

## Research question

How do Bitcoin and S&P 500 returns and volatility vary
over time, and how are they associated with changes
in the interest-rate environment?

## Data sources

1. Yahoo Finance, accessed through yfinance:
   - BTC-USD: Bitcoin prices in US dollars.
   - ^GSPC: S&P 500 price index.
   - Downloaded coverage: January 2018–November 2026.

2. Federal Reserve Board, distributed through FRED:
   - DGS10: 10-year Treasury constant-maturity market yield.
   - Units: percent per annum.
   - https://fred.stlouisfed.org/series/DGS10

Exact coverage and download details are documented
in the notebook. Raw data are stored locally in data/raw.

Earlier exploratory inputs include Binance BTC/USDT data
and a Kaggle S&P 500 file. BTC/USDT is distinct from
BTC-USD; these inputs are retained as preliminary work
and are not silently combined with the USD analysis.

## Current progress

- Initial Bitcoin price exploration and daily returns.
- Preliminary Binance OHLCV validation.
- Downloaded BTC-USD and S&P 500 data from Yahoo Finance.
- Downloaded Treasury yields from an independent source.
- Recorded source information and initial coverage checks.

## Next steps

- Validate the newly downloaded datasets.
- Review missing observations and trading calendars.
- Account for different observation and closing times.
- Merge the datasets and analyze returns and volatility.
- Present visual evidence, conclusions and limitations.

Price forecasting is planned for the later Machine
Learning course and is not implemented in this stage.

## Project structure

- notebooks/01_data_exploration.ipynb — analysis notebook.
- data/raw/ — local source files.
- src/ — directory reserved for reusable code.
- tests/ — directory reserved for validation tests.

## Running the notebook

Required packages:
pandas, numpy, matplotlib, seaborn, yfinance.

From the project directory:

    cd notebooks
    jupyter notebook

The current notebook contains preliminary sections requiring
the earlier input files. Downloaded data and package versions
may change; reproducibility will be improved during development.

## Limitations

This is an exploratory educational project.
Associations do not establish causation.
The S&P 500 price index does not include dividend reinvestment.
Treasury yields are interest-rate levels, not investment returns.
No forecasting performance or trading profitability is claimed.