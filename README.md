# NVIDA-STOCK-PREDICTION-RF-MODEL
📈 NVIDIA Stock Gap Prediction Using Random Forest

This project builds a machine learning classification model to predict whether the next trading day’s opening price of NVIDIA Corporation (NVDA) will be higher than the previous day’s closing price.

The task is formulated as a binary classification problem:

​<img width="345" height="112" alt="image" src="https://github.com/user-attachments/assets/4c94946b-1d10-4092-908d-c81f9a2e58e5" />

Project Overview

Financial markets exhibit complex, noisy behavior. This project explores whether historical price-based technical indicators can help predict gap-up vs gap-down movements using:

- yfinance for historical data

- Feature engineering with rolling statistics

- RandomForestClassifier from scikit-learn

- Time-series aware train/test split

Historical stock data is retrieved using:

 - Yahoo Finance API

Python package: yfinance

Ticker used: NVDA

Time period: 2015-01-01 to 2024-12-31

| Feature       | Description                                 |
| ------------- | ------------------------------------------- |
| Return        | Daily percentage return                     |
| MA_5          | 5-day moving average                        |
| MA_10         | 10-day moving average                       |
| Volatility_5  | 5-day rolling standard deviation of returns |
| Momentum_5    | 5-day price momentum                        |
| Volume_Change | Daily percentage change in volume           |

** All features are constructed using past data only to prevent look-ahead bias.

🎯 Binary label: Target = 1 if Next_Open > Close else 0

Algorithm: RandomForestClassifier

Hyperparameters:

- n_estimators = 300

- max_depth = 6

- class_weight = "balanced"

- random_state = 42

The dataset is split chronologically:

- 80% training

- 20% testing

- No shuffling (time-series safe)

📈 Evaluation Metrics

- Accuracy

- Confusion Matrix

- Precision / Recall / F1-score

- Feature Importance

⚠️ Note: In financial prediction, even 52–55% accuracy can be meaningful due to market efficiency constraints.

📌 Disclaimer

This project is for educational and research purposes only.

It does not constitute financial advice or a trading recommendation.

Financial markets are highly unpredictable, and past performance does not guarantee future results.




































	​
