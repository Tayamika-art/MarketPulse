**Overview**

MarketPulse is a quantitative financial data analysis project built with Python.

The project analyzes historical stock market data to explore investment returns, volatility, correlations, and basic forecasting methods.

**Assets Analyzed**

- Apple (AAPL)
- Microsoft (MSFT)
- NVIDIA (NVDA)
- S&P 500 ETF (SPY)

**Technologies Used**

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Yahoo Finance (yfinance)
- Jupyter Notebook

**Analysis Performed**

1. Historical Performance: Compared adjusted stock prices and calculated cumulative returns.
2. Daily Returns: Measured average daily returns for each asset.
3. Volatility: Compared how much each asset's returns fluctuated.
4. Correlation Analysis: Examined relationships between the four assets.
5. Yearly Performance: Compared returns and volatility across 2024, 2025, and 2026.
6. Forecasting: Tested a 20-day moving average and a linear regression model.

**Forecasting Methodology**

The linear regression model focused on AAPL.

It used:
- Previous-day AAPL returns.
- Five-day average returns.
- Twenty-day average returns.
- Twenty-day volatility.
- Previous-day SPY returns.

The dataset was split chronologically:
- 80% for training.
- 20% for testing.

The model was evaluated against a zero-return baseline using Mean Absolute Error (MAE) and Root Mean Squared Error (RMSE).

**Key Findings**

- AAPL had the highest cumulative return during the analyzed period.
- NVDA showed the highest daily volatility overall.
- SPY had the lowest daily volatility overall.
- NVDA and SPY had the strongest positive return correlation.
- The best return-to-volatility ratio varied across the years.

**Forecasting Results**

The AAPL linear regression model produced the following test results:

| Metric | Result |
|---|---:|
| Training observations | 384 |
| Testing observations | 96 |
| Linear Regression MAE | 1.197% |
| Zero Forecast MAE | 1.206% |
| Directional Accuracy | 45.83% |

The linear regression model slightly outperformed the zero-return baseline in MAE, with approximately 0.75% relative improvement.

However, its directional accuracy was below 50%, showing that it struggled to predict whether AAPL would rise or fall.

**Limitations**

- The analysis uses historical data, which does not guarantee future performance.
- The forecasting model is relatively simple.
- The model was tested on one holdout period.
- The small improvement over the baseline does not establish reliable predictive power.

**How to Run**

1. Clone or download this repository.
2. Install the required libraries:

   '''bash'''
   pip install pandas numpy matplotlib seaborn yfinance scikit-learn jupyter

**Project Structure**

MarketPulse/
└── market_analysis.ipynb

 **Author:** Tayamika Phiri

