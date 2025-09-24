https://colab.research.google.com/drive/1kwS9UbY2aprNFpzsQxh8xYFbaPlJKh5H?usp=sharing
# cryptocurrency-analysis

## Project Overview
This project analyzed historical cryptocurrency trading data alongside the **Fear & Greed Index** to uncover patterns in trader profitability, trading behavior, and account performance.  
The analysis aimed to explore the relationship between market sentiment and trading outcomes, identify account archetypes, and provide actionable insights for trading strategies.

---

## Data Loading & Cleaning
1. Loaded `historical_data.csv` (trade logs) and `fear_greed_index.csv` (market sentiment).  
2. Standardized date/time columns and removed invalid entries.  
3. Merged datasets on trading date to associate each trade with market sentiment.

---

## Data Preprocessing
1. Converted `closedPnL` and `position size` to numeric values.  
2. Filled missing sentiment values with **Neutral**.  
3. Encoded sentiment categories into numeric labels for analysis.

---

## Visualization & Analysis
Generated **10 key visualizations** to explore the relationships between sentiment, PnL, position size, time, symbols, and accounts.  

**Key metrics analyzed:**  
- Profitability  
- Win rate  
- Trade volume  
- Position size distribution  
- Rolling PnL  
- Account clustering  
- Correlations  

---

## Key Insights & Patterns

### 1️⃣ Sentiment vs Profitability
- Trades during **Greed** periods had higher PnL.  
- Trades during **Fear** periods showed smaller or negative profits.  
- Most trades occurred under **Neutral** or **Greed** conditions.

### 2️⃣ Win Rate Analysis
- Win rates were generally higher during **Greed** periods.  
- Neutral sentiment trades had moderate win rates but a larger number of trades.

### 3️⃣ Symbol-Level Performance
- Top traded coins contributed most to profits.  
- Certain coins performed consistently better under specific sentiment conditions.  
- Heatmaps revealed clear differentiation of average PnL by sentiment and symbol.

### 4️⃣ Time-of-Day Patterns
- Mid-day trading hours were more profitable.  
- Early morning or late-night trades were slightly riskier.

### 5️⃣ Position Size vs Performance
- Moderate position sizes yielded better PnL.  
- Very small or very large trades often resulted in inconsistent profits or losses.

### 6️⃣ Position Size Distribution
- Trades were categorized into five bins (Small → Large).  
- Medium to medium-large trades contributed most to consistent profits.

### 7️⃣ Rolling PnL Analysis
- Short-term PnL was highly volatile.  
- Medium and long-term rolling averages revealed stabilized profit trends over time.

### 8️⃣ Account Performance Clustering
- Accounts clustered based on total PnL, average PnL, and position size:  
  1. **High-performing large traders** – high PnL, moderate to large positions.  
  2. **Small but consistent traders** – low PnL but frequent trades.  
  3. **Low-performing traders** – small/medium positions with negative cumulative PnL.

### 9️⃣ Correlation Analysis
- Positive correlations observed between `closedPnL` and `size`, and between `closedPnL` and sentiment.  
- Weak correlation with trading hour; sentiment was a stronger predictor of profitability than time-of-day alone.

### 🔟 Comprehensive Sentiment Analysis
- **Greed sentiment** → highest average PnL and win rate.  
- **Fear sentiment** → lowest profitability and win rate.

---

## Folder Structure
