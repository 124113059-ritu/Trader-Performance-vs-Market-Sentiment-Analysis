# 📊 Trader Performance vs Market Sentiment Analysis

## 🔍 Objective

This project analyzes how market sentiment (Fear vs Greed) impacts trader behavior and performance using Hyperliquid trading data.

The goal is to identify patterns in profitability, risk-taking, and trading activity, and derive actionable insights to improve trading strategies.

---

## 📁 Datasets Used

### 1. Market Sentiment Data

* Columns: date, classification (Fear, Greed, etc.)
* Represents daily Bitcoin market sentiment

### 2. Historical Trader Data

* Includes: account, trade size, direction, PnL, fees, timestamp, etc.
* Contains detailed trading activity of users

---

## 🧹 Data Preparation

* Standardized column names for consistency
* Converted timestamps (`timestamp_ist`) to datetime format
* Extracted date for daily-level alignment
* Merged datasets on date
* Removed 6 rows with missing sentiment (negligible impact)

---

## ⚙️ Feature Engineering

Created key features for analysis:

* **is_profit** → Indicates profitable trades
* **net_pnl** → PnL after deducting fees
* **daily_pnl** → Aggregated profit per trader per day
* **win_rate** → Ratio of profitable trades
* **trade frequency** → Number of trades per day

---

## 📊 Analysis & Findings

### 🔹 1. Performance vs Sentiment

* PnL distribution shows **high variability** across all sentiment phases
* Both Fear and Greed exhibit **extreme profits and losses**
* Greed phases show **larger negative outliers**, indicating risky behavior

---

### 🔹 2. Behavior Changes with Sentiment

* Traders take **larger positions during Greed**, showing increased risk appetite
* Fear periods show **high volatility and unpredictable outcomes**
* Trading activity varies slightly but risk intensity changes significantly

---

### 🔹 3. Direction Bias (Long/Short)

* Traders tend to take more **short positions during Fear**
* Traders show a **long bias during Greed phases**

---

### 🔹 4. Trader Segmentation

* **Frequent vs Infrequent Traders**
  → Frequent traders show more consistent performance

* **Winners vs Losers**
  → A small group of traders contributes to most profits

---

## 💡 Key Insights

1. Market sentiment strongly influences **risk-taking behavior**, not just profitability
2. **Greed phases lead to overconfidence**, resulting in extreme losses
3. **Fear phases are highly volatile**, with both large gains and losses
4. Most trades yield **small returns**, but a few extreme trades dominate outcomes

---

## 🎯 Strategy Recommendations

1. **Reduce leverage during Fear periods**
   → High volatility increases risk exposure

2. **Avoid overtrading during Greed phases**
   → Overconfidence leads to large losses

3. **Focus on risk management over trade frequency**
   → Few extreme trades dominate overall performance

---

## 🛠 Tools & Technologies

* Python
* Pandas
* NumPy
* Matplotlib / Seaborn
* Jupyter Notebook

---

## 📌 Conclusion

Market sentiment plays a crucial role in shaping trader behavior and risk exposure. While it does not directly determine profitability, understanding sentiment-driven patterns can significantly improve trading strategies and decision-making.

---

## ▶️ How to Run

1. Open the Jupyter Notebook
2. Install required libraries:

   ```bash
   pip install pandas numpy matplotlib seaborn
   ```
3. Run all cells step-by-step

---

## 📎 Submission

This project was completed as part of the Data Science Intern assignment for Primetrade.ai.

