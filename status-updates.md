---
layout: page
title: Status Updates
permalink: /status-updates/
---
# Status Updates


## About Us
If you don't know us already, our names are Jin Kim and Sai Chintalapati, both seniors in SEAS studying Computer Science.

## Project Idea
The goal of our project is to develop a high-performance system to buy and sell securities for profit, specifically cryptocurrencies, with the decisions being made by a deep learning model. This way, the analysis and trading is automated, similar to what is done at today’s hedge funds. The trading of cryptocurrency was chosen over stocks due to trading being consistent around the clock, rather than fixed trading hours. The infrastructure should allow for the execution of trades on a mock exchange API that trades cryptocurrencies in a “paper-trading” account. The success of the algorithmic trading system can be measured by the return of the system historically, and in a specific time-frame. 

## Wins
- End-to-end system online running on Google Cloud with monitoring dashboard, including infrastructure for data pipeline, triggering algorithm every 20 minutes, and running trades
- Rapidly brainstormed and iterated through various trading engine algorithm ideas, from simple moving average to mean reversion to momentum trading strategies
- Backtesting: 75% in profits over the course of two yeras, despite the turmoil in sudden increase and decrease of prices in the time period tested, 1/1/2021 to 2/28/2023


## Plans
- We believe a system ingesting stock data in real-time and making real-time decisions is a more exciting thing to work on, so we plan to transition our current system to that method
- Coded portfolio rebalncing with Sharpe Ratio, but yet to use because better option may be available with https://pypi.org/project/pyportfolioopt/

## Issues
There were some issues we faced along the way, primarily regarding the success of the underlying stock prediction algorithms
