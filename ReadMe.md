# 📈 Trader Behavior Analysis Using Market Sentiment

## Overview
This project analyzes the relationship between **trader behavior**, **trade performance**, and **Bitcoin market sentiment (Fear vs Greed)** using historical trading data and the Bitcoin Fear & Greed Index.

The objective is to identify how market sentiment influences trader decision-making, trade sizing, and profitability, and to extract actionable insights that can support **sentiment-aware trading and risk management strategies**.

---

## Datasets

### 1. Historical Trader Data
Contains trade-level information including:
- Account
- Symbol
- Side (Buy/Sell)
- Execution details
- Trade size in USD
- Closed PnL
- Event and timing metadata

### 2. Bitcoin Fear & Greed Index
Daily sentiment classification indicating:
- Fear
- Greed

Each trade is mapped to the corresponding sentiment using the trade date.

---

## Data Preparation

- Converted trade timestamps to datetime format
- Extracted trade-level dates for alignment
- Merged trader data with Fear & Greed Index on date
- Cleaned and standardized key columns
- Exported merged dataset for reuse

---

## Feature Engineering

- Created trade-level profitability bins:
  - Profit
  - Loss
  - Zero
- Aggregated trader-level metrics:
  - Total PnL
  - Trade count
  - Average trade size (USD)
- Filtered out low-activity traders (less than 10 trades)

---

## Trader Segmentation

Traders were segmented based on **total PnL distribution**:
- **Profitable**: Top 20% of traders
- **Average**: Middle 60%
- **Losing**: Bottom 20%

Trader type labels were added back to the merged dataset to enable behavioral comparison.

---

## Analysis Performed

- Compared trader behavior across **Fear vs Greed** sentiment regimes
- Evaluated differences in:
  - Average PnL per trade
  - Average trade size
  - Trade frequency
- Analyzed how trader segments behave differently under changing sentiment
- Visualized key trends for interpretability

---

## Key Insights

- Profitable traders maintain more consistent trade sizing across both Fear and Greed periods.
- Losing traders significantly increase trade size during Greed phases, suggesting overconfidence.
- Market sentiment amplifies risk-taking behavior more strongly than trader skill alone.
- Greed periods exhibit higher variability in trading outcomes, increasing downside risk.

---

## Business Implications

- Sentiment-aware position sizing can help reduce excessive risk during Greed phases.
- Trading platforms can implement monitoring systems to detect overtrading behavior during high-optimism markets.
- Trader education and risk controls can be dynamically adjusted based on sentiment signals.

These insights can support better **risk management**, **trader profiling**, and **strategy design**.

---

## Tools & Technologies

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Jupyter Notebook

---

## Limitations & Future Scope

- Uses daily sentiment data and does not capture intraday sentiment changes
- Results depend on historical patterns and may not generalize across all market conditions
- Future extensions could include:
  - Statistical significance testing
  - Real-time sentiment integration
  - Predictive modeling using sentiment features

---

## Repository Contents

- `Data Analysis.ipynb` – Full analysis notebook
- `historical_data.csv` – Raw trader data
- `fear_greed_index.csv` – Market sentiment data
- `merged_data.csv` – Processed merged dataset
- `README.md` – Project documentation

---

## Author
**Akshat Mishra**  
B.Tech Computer Engineering (Data Science)  
Aspiring Data Scientist | Analytics | Trading Intelligence

