

**Author**: Olasubomi Precious Odujebe  
**Date**: August 2024  

## Project Overview

This project applies financial econometrics techniques to construct and optimize a 3-stock portfolio using **Microsoft (MSFT)**, **Amazon (AMZN)**, and **Google (GOOGL)**. The project analyzes the daily price series for these stocks over the past 15 years, tests for stationarity, calculates monthly returns, and applies a multivariate **GARCH-DCC model** to estimate dynamic correlations between the stock returns.

Finally, the forecasted returns and variance-covariance matrix are used to construct a **Sharpe Ratio-maximizing portfolio**, with the constraint that short-selling is not allowed.

## Key Features

1. **Data Collection**:  
   - Stock prices are sourced from Yahoo Finance for the period between 2009 and 2024.
   - The dataset is used to calculate monthly returns and analyze the price trends of MSFT, AMZN, and GOOGL.

2. **ADF Test for Stationarity**:  
   - The Augmented Dickey-Fuller (ADF) test is applied to check for stationarity in the monthly returns of each stock. All stocks exhibit stationary behavior in their returns.

3. **GARCH-DCC Model**:  
   - A multivariate **GARCH-DCC (1,1)** model is used to model the dynamic correlations between the three stocks.
   - This approach captures the time-varying volatility and correlations, providing valuable insights into the relationships between these stocks over time.

4. **Forecasting**:  
   - Forecasts of expected returns, variance-covariance matrix, and correlation matrix are produced using the GARCH-DCC model.
   - These forecasts are essential for the subsequent portfolio optimization process.

5. **Sharpe Ratio-Maximizing Portfolio**:  
   - Using the forecasted data, a portfolio is optimized to maximize the **Sharpe Ratio** under the constraint that short-selling is not allowed.
   - The portfolio assigns the highest weight to **Microsoft (MSFT)**, followed by **Amazon (AMZN)** and **Google (GOOGL)**.

## Files in the Repository

- `econometrics.md`: Contains the detailed markdown report, including data collection, ADF test results, GARCH-DCC model analysis, forecasting, and the Sharpe Ratio-maximizing portfolio.
- **Image Files**: Plots and figures of stock price trends and correlations (e.g., `amzn_plot.png`, `googl_plot.png`, `msft_plot.png`).
- **R Code**: R scripts used for data processing, model fitting, and forecasting.

## Results Summary

- **Optimal Portfolio Weights**:
  - **MSFT**: 63.39%
  - **AMZN**: 18.68%
  - **GOOGL**: 17.92%

- **Expected Portfolio Return**: 1.9578% per month  
- **Portfolio Variance**: 0.003235571  
- **Portfolio Standard Deviation**: 0.0569  
- **Sharpe Ratio**: 0.284413126

## How to Run

1. **Install Required R Packages**:
   - The analysis was performed using R. Make sure you have the following R packages installed:
     ```r
     install.packages(c("quantmod", "rugarch", "rmgarch", "quadprog", "tseries"))
     ```

2. **Run the R Code**:
   - Use the R scripts provided in the repository to replicate the analysis, including data collection, ADF tests, and the GARCH-DCC model.

## Conclusion

This project demonstrates how financial econometrics tools, such as the GARCH-DCC model, can be used to forecast asset returns and construct optimized portfolios. By maximizing the Sharpe Ratio and understanding the dynamic correlations between assets, investors can enhance their portfolio management strategies and make informed decisions.


