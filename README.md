# 🪙 Silver Prices Historical Data & 2026 Forecast

[![License: CC0](https://img.shields.io/badge/License-CC0-blue.svg)](https://creativecommons.org/publicdomain/zero/1.0/)
[![Python](https://img.shields.io/badge/Python-3.11+-green.svg)](https://python.org)
[![Data Source](https://img.shields.io/badge/Source-Yahoo_Finance-purple.svg)](https://finance.yahoo.com)

## 📋 Dataset Overview

This dataset contains **10 years (2016-2026)** of daily silver futures (SI=F) prices sourced from Yahoo Finance, along with machine learning-based price forecasts for Q1 2026.

## 📁 Files Included

| File                              | Description                                     | Records |
| --------------------------------- | ----------------------------------------------- | ------- |
| `silver_prices_historical.csv`    | Historical OHLCV data with technical indicators | 2,524   |
| `silver_prices_forecast_2026.csv` | Prophet model predictions for Jan-Mar 2026      | 85      |
| `Silver_Prices_EDA.ipynb`         | Complete Jupyter Notebook with EDA & ML models  | -       |

## 📊 Data Columns

### Historical Data (`silver_prices_historical.csv`)

| Column         | Type     | Description                            |
| -------------- | -------- | -------------------------------------- |
| Date           | datetime | Trading date                           |
| Open           | float    | Opening price (USD/oz)                 |
| High           | float    | Highest price of the day               |
| Low            | float    | Lowest price of the day                |
| Close          | float    | Closing price                          |
| Adj Close      | float    | Adjusted closing price                 |
| Volume         | int      | Trading volume                         |
| MA_50          | float    | 50-day moving average                  |
| MA_200         | float    | 200-day moving average                 |
| Daily_Return   | float    | Daily percentage return                |
| Year           | int      | Year                                   |
| Month          | int      | Month                                  |
| Volatility_30d | float    | 30-day rolling volatility (annualized) |

### Forecast Data (`silver_prices_forecast_2026.csv`)

| Column          | Type     | Description              |
| --------------- | -------- | ------------------------ |
| Date            | datetime | Forecast date            |
| Predicted_Price | float    | Model's price prediction |
| Lower_Bound     | float    | 95% CI lower bound       |
| Upper_Bound     | float    | 95% CI upper bound       |

## 🔬 Analysis Performed

1. **Exploratory Data Analysis (EDA)**
   - Price trends and patterns
   - Volume analysis
   - Volatility assessment
   - Seasonality detection

2. **Time Series Decomposition**
   - Trend extraction
   - Seasonal components
   - Residual analysis

3. **Machine Learning Models**
   - **Prophet**: Time series forecasting with yearly/weekly seasonality
   - **XGBoost**: Feature-based regression with lag features

4. **Model Evaluation**
   - MAE (Mean Absolute Error)
   - RMSE (Root Mean Square Error)
   - MAPE (Mean Absolute Percentage Error)

## 📈 Key Insights

- Silver showed strong upward trend, especially during economic uncertainty
- Seasonal patterns: Higher prices typically in Q4 and Q1
- 2026 shows elevated prices due to industrial demand (solar, EVs)
- XGBoost achieved ~2-5% MAPE on test data

## 🏷️ Tags

`silver` `commodities` `time-series` `forecasting` `machine-learning` `finance` `yahoo-finance` `precious-metals` `investing` `prophet` `xgboost` `EDA` `python`

## 📜 License

**CC0: Public Domain** - This dataset is free to use for any purpose.

## 👨‍💻 Author

**Eng. Hassan Jameel**  
Business & Economic Analyst | Data Scientist  
January 2026

---

## ❓ Frequently Asked Questions

### Q1: What is the data source?

> Data is fetched from Yahoo Finance using the `yfinance` Python library. The ticker symbol is `SI=F` (Silver Futures COMEX).

### Q2: Are there any missing values?

> The raw data may have gaps on non-trading days (weekends, holidays). These are handled by dropping NA values. The final dataset is complete with no missing values in the core OHLCV columns.

### Q3: What type of analysis was performed?

> - Exploratory Data Analysis (EDA)
> - Time Series Decomposition (trend, seasonality, residuals)
> - Feature Engineering (lag features, rolling statistics)
> - Machine Learning Forecasting (Prophet, XGBoost)

### Q4: How accurate are the predictions?

> The models achieve approximately:
>
> - MAE: ~0.5-1.5 USD
> - RMSE: ~1.0-2.0 USD
> - MAPE: ~2-5%
>
> (Actual values vary based on market conditions and data period)

### Q5: Can this data be used for commercial purposes?

> Yes! This dataset is released under CC0 (Public Domain). However, for actual trading decisions, please perform additional due diligence and consult financial advisors.

### Q6: What models work best for silver price prediction?

> Based on our analysis:
>
> - **Prophet** works well for capturing long-term trends and seasonality
> - **XGBoost** excels at short-term predictions using lag features
> - Ensemble methods combining both can improve results

### Q7: Why are silver prices rising in 2026?

> Several factors:
>
> 1. **Industrial demand surge** (solar panels, EVs, 5G)
> 2. **US Dollar weakness**
> 3. **Inflation hedging**
> 4. **Supply constraints** (mining disruptions)
> 5. **Investment demand** (ETF inflows)

### Q8: How often should this dataset be updated?

> For the most accurate forecasts, update monthly or weekly with fresh data from Yahoo Finance.

---

_If you found this dataset helpful, please consider upvoting on Kaggle!_ ⭐
