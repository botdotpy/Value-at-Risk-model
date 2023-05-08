# Value-at-Risk-model
Value-at-Risk estimates the risk associated with investments for a given confidence level, from a range of possible future scenarios using Monte Carlo simulation.

This project assesses the maximum risk of holding 1000 units of MSFT (Microsoft Inc) shares for a month.

It requires downloading the stock's live price with the yfinance python module and calling the history method and iloc[0] on the close price column, to extract the last close price for the stock. 

After setting a risk free rate and determining volalility for the time period, the investment value of the stock is calculated by multiplying the stock price by the number of share units.

Values therefrom are passed as arguments in the VaR function; which deducts the present value of the stock from the end value to derive returns but also requires random standard normal generated values for the number of simulations.

These returns are then plotted on a histogram with the values at certain confidence levels highlighted with dashed axvlines.

Each confidence level informs an investor that, for example, although there is a 5% chance of losing $4,500 from holding MSFT shares for a month, there is a 95% chance of not losing more than $4,500 on the said investment.

