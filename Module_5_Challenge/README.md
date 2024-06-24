# Module_5_Challenge
In this challenge we are evaluating the portfolio of a credit union customer, and will ultimately determine whether their current total portfolio value is adequate to create an emergency fund, and will then run Monte Carlo simulations with different portfolio weights to determine whether a ten year retirement goal is advisable.

By using the client's monthly income, and current stakes in both cryptocurrencies and a bond/stock portfolio, we are able to determine the current total portfolio value. By using API calls, we can be sure that the data collected is up to date, and reflects the current value of the portfolio. After calculating the totals for each asset and the total portfolio, we can evaluate whether this amount is adequate to support the creating of an emergency fund. 

To evaluate the possibility of retirement, we return to our stock/bond portfolio and using the alpaca API collect ten years worth of financial data from the current date. It should be noted that due to current limitations of the free alpaca software, a limited amount of data can be collected. The code, however, is set for ten years of financial data. We then run a Monte Carlo simulation of 500 samples, 30 years, for a 60% bond, 40% stock weighted portfolio. After collecting the summary statistics we are able to show the range of possible outcomes using an upper and lower 95% confidence interval. We then repeated the process but ran a Monte Carlo simulation of 500 samples, 10 years, for a 20% bond, 80% stock weighted portfolio. After collecting the summary statistics we again show the range of possible outcomes using an upper and lower 95% confidence interval. 

While it was clear, based on the simulations, that a portfolio that is held longer produces signficantly advantageous results as to return, it was not immediately clear how the weights in the portfolio impacted these results. To determine this, we ran the the ten year simulation once more, but with the portfolio weights now 80% in bonds, and 20% in stocks. This revealed that a portfolio more heavily weighted towards stocks produced a notably better outcome as to return. Therefore, we can suggest that a client hold their portfolio as long as possible, and weigh their portfolio more heavily towards stocks in order to achieve the greatest results in a retirement portfolio.