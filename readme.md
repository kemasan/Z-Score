# Stock Price Analysis with Rolling Z-Scores

## Overview
This project analyzes stock price trends using rolling Z-scores to identify potential buy and sell signals based on statistical deviations. It utilizes historical stock data from Yahoo Finance, computes rolling Z-scores for different window sizes, and visualizes the results.

## Features
- Fetches historical stock data using the Yahoo Finance API
- Computes rolling Z-scores for multiple time windows (30, 60, and 90 days)
- Identifies buy/sell signals based on a predefined Z-score threshold
- Visualizes stock prices and corresponding Z-score trends

## Technologies Used
- Python
- Pandas
- Matplotlib
- yFinance

## Installation
Clone the repository:
```git clone <repository_url>```

Install required dependencies:
```pip install pandas matplotlib yfinance```

## Usage
Modify the constants in the script to change stock ticker and analysis period:
```
TICKER_SYMBOL = 'ESTC'
START_DATE = '2020-01-01'
ENDING_DATE = '2025-01-31'
```
Run the script:
```python script.py```

The output will display stock price trends and Z-score analysis, highlighting buy/sell signals.

## How It Works
- Fetching Stock Data: Uses yfinance to retrieve daily historical stock prices.
- Rolling Z-Score Computation: Calculates rolling means and standard deviations for multiple windows, then computes Z-scores as: z_score = (price - rolling_mean) / rolling_std
- Signal Identification: Marks buy/sell signals when the Z-score crosses below or above the threshold (-2, 2).
- Visualization: Displays stock price trends and overlays Z-scores for analysis.

### Z-Score Calculation and Trading Signals
The Z-score calculation quantifies how far a stock's price has deviated from its typical behavior over the past 5 years. By applying this method to multiple rolling windows, we can identify both short-term anomalies and Z-scores that exceed thresholds such as ±1.5 or ±2.0, acting as alerts for potential action. Adjusting the Z-score threshold can help to align the signals with the chosen trading strategy.

### Above the threshold: 
Indicates a potential sell point due to overvaluation.
### Below the threshold: 
Indicates a potential buy signal when the stock is undervalued.

### Notes: 
- Ensure you have an active internet connection to fetch stock data.
- The Z-score threshold and window sizes can be adjusted to fit different trading strategies.



