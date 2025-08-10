

# 📊 Trader Behavior vs Market Sentiment Analysis

## 📌 Project Overview
This project analyzes the relationship between **trader performance** and **Bitcoin market sentiment** (Fear vs Greed) using:
1. **Historical Trader Data** from Hyperliquid
2. **Bitcoin Market Sentiment Data** (Fear & Greed Index)

The goal is to uncover **patterns in profitability, trade size, and asset preference** during different sentiment conditions.  
Insights from this project can help build **smarter trading strategies**.

---

## 📂 Dataset Details

### 1. **Trader Data** (`historical_data.csv`)
- **Columns**:  
  `account`, `coin`, `execution_price`, `size_tokens`, `size_usd`, `side`,  
  `timestamp_ist`, `start_position`, `direction`, `closed_pnl`,  
  `transaction_hash`, `order_id`, `crossed`, `fee`, `trade_id`, `timestamp`

- **Key Info**: Contains trade execution details, profit/loss values, and position sizes.

### 2. **Market Sentiment Data** (`fear_greed_index.csv`)
- **Columns**:  
  `timestamp`, `value`, `classification`, `date`

- **Key Info**: Daily Bitcoin sentiment classified as **Fear** or **Greed**.

---

## 🛠️ Steps Performed

### 1️⃣ Data Cleaning
- Standardized column names for easier processing.
- Converted timestamps to proper **datetime** format.
- Created `trade_date` column to match trades with daily sentiment.
- Simplified sentiment classification to **Fear** and **Greed** (merged "Extreme" versions).
- Merged trader data with sentiment data on matching dates.

### 2️⃣ Analysis Performed
#### **Profitability**
- **Total PnL**: Higher on **Greed** days (~$4.86M) than Fear days (~$4.09M)
- **Win Rate**: Slightly higher in Greed (42%) vs Fear (40.8%)
- **Distribution**: Most trades close near break-even in both sentiments.

#### **Trade Size & Risk**
- **Average Trade Size**: Larger in Fear (~$7,182) than Greed (~$4,574)
- **Max Trade Size**: Fear days see significantly larger single trades (~$3.92M vs $2.22M)
- **Total Volume**: Higher in Fear (~$597.8M) than Greed (~$413.0M)

#### **Coin-Specific Insights**
- **BTC** dominates trading volume in both sentiments.
- **Altcoins** like HYPE, SOL, ETH see **more activity in Fear days**.
- Some niche coins (TRUMP, MELANIA, FARTCOIN) show sentiment-driven spikes.

---

## 📊 Visualizations
- **PnL Distribution by Sentiment** → `pnl_distribution.png`
- **Average Trade Size by Sentiment** → `avg_trade_size_by_sentiment.png`
- **Top 10 Coins by Volume in Fear vs Greed** → `top10_coins_by_sentiment.png`

---

## 📁 Project Structure
```

DS\_SSG/
├── main.ipynb                           # Main analysis notebook
├── csv\_files/
│   ├── historical\_data.csv              # Trader dataset
│   └── fear\_greed\_index.csv             # Sentiment dataset
├── outputs/
│   ├── avg\_trade\_size\_by\_sentiment.png  # Chart: Avg trade size vs sentiment
│   ├── pnl\_distribution.png             # Chart: PnL distribution by sentiment
│   └── top10\_coins\_by\_sentiment.png     # Chart: Top coins by volume in each sentiment
├── ds\_report.pdf                        # Final analysis report
└── README.md                            # Project documentation

````

---

## 🚀 How to Run
1. **Clone the Repository**:
   ```bash
   git clone https://github.com/SandipGiri-Developer/crypto-sentiment-analysis.git


2. **Open in Google Colab**:

   * Upload the repository folder to Google Drive.
   * Open `main.ipynb` in **Google Colab**.
3. **Run All Cells** to:

   * Clean and merge data
   * Generate visualizations
   * Produce final insights
4. **Check Generated Charts** in the `outputs/` folder.

---

## 📌 Key Takeaways

* **Greed days** → Slightly better win rate & total PnL.
* **Fear days** → Larger trades, higher total volume, better altcoin opportunities.
* **BTC** remains dominant but sentiment affects focus on altcoins.

---

## 📨 Submission Info

* **Report PDF**: `ds_report.pdf`

---

## 👤 Author

**Name**: Sandip Giri
**Email**: [girisandip602@gmail.com](mailto:girisandip602@gmail.com)

```

````
