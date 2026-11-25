# FinancialMarketIntelligenceLab

An exploratory Data Science research project investigating the relationship between Bitcoin (BTC-USD), the S&P 500 index, and the US interest-rate environment.

## Research question

How do Bitcoin and S&P 500 returns and volatility vary over time, and how are they associated with changes in the interest-rate environment?

## Research objectives

- Explore historical financial time series and daily returns.
- Assess data quality, coverage, consistency, and missing observations.
- Investigate returns, volatility, and relationships between financial variables.
- Apply statistical hypothesis testing to financial research questions.
- Communicate findings through visualizations, statistical evidence, and explicit limitations.

## Data sources

| Source | Series | Description |
| --- | --- | --- |
| [Yahoo Finance](https://finance.yahoo.com/) | BTC-USD | Bitcoin prices in US dollars |
| Yahoo Finance | ^GSPC | S&P 500 price index |
| [FRED / Federal Reserve Board](https://fred.stlouisfed.org/series/DGS10) | DGS10 | 10-year Treasury constant-maturity market yield, percent per annum |

The Yahoo Finance data were downloaded through `yfinance`, with coverage from January 2018 to November 2026. Exact coverage and download details are documented in the notebooks. Raw data are stored locally in `data/raw/`.

Earlier exploratory inputs include Binance BTC/USDT data and a Kaggle S&P 500 file. BTC/USDT is distinct from BTC-USD. These preliminary inputs are not silently combined with the USD analysis.

## Research workflow

| Stage | Notebook | Focus |
| --- | --- | --- |
| 01 | [Data Exploration](notebooks/01_data_exploration.ipynb) | Initial exploration, descriptive analysis, daily returns, and data acquisition |
| 02 | [Market Data Validation](notebooks/02_market_data_validation.ipynb) | Financial data quality and validation |
| 03 | Hypothesis Testing | Statistical investigation of financial research questions |

The notebooks form a progressive research workflow, from data exploration and validation to statistical inference.

The statistical methodology considers null and alternative hypotheses, significance levels, p-values, confidence intervals, test assumptions, and practical interpretation. The choice of statistical test depends on the research question and the properties of the data.

## Project structure

```text
FinancialMarketIntelligenceLab/
├── data/
│   └── raw/       # Local source data
├── notebooks/     # Exploration, validation, and hypothesis testing
├── src/           # Reserved for reusable Python code
├── tests/         # Reserved for validation tests
└── README.md
```

## Technologies

- Python and Jupyter Notebook
- pandas and NumPy — data processing and numerical analysis
- Matplotlib and seaborn — visualization and exploratory data analysis
- yfinance — financial data acquisition

## Running the notebooks

From the project directory, install the baseline dependencies:

```bash
python -m pip install pandas numpy matplotlib seaborn yfinance scipy notebook
```

Launch Jupyter:

```bash
cd notebooks
jupyter notebook
```

Run the notebooks in numerical order. Some preliminary sections require earlier input files. The dependency list is a starting point rather than a verified, version-pinned environment; reproducibility will be improved during development.

## Project status

**Updated: 25 November 2026**

- [x] Initial data exploration and daily returns
- [x] Preliminary Binance OHLCV validation
- [x] Financial data acquisition and source documentation
- [x] Market data validation notebook
- [x] Hypothesis testing notebook
- [ ] Consolidate visual evidence, statistical findings, and limitations
- [ ] Improve reproducibility and reusable code

## Future development

- Review missing observations, trading calendars, and differences in observation and closing times as needed.
- Refine dataset alignment and the analysis of returns and volatility.
- Consolidate statistical results and assess their robustness.
- Evaluate additional visualization and image-based techniques where they serve the research question.
- Explore forecasting using Machine Learning in a later course stage, with appropriate time-aware validation.

Price forecasting is not implemented at this stage.

## Limitations

- This is an exploratory educational research project, not financial advice.
- Statistical associations do not establish causation.
- Bitcoin and traditional financial markets have different trading calendars and observation times.
- The S&P 500 price index does not include dividend reinvestment.
- Treasury yields are interest-rate levels, not investment returns.
- No forecasting performance or trading profitability is claimed.
