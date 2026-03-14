# Trader Behavior Analysis Using Market Sentiment

## Overview

This project analyzes trader behavior using historical trading data from the Hyperliquid platform and the Bitcoin Fear & Greed Index.
The goal is to explore how market sentiment influences trader performance and identify patterns that can help improve trading strategies.

The analysis combines two datasets:

1. **Hyperliquid Historical Trader Data**
2. **Bitcoin Fear & Greed Index (Market Sentiment Dataset)**

By merging these datasets based on date, we can evaluate how trader performance changes under different market sentiment conditions.

---

## Objectives

* Analyze trader performance across different market sentiment regimes.
* Identify patterns in profitability, trade size, and trading activity.
* Discover behavioral trends that can inform smarter trading strategies.

---

## Datasets

### 1. Hyperliquid Historical Trader Data

Contains detailed trading activity including:

* Account
* Coin
* Execution Price
* Trade Size (Tokens & USD)
* Trade Direction (Buy/Sell)
* Timestamp
* Closed Profit & Loss (PnL)
* Trading Fees

### 2. Bitcoin Fear & Greed Index

Market sentiment dataset including:

* Date
* Sentiment Classification

  * Extreme Fear
  * Fear
  * Neutral
  * Greed
  * Extreme Greed

---

## Methodology

### 1. Data Collection

Datasets were downloaded from Google Drive and loaded into Python using Pandas.

### 2. Data Cleaning

* Converted timestamps to datetime format
* Extracted trading date and time
* Handled missing sentiment values
* Standardized column formats

### 3. Feature Engineering

Additional features were created:

* **profit** → whether a trade resulted in profit
* **trade_value** → trade size in USD
* **hour** → hour of trade execution

### 4. Dataset Merge

The trader dataset and sentiment dataset were merged using the **date column** to analyze trader behavior relative to market sentiment.

---

## Exploratory Data Analysis (EDA)

The following analyses were conducted:

* Average Profit by Market Sentiment
* Trader Win Rate by Sentiment
* Trade Size vs Market Sentiment
* Buy vs Sell Profitability
* Trading Activity by Hour

---

## Visualizations

Several charts were created to understand trader behavior patterns:

* Profit Distribution by Market Sentiment
* Trade Size Distribution by Sentiment
* Trading Activity by Hour
* Correlation Heatmap of Trading Metrics

These visualizations help highlight how trader behavior shifts under different sentiment conditions.

---

## Key Insights

**1. Highest Win Rate in Extreme Greed**
Traders achieve the highest win rate during **Extreme Greed** sentiment, suggesting strong bullish momentum improves trading outcomes.

**2. Lower Profitability During Extreme Fear**
Extreme Fear markets tend to produce lower profitability due to panic-driven trading behavior.

**3. Larger Trade Sizes During Greed**
Trade sizes increase during **Greed and Extreme Greed** markets, indicating higher trader confidence and risk appetite.

**4. Concentrated Trading Activity**
Trading activity peaks during certain hours, likely corresponding to periods of higher liquidity and market volatility.

---

## Technologies Used

* Python
* Pandas
* NumPy
* Seaborn
* Matplotlib
* Google Colab

---

## Project Structure

```
trader-behavior-analysis-market-sentiment
│
├── Trader_Behavior_Analysis.ipynb
├── dataset/
└── README.md
```

---

## Conclusion

This analysis demonstrates that market sentiment plays a significant role in trader behavior and performance.
Understanding these behavioral patterns can help traders and analysts design more informed trading strategies.

---

## Author

**Vivekanand Kumar**
B.Tech CSE | Data Science & Machine Learning Enthusiast
