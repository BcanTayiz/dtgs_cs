# Stock Market Prediction Report

## Executive Summary
This report provides an overview of the stock market prediction model's performance, highlighting its accuracy and ability to explain variability in stock prices. Notably, the model achieved low RMSE and MAPE values, indicating high accuracy in its predictions.

## Introduction
This report outlines the process of predicting stock market prices using historical data and technical indicators. The analysis leverages machine learning techniques, specifically the Linear Regression algorithm, to forecast the next day's closing price for a given stock. Stock market prediction is significant as it aids investors in making informed decisions.

## Methodology
The data was collected through the `yfinance` library for the specified ticker symbol (e.g., 'NVDA') from January 1, 2015, to January 1, 2025. The analysis involved data preprocessing, feature engineering, and model selection. The libraries used include `pandas`, `numpy`, and `matplotlib`.

## Data Preprocessing and Feature Engineering
- **Data Loading**: Stock market data was loaded using the `yfinance` library for the specified ticker symbol (e.g., 'NVDA').
- **Data Cleaning**: Rows with missing values were removed to ensure the dataset was complete for analysis. Outliers were also handled to improve data quality.
- **Technical Indicators**: Several indicators were calculated, including:
  - **Simple Moving Averages (SMA)**: Helps identify trends by smoothing out price data.
  - **Exponential Moving Averages (EMA)**: Gives more weight to recent prices, making it more responsive to new information.
  - **Relative Strength Index (RSI)**: Measures the speed and change of price movements to identify overbought or oversold conditions.
  - **MACD** and its components: Helps in identifying momentum and trend direction.
  - **Bollinger Bands**: Indicates volatility and potential price movement.
  - **Average True Range (ATR)**: Measures market volatility.
- **Lagged Features**: Lagged features of the closing price were created to allow the model to use past values for predicting future prices, enhancing its predictive capability.

## Model Selection and Evaluation
- **Model Used**: `Ridge Best Model` was selected for its effectiveness in regression tasks. Exploring models like XGBoost could further enhance accuracy.
- **Evaluation Metrics**: 
  - **Root Mean Squared Error (RMSE)**: Measures the average magnitude of the errors between predicted and actual values.
  - **Mean Absolute Percentage Error (MAPE)**: Expresses accuracy as a percentage, making it easy to interpret.
  - **R-squared (Coefficient of Determination)**: Indicates the proportion of variance in the dependent variable that can be explained by the independent variables.

## Findings and Recommendations
The model performed well, with low RMSE and MAPE values, suggesting high accuracy. The R-squared value indicated a good fit, demonstrating the model's ability to explain the variability in stock prices. Recommendations include continuous monitoring of the model, exploring other machine learning algorithms for improved accuracy, and considering hyperparameter tuning.

## Visual Examples
Visual representations of the data and predictions, such as plots of the closing prices, can be found in the `starter.ipynb`. For example, the following code generates a plot of the actual closing prices:
```python
plt.plot(data['Close'], label='Actual Closing Prices', color='blue')
```
This plot allows for a visual assessment of the stock's performance over time.

## Conclusion
This notebook serves as a foundation for stock market prediction using historical data and machine learning techniques. Future work could involve optimizing the model, exploring additional stocks, and incorporating more features to enhance predictive performance.