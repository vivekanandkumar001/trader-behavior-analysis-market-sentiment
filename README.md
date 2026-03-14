# Trader Behavior Analysis Using Market Sentiment (AI & ML)

## Overview

This project analyzes trader behavior using historical trading data from the Hyperliquid platform combined with the Bitcoin Fear & Greed Index.
The goal is to understand how **market sentiment influences trading performance** and to build a **machine learning model that predicts trade profitability**.

The analysis integrates **data science, exploratory data analysis (EDA), and machine learning techniques** to uncover hidden patterns in trading behavior.

---

## Objectives

* Analyze how market sentiment impacts trader performance.
* Identify behavioral patterns in profitable and losing trades.
* Understand how trade size, execution price, and sentiment influence outcomes.
* Build a **machine learning model to predict whether a trade will be profitable**.

---

## Datasets

### 1. Hyperliquid Historical Trader Data

This dataset contains detailed trading activity including:

* Account
* Coin
* Execution Price
* Trade Size (Tokens)
* Trade Size (USD)
* Buy/Sell Side
* Timestamp
* Start Position
* Closed Profit & Loss (PnL)
* Trading Fee

### 2. Bitcoin Fear & Greed Index

This dataset represents market sentiment and contains:

* Date
* Sentiment Value
* Sentiment Classification

  * Extreme Fear
  * Fear
  * Neutral
  * Greed
  * Extreme Greed

---

## Methodology

### 1. Data Collection

Both datasets were downloaded from Google Drive and loaded using **Python and Pandas**.

### 2. Data Cleaning

Data preprocessing steps included:

* Converting timestamps to datetime format
* Extracting date and time features
* Handling missing sentiment values
* Standardizing column formats

### 3. Feature Engineering

Additional features were created to improve analysis and machine learning performance:

* **profit** → Indicates whether a trade resulted in profit
* **trade_value** → Total trade value in USD
* **hour** → Hour of trade execution

These engineered features help capture trading behavior patterns.

---

## Dataset Merge

The trader dataset and sentiment dataset were merged using the **date column** so that each trade is associated with the corresponding market sentiment.

```text
Trader Data + Market Sentiment → Combined Dataset
```

---

## Exploratory Data Analysis (EDA)

Several analyses were conducted to understand trading patterns:

* Average Profit by Market Sentiment
* Trader Win Rate by Sentiment
* Trade Size vs Market Sentiment
* Buy vs Sell Performance
* Trading Activity by Hour

These analyses reveal how trader behavior changes across different market conditions.

---

## Visualizations

The project includes multiple visualizations to interpret trading behavior:

* Profit Distribution by Market Sentiment
* Trade Size Distribution by Sentiment
* Trading Activity by Hour
* Correlation Heatmap of Trading Metrics

These charts help highlight patterns between sentiment and trading performance.

---

## Machine Learning Model

A **Random Forest classifier** was trained to predict whether a trade will be profitable based on trading metrics and sentiment features.

### Features Used

* Execution Price
* Trade Size (USD)
* Trade Value
* Market Sentiment Value
* Hour of Trade

### Target Variable

```
profit (True / False)
```

### Model Workflow

1. Feature selection
2. Train-test split
3. Model training using Random Forest
4. Prediction on test dataset
5. Model evaluation

---

## Model Evaluation

The model was evaluated using:

* Accuracy Score
* Confusion Matrix
* Classification Report
* Feature Importance Analysis

Feature importance helps identify which trading factors most influence profitability.

---

## Key Insights

**Insight 1 — Highest Win Rate During Extreme Greed**

Traders achieve the highest win rate during **Extreme Greed sentiment**, suggesting that strong bullish momentum improves trading outcomes.

---

**Insight 2 — Lower Profitability During Extreme Fear**

Extreme Fear markets show lower profitability due to panic-driven trading behavior and increased volatility.

---

**Insight 3 — Larger Trade Sizes During Greed Markets**

Trade sizes tend to increase during **Greed and Extreme Greed sentiment**, indicating higher trader confidence and risk appetite.

---

**Insight 4 — Concentrated Trading Activity**

Trading activity peaks during specific hours, likely corresponding to periods of higher market liquidity and volatility.

---

**Insight 5 — Market Sentiment Influences Trading Behavior**

Market sentiment has a measurable impact on trading performance, risk-taking behavior, and trade execution patterns.

---

## Technologies Used

* Python
* Pandas
* NumPy
* Seaborn
* Matplotlib
* Scikit-learn
* Google Colab

---

## Project Structure

```
trader-behavior-analysis-market-sentiment
│
├── Trader_Behavior_Analysis_Using_Market_Sentiment.ipynb
├── dataset/
│   ├── Historical_Data.csv
│   └── Fear_Greed_Index.csv
└── README.md
```

---

## Conclusion

This project demonstrates how combining **market sentiment indicators with trading data** can reveal behavioral patterns in trading performance.

By applying **machine learning models**, we can move beyond descriptive analysis and begin predicting trade outcomes, which could potentially support more informed trading strategies.

---

## Author

**Vivekanand Kumar**

B.Tech Computer Science Engineering
Machine Learning & AI Enthusiast

GitHub:
https://github.com/vivekanandkumar001
