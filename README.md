# Stock Market Analysis and Buy/Sell Signal Detection

This Python script analyzes historical stock market data for a given stock (in this case, Apple Inc. - AAPL) and generates buy/sell signals based on Simple Moving Averages (SMA) of 10-day and 25-day periods.

## Dataset Overview

The script utilizes historical stock data for AAPL obtained from a CSV file (`aapl.csv`). The dataset includes columns such as 'Date', 'Open', 'High', 'Low', 'Close', 'Volume', 'Dividends', and 'Stock Splits'. The analysis focuses on 'Adj Close Price', which accounts for dividends.

## Data Preprocessing

The following data preprocessing steps are performed:

1. **Creating a Copy**: A copy of the original dataset is created to preserve the integrity of the original data.
2. **Handling Missing Values**: The script checks for missing values in the dataset, but it appears there are none.
3. **Dropping Unnecessary Columns**: The 'Stock Splits' column, which does not contain relevant information, is dropped from the copy of the dataset.
4. **Calculating Adjusted Close Price**: A new column, 'Adj Close Price', is created by subtracting 'Dividends' from 'Close'.
5. **Converting Date Column**: The 'Date' column is converted to a datetime format for time-series analysis.

## Data Visualization

The script utilizes the `matplotlib` and `seaborn` libraries to visualize the data. Key visualizations include:

1. **Adj Close Price Over Time**: A line plot showing the adjusted close price of AAPL over time.
2. **Moving Averages**: Line plots overlaying the adjusted close price with 10-day and 25-day SMAs.
3. **Buy/Sell Signals**: Scatter plots indicating buy and sell signals based on SMA crossovers.

## Buy/Sell Signal Generation

The script generates buy and sell signals based on the following criteria:
- Buy Signal: When the 10-day SMA crosses above the 25-day SMA.
- Sell Signal: When the 10-day SMA crosses below the 25-day SMA.

The buy and sell signals are plotted on the chart for visual representation.

## Usage

1. Ensure you have installed the required libraries using `pip install seaborn`.
2. Run the Python script on your local environment, providing the path to the 'aapl.csv' dataset.
3. The script will generate visualizations of AAPL's stock data, including buy/sell signals.
```
