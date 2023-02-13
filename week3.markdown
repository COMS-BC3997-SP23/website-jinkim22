---
layout: page
title: Week 3
permalink: /week-3/
---
## Week 3

Read research paper and tried implementing LSTM model to do binary prediction on price movement with hourly data of BTC. Goal was to give binary classification on whether
price goes up or down at the next hour. Result was unsuccessful, accuracy was 48~52%, which means that it was just as good as a random guess. All prices were normalized
using min max. Lookback times 30, 100 hours were used, bigger parameters made the RAM crash, which means that we probably need to build out batch training structure to do
this. Random forest was not successful either.

Interesting finding: doing regression and trying to forecast prices, then using that to see if were able to predict increase / decrease from previous price was much more
accurate, 92%. it may have been overfit, however, and it does not make sense how this could have been the case when the previous models failed to learn completely when it
was trained to do binary classification.
