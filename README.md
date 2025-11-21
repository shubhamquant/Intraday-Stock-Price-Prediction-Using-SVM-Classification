# Intraday-Stock-Price-Prediction-Using-SVM-Classification

Intraday Trading Strategy using SVM
Project Overview
This project implements an intraday trading strategy for ICICI stock using minute-level data and a Support Vector Machine (SVM) classifier. The algorithm generates trading signals (-1, 0, 1) based on technical indicators and price patterns to make buy/sell/hold decisions.

Key Features
Data Preparation
Data Source: ICICI minute-level OHLCV data

Time Period: February 22-23, 2018

Features: 750 data points with 5-minute intervals

Feature Engineering
Technical indicators calculated with 10-minute lookback periods:

RSI (Relative Strength Index): Momentum indicator

SMA (Simple Moving Average): Trend indicator

Correlation: Price-SMA correlation

SAR (Parabolic SAR): Trend reversal indicator

ADX (Average Directional Index): Trend strength

Price-based features: Previous High, Low, Close

Open-based features: Open-Open and Open-Close differences

Return trends: 9-period historical returns

Machine Learning Model
Algorithm: Support Vector Classifier (SVM)

Kernel: RBF (Radial Basis Function)

Hyperparameter Tuning: RandomizedSearchCV with TimeSeriesSplit

Preprocessing: StandardScaler for feature normalization

Signal Generation: Ternary classification (-1, 0, 1) based on return quantiles

Trading Strategy
Execution: Trade at open prices based on predicted signals

Position Management: Intraday only, positions closed at market close (3:29 PM)

Risk Management: No overnight positions

Performance Metrics
Model Accuracy
Training Accuracy: 99%

Testing Accuracy: 42%

Risk-Adjusted Returns
Annualized Sharpe Ratio: 77.74

Maximum Drawdown: -0.14%

Strategy Return: 1.49%
