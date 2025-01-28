# Stock Market Prediction Report

## Introduction
This report outlines the process of predicting stock market prices using historical data and technical indicators. The analysis leverages machine learning techniques, specifically the Linear Regression algorithm, to forecast the next day's closing price for a given stock.

## 1. Data Preprocessing Steps
- **Data Loading**: Stock market data was loaded using the `yfinance` library for the specified ticker symbol (e.g., 'NVDA') from January 1, 2015, to January 1, 2025).
- **Data Cleaning**: Rows with missing values were removed to ensure the dataset was complete for analysis.
- **Feature Engineering**: Several technical indicators were calculated, including:
  - **Simple Moving Averages (SMA)**: `SMA_20`, `SMA_50`
  - **Exponential Moving Averages (EMA)**: `EMA_20`, `EMA_50`
  - **Relative Strength Index (RSI)**
  - **MACD** and its components
  - **Bollinger Bands**
  - **Average True Range (ATR)**
  
These indicators provide additional context for predicting stock prices.

## 2. Technical Indicators and Features Used
- **Technical Indicators**: 
  - Indicators such as SMA and EMA help identify trends and potential reversal points.
  - RSI provides insights into overbought or oversold conditions.
  - MACD helps in identifying momentum and trend direction.
  - Bollinger Bands indicate volatility and potential price movement.
  - ATR measures market volatility.
- **Lagged Features**: 
  - Lagged features of the closing price were created to allow the model to use past values for predicting future prices.

## 3. Model Selection Process
- **Model Used**: `LineerREgression` was selected for its effectiveness in regression tasks and ability to handle various data types.
- **Hyperparameter Tuning**: Hyperparameters were tuned using cross-validation techniques to optimize model performance.

## 4. Evaluation Metrics
To assess the performance of the stock market prediction model, we utilized the following evaluation metrics:

- **Root Mean Squared Error (RMSE)**: Measures the average magnitude of the errors between predicted and actual values. It is sensitive to outliers and provides a clear indication of the model's predictive accuracy in the same units as the target variable.

- **Mean Absolute Percentage Error (MAPE)**: Expresses accuracy as a percentage, making it easy to interpret. It is scale-independent and useful for comparing performance across different datasets.

- **R-squared (Coefficient of Determination)**: Indicates the proportion of variance in the dependent variable that can be explained by the independent variables. It provides insight into the model's explanatory power.

These metrics were selected because they offer a comprehensive view of the model's performance, allowing us to measure error, accuracy, and the model's ability to explain variance in stock prices.

## 5. Evaluation Results and Insights
The evaluation results indicated that the model performed well, with low RMSE and MAPE values, suggesting high accuracy. The R-squared value indicated a good fit, demonstrating the model's ability to explain the variability in stock prices.

## Conclusion
This section summarizes the key findings and implications of the analysis, highlighting the importance of the chosen features and model in predicting stock prices.