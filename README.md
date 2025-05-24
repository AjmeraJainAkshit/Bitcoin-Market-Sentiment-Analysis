# Bitcoin-Market-Sentiment-Analysis
📊 Bitcoin Trading Sentiment Analysis – Project Documentation
1. 📌 Project Overview
This project investigates the relationship between market sentiment (Fear & Greed Index) and trader performance on the Hyperliquid platform. By combining sentiment classification with historical trade data, we aim to uncover actionable insights that inform better trading strategies.
________________________________________
2. 📁 Datasets Used
- Bitcoin Market Sentiment Dataset
-  Hyperliquid Trader Data
________________________________________
3. ⚙️ Data Processing
- 	Parsed dates and synchronized time format.
- 	Merged sentiment and trader datasets on the date field.
- 	Filtered outliers and invalid trades.
- 	Derived new fields:
o	Leverage (est.) = (Start Position + Trade Size) / Trade Size
o	is_win = True if Closed PnL > 0, else False
________________________________________
4. 📈 Analysis Performed (7 Key Visuals)
- 1. Correlation between Sentiment Index & Closed PnL
  - 	Used scatter + regression plot.
  - 	Weak positive correlation observed.
- 2. Average Closed PnL by Sentiment
  - 	Traders performed slightly better in Greed markets.
- 3. Daily PnL Trends by Sentiment
  - 	Line chart showed strong volatility in Fear periods.
- 4. Leverage vs PnL by Sentiment
  - 	High leverage trades had extreme outcomes (both profit and loss).
  - 	Used estimated leverage formula.
- 5. Trade Size vs PnL by Sentiment
  - 	Regression showed larger trades more volatile in Fear periods.
- 6. Win Rate by Sentiment
  - 	Greed periods had higher win rates (~60%+).
  - 	Calculated as % of trades with Closed PnL > 0.
- 7. PnL Volatility by Sentiment (Box Plot)
  - 	Fear periods had wider spread in PnL outcomes.
  - 	Volatility = daily PnL standard deviation.
________________________________________
5. 📌 Key Insights
- 	Greed markets show higher win rates and better average PnL.
- 	Fear markets are more volatile, with wider distribution of outcomes.
- 	Estimated leverage increases both risk and reward, especially in volatile conditions.
- 	Trade size is a double-edged sword — larger trades can amplify losses or gains.
________________________________________
7. 🧠 Recommendations
- 	Reduce leverage during Fear periods to manage volatility.
- 	Cap trade size in uncertain sentiment conditions.
- 	Build sentiment-aware trading bots that adjust risk levels dynamically.
- 	Continue tracking real-time sentiment as part of pre-trade analysis.

