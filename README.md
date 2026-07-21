# Bitcoin Price Prediction Using Machine Learning

## Project Motivation and Overview

Bitcoin is one of the world's most volatile financial assets, making accurate price forecasting a challenging machine learning problem.

This project explores whether historical Bitcoin market data can be used to predict future closing prices by comparing traditional machine learning algorithms with a Long Short-Term Memory (LSTM) neural network designed for sequential data.

Rather than focusing solely on prediction accuracy, this project emphasizes the complete data science workflow—from data validation and exploratory analysis to feature engineering, model evaluation, and deployment through an interactive dashboard.

---

## Problem Statement

Develop a machine learning model capable of predicting Bitcoin's next closing price using historical market data.

The project compares multiple regression algorithms to determine which modeling approach performs best for cryptocurrency time-series forecasting.


## Objectives

- Analyze historical Bitcoin market data
- Validate and preprocess the dataset
- Perform exploratory data analysis
- Engineer meaningful time-series features
- Train and evaluate multiple machine learning models
- Compare classical machine learning and deep learning approaches
- Build an interactive dashboard for exploring data and model predictions

---

## Dataset

**Source:** BITCOIN Historical Datasets 2018-2026 Binance API 

Kaggle: https://www.kaggle.com/datasets/novandraanugrah/bitcoin-historical-datasets-2018-2024/data

The dataset contains historical OHLCV (Open, High, Low, Close, Volume) information sampled at regular intervals (15m, 1h, 4h, 1d).


### Features

| Feature | Description |
|----------|-------------|
| Open Time | Start of the trading interval |
| Open | Opening price |
| High | Highest price during the interval |
| Low | Lowest price during the interval |
| Close | Closing price |
| Volume | Bitcoin traded during the interval |
| Close Time | End of the trading interval |
| Quote Asset Volume | Total trading volume in USDT |
| Number of Trades | Number of executed trades |
| Taker Buy Base Asset Volume | Bitcoin purchased by takers |
| Taker Buy Quote Asset Volume | USDT value of taker purchases |

---

## Project Structure

```text
bitcoin-price-prediction/
│
├── data/
│   ├── raw/
│   └── processed/
│
├── notebooks/
│   ├── 01_data_validation.ipynb
│   ├── 02_exploratory_analysis.ipynb
│   ├── 03_feature_engineering.ipynb
│   ├── 04_classical_models.ipynb
│   ├── 05_lstm.ipynb
│   └── 06_model_comparison.ipynb
│
├── src/
│   ├── preprocessing.py
│   ├── features.py
│   ├── models.py
│   ├── lstm.py
│   ├── metrics.py
│   └── visualization.py
│
├── dashboard/
│   └── app.py
│
├── requirements.txt
└── README.md
```


## Machine Learning Models

### Classical Machine Learning

- Linear Regression (Baseline)
- Random Forest Regressor
- Support Vector Regressor (SVR)
- XGBoost Regressor

### Deep Learning

- Long Short-Term Memory (LSTM)


## Evaluation Metrics

Each model will be evaluated using:

- Mean Absolute Error (MAE)
- Root Mean Squared Error (RMSE)
- Mean Absolute Percentage Error (MAPE)
- R² Score

Performance will be compared both quantitatively and visually.


## Exploratory Data Analysis

The project investigates questions such as:

- How has Bitcoin's price changed over time?
- How volatile is Bitcoin?
- Does trading volume correlate with price movement?
- What is the distribution of daily returns?
- Are there seasonal or cyclical market patterns?
- Which features appear most predictive?


## Feature Engineering

Additional features will be created from the raw market data, including:

- Daily Returns
- Log Returns
- Price Range
- Rolling Volatility
- Moving Averages (SMA & EMA)
- Relative Strength Index (RSI)
- MACD
- Bollinger Bands
- Lag Features
- Average Trade Size
- Buy/Sell Pressure Ratios


## Dashboard

A Streamlit dashboard will allow users to:

- Explore historical Bitcoin price data
- Visualize market trends
- Display technical indicators
- Compare machine learning models
- View prediction results
- Analyze feature importance


## Technologies

- Python
- Pandas
- NumPy
- Scikit-learn
- TensorFlow / Keras
- XGBoost
- Plotly
- Streamlit
- Matplotlib

---

## Results

> *This section will be updated after model training.*

| Model | MAE | RMSE | MAPE | R² |
|------|----:|-----:|------:|---:|
| Linear Regression | - | - | - | - |
| Random Forest | - | - | - | - |
| XGBoost | - | - | - | - |
| SVR | - | - | - | - |
| LSTM | - | - | - | - |

---

## Future Improvements

Potential future enhancements include:

- Hyperparameter optimization
- Cross-validation for time-series forecasting
- Transformer-based forecasting models
- Multi-step price prediction
- Live Binance API integration
- Docker containerization
- Cloud deployment
- Real-time prediction dashboard

---

## Installation

Clone the repository:

```bash
git clone https://github.com/<your-username>/bitcoin-price-prediction.git
cd bitcoin-price-prediction
```

Install the required packages:

```bash
pip install -r requirements.txt
```

Run the dashboard:

```bash
streamlit run dashboard/app.py
```

---

## Author

**Kenneth C. Prado**
M.S. Data Sience Candidate at Vanderbilt

LinkedIn: https://www.linkedin.com/in/kenneth-c-prado/

---

## License

This project is intended for educational purposes only.

The models developed in this repo should **not** be interpreted as financial advice or relied upon for investment decisions. 