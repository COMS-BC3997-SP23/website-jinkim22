---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
---
## Home
### Automated Cryptocurrency Trader using ML

Stock exchanges are the economic engines of the world, organizing the sales of shares in companies; investors seek to buy and sell stocks via these stock exchanges in order to turn a profit. Their decisions may be made based on fundamentals of the company such as their earning reports, analysis of the current trend of the stock, or broader macroeconomic factors. As such, day-traders of stocks may spend hours a day reviewing the latest news or examining the trends of stocks, and buying or selling based on their analysis.
The goal of our project is to develop a high-performance system to buy and sell securities for profit, specifically cryptocurrencies, with the decisions being made by a deep learning model. This way, the analysis and trading is automated, similar to what is done at today’s hedge funds. The trading of cryptocurrency was chosen over stocks due to trading being consistent around the clock, rather than fixed trading hours. 
The infrastructure should allow for the execution of trades on a mock exchange API that trades cryptocurrencies in a “paper-trading” account. The trading decisions must be made using a constant data stream of cryptocurrency prices (from Alpaca). This data stream is processed to result in a series of signals, which traditionally offer insight to traders. A deep learning algorithm, trained on historical data, predicts if the cryptocurrency will increase or decrease based on these signals. The success of the algorithmic trading system can be measured by the return of the system historically, and in a specific time-frame. 
There are various components to the project that will be built using Python. Firstly, there must be a data pipeline that fetches and processes historical cryptocurrency price data from Alpaca’s API. The stock signals are derived from this data. The data is then input into the machine learning algorithm, which, once trained, can predict if the price of the asset will rise or fall. The output of the algorithm is then fed into the trading engine, which actually executes trades based on insight from the algorithm; this is done by communicating with the mock exchange API. The actions should be logged via a logger. Stretch goals for the project are a simple UI dashboard showing the trades that have been made as well as offering insights into portfolio performance, as well as the implementation of risk management. An estimated timeline for the project is displayed below.

| Timeline   | Goals                              |
|------------|------------------------------------|
| Week 1-2   |  Write and refine project proposal |
| Week 3     |    Design and build architecture   |
| Week 4     | Build basic trading infrastructure |
| Week 5-6   |   Explore and refine ML algorithm  |
| Week 7-8   | Putting it all together            |
| Week 9-19  |            Stretch goals           |
| Week 11-12 |    Final report and presentation   |

Since the project will be based on a mock cryptocurrency trading API, and no actual cryptocurrencies will be bought or sold, no budget is required. The trading algorithm will be based on the research at the following research paper. Advice will be taken from many individuals, including an incoming quantitative researcher at a large hedge fund. Our team has experience in building and working with large-scale infrastructure, including on large distributed systems at Google and Facebook.
