# Trend-based-Trading-Strategies

## Project Description:
Study of strategy results and evaluation of trend-based trading strategies under different technical indicators, strategy rules, etc.

## Background
Technical analysis focuses on the historical price and trading volume of securities to find price trends and thus predict future prices.

## Strategies Implemented
1) Double SMA trading strategy based on 5-day and 20-day simple averages
     - Technical Indicator: Simple Averages
     - Test data: GME 2022-01 to 2023-8 closing prices
     - Strategy Idea
         ~ The use of golden cross and death cross as a signal to open buy and close sell positions
     - Specific conditions for opening and closing positions
         ~ Positions are opened on signals, closed and reversed on reverse signals.
             -> 5-day simple average breaks above the 20-day simple average as a buy signal.
             -> A downward break of the 5-day simple average above the 20-day simple average is a sell signal.
         ~ Close a position immediately when a loss occurs on opening the position

2) Trading Strategies Based on Exponentially Moving Average Convergence Divergence (MACD)
     - Technical Indicator: Moving Average Convergence Divergence (MACD)
     - Test data: GME 2022-01 to 2023-8 closing prices
     - Strategy Idea
         ~ Utilize the divergence (trend strengthening) and convergence (trend slowing) of the long and short-term moving averages reflected by this technical indicator to formulate trading strategies.
     - Specific conditions for opening and closing positions
         ~ Signal for Opening a Position: When DIF and DEA are both positive, it's a bullish market. A DIF crossover above DEA (MACD turning positive) is a buy signal. A DIF crossover below DEA (MACD turning negative) is a sell signal.
         ~ Signal for Closing a Position and Reversing: When DIF and DEA are both positive and negative, it's a bearish market. A DIF crossover below DEA (MACD turning negative) is a sell signal. A DIF crossover above DEA (MACD turning positive) is a buy signal.
         ~ Additional Signals: When DIF falls below the zero axis (death cross), it's a sell signal. When DIF crosses above the zero axis (golden cross), it's a buy signal.
         ~ Close a position immediately when a loss occurs on opening the position
