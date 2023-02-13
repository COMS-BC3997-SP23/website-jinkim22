---
layout: page
title: Week 1
permalink: /week-1/
---
This is what we did

---
layout: page
title: Week 2
permalink: /week-2/
---
Created a script for generating a spreadsheet with 20 stock price movement indicators, and feature expansions on selected features.
Started building framework for feeding data into LSTM, random forest classifications, and regressions to try and predict binary movement of price, and price forecasts.
All parameters for indicators were given straight from a research paper. lstm_stock_pred_research_paper.pdf in my repo.


---
layout: page
title: Week 3
permalink: /week-3/
---
Read research paper and tried implementing LSTM model to do binary prediction on price movement with hourly data of BTC. Goal was to give binary classification on whether
price goes up or down at the next hour. Result was unsuccessful, accuracy was 48~52%, which means that it was just as good as a random guess. All prices were normalized
using min max. Lookback times 30, 100 hours were used, bigger parameters made the RAM crash, which means that we probably need to build out batch training structure to do
this. Random forest was not successful either.

Interesting finding: doing regression and trying to forecast prices, then using that to see if were able to predict increase / decrease from previous price was much more
accurate, 92%. it may have been overfit, however, and it does not make sense how this could have been the case when the previous models failed to learn completely when it
was trained to do binary classification.
