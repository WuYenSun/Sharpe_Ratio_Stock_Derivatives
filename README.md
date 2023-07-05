# Sharpe_Ratio_Stock_Derivatives

How do we define the return on derivatives, or more generally, how can we effectively measure the performance of a trading strategy? 
The challenge lies in the difficulty of determining the appropriate amount of resources to allocate to a trading strategy at its inception. 
Even if the amount is known, the timing of capital utilization introduces an additional dimension of randomness.

To tackle these challenges, we propose the use of a simulation-based dollarized Sharpe ratio in this project. 
This methodology allows us to assess the performance of both portfolios (static sense) and trading strategies (dynamic sense). The key idea behind this approach lies in simulating both the asset and liability sides, thereby accounting for path-dependent outcomes. This method represents an extension of the traditional Sharpe ratio, which focuses solely on the asset side and assumes a constant financing cost. However, it should be noted that this method is not suitable for evaluating trading strategies involving free-boundary problems, such as American call option contracts.

We illustrate this idea within the context of stocks, a portfolio of stocks, forward contracts, futures contracts, and European call option contracts. 
In the stock section, we provide an overview of the basic concept of the dollarized Sharpe ratio using Monte Carlo simulation.
Our sensitivity analysis demonstrates that the Sharpe ratio increases as the drift of the stock price or time horizons increase, while it decreases when interest rates or volatility of the stock price increase. Moreover, including stocks with imperfect correlation in a portfolio can improve its Sharpe ratio.

Moving on to the forward contract section, our findings reveal that the Sharpe ratio of a long forward contract equals that of the underlying stock when the forward price satisfies the no-arbitrage condition, and the margin interest is paid at the borrowing cost. This is due to the fact that the Sharpe ratio is unaffected by leverage, and a forward contract, which does not have maintenance margin requirements, essentially represents a leveraged version of owning the underlying stock.

In the futures contract section, we observe that the Sharpe ratio is slightly higher than that of the underlying stock and forward contract. Engaging in daily borrowing (or lending) against the underlying stock is essentially equivalent to being long a futures contract. However, we must define the feasible trading strategy space before determining whether an asset price can be derived from others under the no-arbitrage condition. In our work, the underlying stock cannot replicate a futures contract since the feasible trading strategy space is limited to only static strategies. Consequently, including futures contracts expands the return space and yields a different Sharpe ratio. European call option contracts, once again, cannot be replicated by primitive assets, resulting in a different Sharpe ratio. 

In conclusion, the measurement of return on derivatives and the evaluation of trading strategy performance present significant challenges due to uncertainties surrounding initial resource allocation and the timing of capital utilization. Nonetheless, by employing a simulation-based dollarized Sharpe ratio, we can address these issues and provide a comprehensive assessment of performance. This methodology, which considers both the asset and liability sides, offers a generalization of the traditional Sharpe ratio, accommodating varying portfolios and trading strategies.
