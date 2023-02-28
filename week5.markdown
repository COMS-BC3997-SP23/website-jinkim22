---
layout: page
title: Week 5
permalink: /week-5/
---
## Week 5

From experimenting with various short-term (intraday) price prediction models, we were unable to create a model that produced reliable hourly predictions that were in any way usable.

However, from experimentation and reading various research papers, we determined that it is possible to create relatively accurate predicitions for day-to-day prices for the near future. 

Explored use of apache airflow to orchestrate the data processing pipeline.


--------------

Notes from runing LSTM:

Used the hourly dataset, but when creating lagged data to feed into LSTM, made it skip 24 index at a time such that the lagged dataset is lagged in
day periods. 
* Note: Could experiment with using 4, 8, 16 hour periods. I think the point of this would be to choose a time period that is long enough such
that the predictions we make don't have to consider randomness as much.

At first, I was getting predictions that were just flat lines, this was caused by keeping both the non normalized features and normalized features. After cutting those down, I ahd 11 features that were all normalized. After running LSTM on that for 15-30 epochs, I had graphs that were consistently
x amount below what the actual price is supposed to be. quite odd. Optimizer was adam at 0.001 learning rate, with mse for loss and MSE for metric. 
MSE was around e^-7, loss was around e^-8. keep in mind though that these aren't very good values because most of the prices that we want to estimate
are in the range of e^-2 to 0 range. 

Did LSTM, Bidirectional LSTM with 64, 128, 256 units, gave it two dense layers of 128 with relu for activation. I tried L2 Regularization, pretty sure
I did it wrong but that didn't help, but using dropout at 0.2 was helpful in making it more generalizable.

Again, the graphs of prediction vs. actual show simliar trends / shape, but for some reason, the predicted are all off by a constant amount. to try and
fix this issue, I tried doing huber los instead of MSE for loss, but no changeoccurred.

LSTM example shown on https://alpaca.markets/learn/trade-crypto-using-ml/ has a 48% accuracy for guessing what the price movement will be in the next 
hour. Tried it myself on https://colab.research.google.com/drive/1CtdDtRKX6bJtP_t70NkWxd1WW-hwsBZg?usp=sharing. Worse than random guess.



