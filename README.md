# Trader Performance vs Market Sentiment (Fear / Greed)

## Data Science Intern – Round-0 Assignment  
**Candidate:** Shafiq Ahmed Khan  

---

## Overview
This project analyzes the relationship between **market sentiment (Fear / Greed)** and **trader behavior and performance** on the Hyperliquid platform.  
The objective is to uncover behavioral patterns and derive **actionable strategy insights** that could inform smarter trading decisions.

The analysis focuses on:
- Trader performance (PnL, win rate)
- Behavioral changes under different sentiment regimes
- Segmentation of traders based on leverage usage

---

## Datasets
Two datasets were provided as part of the assignment:

1. **Bitcoin Market Sentiment (Fear / Greed Index)**  
   - Fields: `Date`, `Classification` (Fear / Greed)
   - Granularity: Daily

2. **Historical Trader Data (Hyperliquid)**  
   - Trade-level data including:
     - `account`, `time`, `side`, `size`, `leverage`, `closedPnL`, etc.
   - Granularity: Individual trades

---

## Methodology

### 1. Data Preparation
- Loaded both datasets into a Google Colab environment.
- Performed basic sanity checks:
  - Shape, data types, missing values, and duplicates.
- Converted timestamps to datetime format.
- Aggregated trader data to **daily per-account level** to align with sentiment data.

### 2. Feature Engineering
Key daily metrics were created for each trader:
- Total daily PnL
- Number of trades
- Win rate
- Average leverage
- Average trade size
- Long/short ratio

### 3. Data Alignment
- Trader-level daily data was merged with the sentiment dataset on date.
- Final analysis dataset represents **trader behavior and performance conditioned on market sentiment**.

### 4. Analysis
- Compared performance metrics (PnL, win rate) between Fear and Greed days.
- Analyzed behavioral differences:
  - Trade frequency
  - Leverage usage
  - Long vs short bias
- Segmented traders into:
  - High-leverage vs low-leverage groups

### 5. Insights & Strategies
Findings were summarized into clear insights and translated into **actionable strategy recommendations**.

---

## Key Insights
- Trader PnL shows higher volatility during Fear periods, indicating elevated risk.
- Average leverage tends to be higher during Greed days, reflecting more aggressive positioning.
- High-leverage traders underperform during Fear regimes compared to low-leverage traders.

---

## Strategy Recommendations
1. During Fear periods, cap leverage for high-leverage traders to reduce downside risk and drawdowns.
2. Encourage higher trade activity primarily during Greed periods for traders with historically higher win rates.

---

## Repository Structure


├── Trader_Performance_vs_Market_Sentiment.ipynb
├── README.md
└── outputs/
└── charts and tables 


---

## How to Run
1. Open the notebook in Google Colab or Jupyter.
2. Upload the provided datasets:
   - `fear_greed_index.csv`
   - `historical_data.csv`
3. Run all cells from top to bottom.

The notebook is fully reproducible and does not require additional configuration.

---

## Notes
- The analysis was intentionally kept simple and interpretable.
- The focus is on reasoning, clarity, and actionable insights rather than complex modeling.
- All results are based solely on the provided datasets.

---

## Contact
For any questions regarding this submission, please feel free to reach out via email.
