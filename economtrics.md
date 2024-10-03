# Financial Econometrics 

**Author**: Olasubomi Precious Odujebe  
**Date**: August 2024  

## Introduction
This project involves building a financial model using GARCH-DCC for the analysis of stock price correlations and volatilities for Microsoft, Amazon, and Google. It includes calculating returns, running stationarity tests, and forecasting using the GARCH model.

## Data Collection
```r
# Set time frame -- 2009-2024
date_from = as.Date("2009-07-18")
date_to = as.Date("2024-07-17")

# Download data for 3 stocks
getSymbols('MSFT', from = date_from, to = date_to)
getSymbols('AMZN', from = date_from, to = date_to)
getSymbols('GOOGL', from = date_from, to = date_to)

# Plot daily price series
chartSeries(MSFT)
chartSeries(AMZN)
chartSeries(GOOGL)

