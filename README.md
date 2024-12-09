
# **EMA-Based Trading Strategy**

## **Overview**
This repository provides an implementation of an **Exponential Moving Average (EMA) crossover trading strategy**, designed for backtesting and evaluating the performance of stock portfolios. The project focuses on:
- Generating buy/sell signals based on EMA crossovers.
- Backtesting the strategy using historical stock data.
- Calculating and analyzing performance metrics to evaluate the strategy's effectiveness.

The primary goal is to showcase the practical application of quantitative trading principles and evaluate the strategy's risk-adjusted returns.

---

## **Project Contents**
### **1. Data Folder**
Contains raw and processed data files, including:
- Historical stock price data (adjusted closing prices).
- Daily returns for individual stocks and the portfolio.

### **2. Scripts**
Includes Python scripts for:
- Fetching historical stock data from Yahoo Finance.
- Implementing the EMA trading strategy.
- Calculating performance metrics and analyzing results.

### **3. Results Folder**
Contains the outputs of the analysis, such as:
- Strategy returns and cumulative portfolio performance.
- Long and short position signals for each stock.
- Key performance metrics, including Sharpe ratio and maximum drawdown.

### **4. Documentation**
This README file, explaining the structure, usage, and key findings.

---

## **Features**
### **1. Trading Strategy**
The trading strategy uses two Exponential Moving Averages (EMAs) with different time horizons:
- **Short-term EMA**: Captures recent price trends.
- **Long-term EMA**: Identifies overall market direction.
- **Signals**:
  - **Buy**: Triggered when the short-term EMA crosses above the long-term EMA.
  - **Sell**: Triggered when the short-term EMA crosses below the long-term EMA.
  - No signal is generated when the EMAs overlap.

### **2. Performance Metrics**
The strategy evaluates several performance measures, including:
- **Average Return**: Mean daily return of the portfolio.
- **Volatility**: Standard deviation of daily returns.
- **Sharpe Ratio**: Risk-adjusted return measure, calculated as return-to-volatility.
- **Sortino Ratio**: Like the Sharpe ratio but penalizes only downside volatility.
- **Maximum Drawdown**: The largest peak-to-trough decline during the backtesting period.
- **Hit Ratio**: Measures the accuracy of trading signals.

### **3. Advanced Features**
- **Out-of-Sample Testing**: Splits the data into training (in-sample) and testing (out-of-sample) periods to validate the strategy.
- **Optimization**: Allows adjustment of EMA parameters (e.g., short/long window lengths) to improve risk-adjusted returns.
- **Volatility Management**: Implements techniques to reduce portfolio volatility, such as diversification and risk-parity weighting.

---

## **Usage Instructions**
### **1. Data Fetching**
The project retrieves historical stock data using Yahoo Finance's API. Users can customize:
- The number of stocks in the portfolio.
- The time horizon for analysis.

### **2. Strategy Implementation**
The EMA crossover strategy determines which stocks to buy (long) and sell (short) at each trading period. It tracks portfolio positions and calculates daily returns.

### **3. Performance Analysis**
The project calculates performance metrics to evaluate the strategy's effectiveness. Users can explore:
- How the strategy performed during different market conditions.
- The contribution of long vs. short positions to overall returns.

---

## **Key Takeaways**
### **1. Flexibility**
The project is designed for extensibility, allowing users to:
- Experiment with different technical indicators.
- Adjust parameters for EMAs and other strategy components.

### **2. Risk Management**
The focus on reducing volatility rather than simply increasing returns helps boost the Sharpe ratio, demonstrating the importance of robust portfolio construction.

### **3. Practical Insights**
This project highlights:
- The trade-offs between risk and return.
- The significance of backtesting and out-of-sample validation in quantitative trading.
