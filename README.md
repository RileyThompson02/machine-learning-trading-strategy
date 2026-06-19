# Machine Learning-Based Multi-Asset Trading Strategy

## Overview

This project develops a machine learning-driven trading strategy that uses technical indicators to predict short-term price movements across multiple equities.

A Random Forest classifier is trained on engineered features, and its predictions are converted into trading signals. The strategy is evaluated through backtesting, including transaction cost modeling.

---

## Features

* Multi-asset analysis across several equities
* Technical indicator-based feature engineering
* Machine learning model (Random Forest) for prediction
* Backtesting framework with transaction costs
* Performance evaluation using classification metrics and Sharpe ratio
* Visualization of strategy vs. market performance

---

## Technologies Used

* Python
* Pandas, NumPy
* Scikit-learn
* Matplotlib
* yFinance API

---

## Methodology

### 1. Data Collection

Historical OHLCV data is retrieved using the yFinance API for multiple stocks.

### 2. Feature Engineering

The following technical indicators are constructed:

* Returns & log returns
* Moving averages (10, 50)
* Volatility
* Momentum
* Relative Strength Index (RSI)
* Z-score
* Rolling Sharpe ratio

### 3. Model

A Random Forest classifier is trained to predict the direction of next-day returns.

### 4. Trading Strategy

* Model predictions are converted into trading signals
* Long positions are taken when the model predicts positive returns
* Transaction costs are included to simulate realistic trading

### 5. Backtesting

Strategy performance is evaluated using:

* Accuracy, precision, recall
* Sharpe ratio
* Cumulative returns vs. market benchmark

---

## Results

The model demonstrates the ability to capture short-term market patterns, though performance varies across assets.

Key observations:

* Strategy performance differs significantly between equities
* Transaction costs reduce profitability
* The strategy does not consistently outperform the market

---

## Limitations

* Relies only on technical indicators (no fundamental data)
* Simple train-test split instead of walk-forward validation
* Does not account for liquidity or market impact
* Potential risk of overfitting

---

## Future Improvements

* Hyperparameter tuning
* Feature selection and dimensionality reduction
* More advanced models (e.g., gradient boosting, neural networks)
* Walk-forward validation for robust backtesting
* Incorporation of alternative data sources

---

## Conclusion

This project demonstrates how machine learning can be applied to financial time series to build systematic trading strategies. While results show potential, further improvements are required for real-world deployment.

---

## How to Run

1. Install dependencies:

   ```bash
   pip install yfinance scikit-learn matplotlib
   ```

2. Open the notebook:

   ```
   Machine Learning-Based Multi-Asset Trading Strategy Using Technical Indicators.ipynb
   ```

3. Run all cells to reproduce results.

---

## Author

Riley Thompson
