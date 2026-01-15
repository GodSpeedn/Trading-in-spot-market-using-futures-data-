
Trading in Spot Markets using Futures Open Interest
This repository contains my first mini-project completed as part of the Executive Programme in Algorithmic Trading (EPAT). As I am just starting my journey in quantitative trading, this project focuses on building a foundational strategy that combines price trends with Open Interest (OI) analysis.

 View Notebook Online (Google Colab)
 https://colab.research.google.com/drive/1sz9fTbsma
📌 Project Overview
The goal of this project was to backtest a trading strategy that trades the underlying asset (spot market) based on trends confirmed by the derivatives market (Futures Open Interest).

Key Objectives
Data Handling: Preprocessing spot price data and Futures Open Interest (OI) data.

Signal Generation: Identifying trends using Simple Moving Averages (SMA) and confirming them with OI momentum.

Backtesting: Generating a trade book and analyzing the strategy's performance.

🧠 Strategy Logic
The strategy attempts to capture momentum by looking for alignment between the spot price trend and futures market participation.

Trend Indicator: 5-day Simple Moving Average (SMA) crossover on the spot price.

Momentum Filter: Futures Open Interest (OI) must be greater than its 10-day moving average.

Entry Rules
Long Signal: Spot price crosses above SMA(5) (Bullish) AND Current OI > 10-day Average OI.

Short Signal: Spot price crosses below SMA(5) (Bearish) AND Current OI > 10-day Average OI.

Exit Rules
Target Hit: 5% profit target is reached.

Momentum Loss: Current OI drops below the 10-day Average OI.

Trend Reversal: Spot price crosses back against the trade direction.

Expiry: Position squared off on the contract expiry date.

📊 Results & Analysis
Total Trades: 231

Win Ratio: ~0.35

Conclusion: The backtest revealed that relying solely on a lagging indicator like SMA without a regime filter (trending vs. ranging) led to multiple false signals (whipsaws). It serves as a valuable lesson on the importance of risk management and regime filtering in algorithmic trading.

🛠️ Built With
Python: Core logic.

Pandas: Data manipulation and aggregation.

Matplotlib: Visualization.

This project represents my first step into algorithmic trading. Feedback and suggestions are welcome!
