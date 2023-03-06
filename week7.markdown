---
layout: page
title: Week 7
permalink: /week-7/
---
## Week 7

Did lot of backtesting and algorithm research on QuantConnect. Along with
mean reversion, we tested the performances of simple moving average, and
momentum trading strategies. We hypothesized that to get the most optimal
performance feedback for an "average" span of crypto price movement, it
should be a period where there has been high volatility, both up and down, but also times of steady volatitliy too. For the start price to end price, 
to avoid being overly optimistic, we wanted to have a period where there's only a 10% increase across 2 years. The time period chosen with all these
factors considered were 1/1/2021 - 2/28/2023.

The parameters to optimize for the strategies:

Mean Reversion
- lookback period
- threshold

Simple Moving Average
- Long moving average
- Short moving average

Momentum
- Lookback period

For these parameters, the only parameter we optimized was Mean Reversion. 
After performing backtesting, it was clear that performance was much better 
whenever the number of days was pretty large, a good baseline we found was 
100 days for the lookback period. For the threshold, we chose a default 
value of 1.5. Though performance was theoretically best when we chose 4.0, 
that was only because the bot had executed one trade. Basically, if 
threshold is super high, it only executes traades if it's SUPER certain 
that we should trade. if it's low, small indications can trigger a trade.
1.5 ended up being a good threshold in performance with fair number of 
trades.

For the simple moving average, people on average use 50 days for short SMA,
and 200 for Long SMA, so I just went with that. It is definitely worth doing an optimization for this, especially because the ensemble model I created only weighs sma indicator as 0.1, while other two strategies are weighted 0.5 and 0.9.

For the momentum period, I used a standard 10 day moving momentum. should
look at optimizing this parameter too.

Then for the ensemble model of these three strategies, we must optimize the parameters for their weights.

- Simple moving average weight
- Momentum weight
- Mean Reversion weight

Initially, we skipped a few steps and went directly to creating the ensemble
model, and finding appropriate weights for them. SMA was weighed 0.1, 
momentum was weighed 0.5, and mean reversion was weighed 0.9.

I got 75% in profits over the course of two yeras, despite the turmoil in
sudden increase and decrease of prices in the time period tested, 1/1/2021
to 2/28/2023.