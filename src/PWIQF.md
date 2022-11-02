---
---

---
- interest rate: $r$
- Forward price: $\$F$
- Spot Price: $\$S$
- Time (in years): $T$
- some arbitrary time: $t$

Must Know
- Logarithms
- Euler's Number
- Taylor Series
- Expectation

Better if you know
- Differential Equations
	1. Ordinary
	2. Partial
	3. Stochastic

---
# Table of Contents

1. [[#Ch01: Products and Markets|Ch01: Products and Markets]]


# Paul Wilmott Introduces Quantitative Finance

# Ch01: Products and Markets
## 1.2 Equities
- Most basic of financial instruments.
- This is the ownership of a small piece of a company.
- The shareholders who own the company between them have some say in the running of the business.
- Directors of a company are meant to act in the best interest of shareholders of a company.
> As the asset prices of an instrument go larger, so does the changes in its price from one day to the next.
> Hence, it is reasonable to model the asset price changes as proportion to the current level to the asset. i.e. it is important to model the asset returns in its percentage change rather than the absolute value.
> This way price doesn't go negative.

### Dividend
- To the average investor, the value in holding stocks comes from either dividends or any growth in stocks value.
- Dividends are portion of company's earnings paid out to its shareholders every quarter or 6 months.
- They are issued in the form of cash payments or shares of stock etc.
- The amount of dividend varies time to time by profitability of the company.
#### Concept of Cum/Ex Dividend
- When the company announces their yearly/half-yearly/quarterly results, they also announce a series of dates
	- **Cum dividend** (CD)[^1]
		It's the date when the company declares it's planning to pay out dividends in near future. 
		If you own(hold/purchase) the stock between CD date and XD date, you are entitled for dividends.
		When the company declares the dividend, Share Price of the company goes up by the dividend amount that's been declared because during this period anyone buying the stock is automatically entitled for the dividend, hence market accounts for this amount in the share price.
		Price of shares between CD date and XD Date is called CD Price.
	- **Ex dividend** (XD)
		After the CD date has been passed, the stock moves to XD state.
		This is when the company has confirmed the list of shareholders to recieve the dividend and no further changes could be made to the list.
		After the company has declared its XD state, the share prices of company falls.[^2]
		>- After the dividend has been distributed, the cash reserves of the company falls, hence value of company falls. The share prices then reflect the drop in fundamental value of the company. 
		>- Theoretically, the fall in stock price is equal to amount of dividend issued per share.
		>i.e. $(Value\ of\ company)/(Shares\ Issued) - Dividend = (Value\ of\ company - Total\ Earnings)/(Shares\ Issued)$
		>i.e. $Share\ Price(CD\ Period) - Dividends = Share\ Price(XD\ Period)$
		
	- **Pay out**
		When the dividend transfers to bank account of shareholders.

### Stock Split
- Every now and then, a company announces a stock split.
- E.g. If a comapany with stock price $90 announces a three for one stock-split, its one 90 dollor share splits into 3 shares of 30 dollor each.

## 1.3 Commodities
- Commodities are usually raw products such as oil, metals etc.
- Mostly trading of commodities is done in [future] markets.

## 1.4 Currencies
- **Exchange rate** is the rate at which one currency can be exchanged with another.
- Exchanges of such sort are called **Foreign Exchange (FX)**.
- The fluctuaion in interest rate is unpredictable, but there is a link between interest rates(savings returns) and exchange rates in two countries.
	> I.e. currency of country with higher interest rates appreciates against currency of country with low interest rate.
- Central banks can use interest rates as a tool for manipulating exchange rates.

## 1.5 Indices
- Indices measure how stock market/economies are doing as a whole.
- An index is typically made up from a weighted sum of selection of representative stocks.
	- The selection might represent the whole market or a sector of market.

## 1.6 The Time Value of Money
- This is the most fundamental concept in finance.
- $1 today is worth more than $1 in a year's time.
- There are multiple types of interest
	1. **Simple Interest**, is where interest in calculated on the initial sum of money(principle amount).
	2. **Compound Interest**, is where interest is generated on interest
		1. Discretely compounded
			Interest is paid out in discrete time intervals, say, yearly (once a year), biannully (twice a year), quarterly (4x a year), weekly, daily etc. Its formula is given by 
			$$\displaystyle{FV = PV\cdot(1+\frac{r}{t})^{yt}}$$
			- $r$ is rate of interest 
			- $t$ is the no of interest payouts in a year.
			- $y$ is the no of years
		2. Continuously compounded[^3][^4]
			Interest is paid out in continuous time i.e. ${\lim}\limits_{t\to \infty}$.
			Its formula is given by 
			$$\displaystyle{FV = PV\cdot e^{ry}}$$ 
			Similarly, if we know the future value (FV) of an asset, we can calculate the present value (PV) by
			$$\displaystyle{PV = FV\cdot e^{-ry}}$$
## 1.7 Fixed Income Securities
- There are two types of interest payments
	1. **Fixed**, Where the interest paid on principal is fixed and does not vary. Example of such kind of security is coupon based bonds, where the interest (coupon value) on principal is paid annually or semi-annually and the amount is fixed.
	2. **Floating**
- Interest rate swaps is the market where exchange of fixed rate of interest for floating interest rate happens.
## 1.8 Inflation Proof Bonds
- These bonds are an effective way of ensuring that income does not get eroded by inflation.
- The coupon value and principal is linked to indices which measure inflation, so as the inflation rises, so does the coupon and principal amount of bonds.
## 1.9 Forwards and Futures
- A **Forward contract** is a customized derivative contract obligating counterparties to buy or sell an asset at specified price on a future date.
	- The asset could be equity, bonds, commodities, currency etc.
	- It is non-standardized in nature. I.e. it can not be exchanged in markets.
	- The amount paid for the asset at the time of delivery (**Maturity**) is called **Delivery Price**. 
	- At the time the contract is made, value of forward contract is zero.
	- The value of forward contract changes from initially 0 to the difference between the spot price of asset at delivery and the delivery price.
	- One con associated with Forward Contracts is the **Counterparty Risk**, i.e. one of the party may default.
	- Whereas a pro associated with Forward Contracts is that they're highlt customizable i.e. their maturity and contract sizes can be customized.
	- Forward Contracts are mainly used for Hedging purposes.
- A **Future Contract** is similar to Forward contract, where the differences being, 
	- Futures are standardized in nature. i.e. they could be traded in exchange.
		- Hence they are more liquid than Forwards.
	- Future contracts settle everyday, i.e. P/L from the future position is calculated and the difference is paid out everyday. This is called **Marking to the Market**
		- This reduces the risk of one party defaulting.
		- Exchanges insist that traders must deposit an intial sum of amount, called **Initial Margin**, in an account called **Margin Account**. As the position of asset is market to market daily, money is deposited/withdrawan from this marhin account.
		- Traders must always maintain amount as margin above a minimum threshold called **Maintainance Margin**. 
	- Hence value of a Future Contract at any point in its lifetime is 0. 
	- Future Contracts are mainly used for speculation purposes.
	- A Future contract
		- specifies the asset being invested in.
		- specifies the quantity of asset to be delivered.
		- specifies when the asset is to be delivered.
	- 
### Forward Price and Spot Price Relationship
- Given constant interest rate holds, Forward price of an asset is related to Spot price by
	$$\displaystyle{F=S(t)\times{e^{r[T-t]}}}$$
	where,
	$F$ = Forward Price
	$S(t)$ = Spot price at some time $t$
	$r$ = rate of interest
	$T$ = Time period (in years)
- They share a linear relationship.
- If the relationship is violated, there's an arbitrage opportunity.
	- The Standard economic argument then says that investors will act quickly to exploit the opportunity and in the process, prices will adjust to eliminate it.
### Commodity Futures
- Futures on Commodity don't always obey the no arbitrage law because of the messy topic of Storage.
- Future prices are always higher than the theoritical no-storage-cost amount.
- The holder of the contract must always compensate the holder of the commodity for his storage costs.
	- This cost is described in terms of percentage by an adjustment $s$ to risk free rate of return.
- Most people holding the commodity are benifitting from it in some way. It is commonly measured in terms of **convenience yield**, $c$. Hence the Relationship between Forward and Spot prices becomes,
	$$\displaystyle{F=S(t)\times{e^{(r+s-c)[T-t]}}}$$
- Market is said to be in **backwardation** if, $\displaystyle{F\lt S(t)\times{e^{r[T-t]}}}$
- Market is said to be in **contango** if, $\displaystyle{F\gt S(t)\times{e^{r[T-t]}}}$
### FX Futures
#todo
### Index Futures
- Future Contracts on Stock Indices are settled in Cash.
- Similar to storage for Commodity Futures, here we have to deal with Dividends.
	$$\displaystyle{F = S(t)\times{e^{(r-q)[T-t]}}}$$
- This is an approximation because dividend yield is not continuous.

# Ch02: Derivatives
A derivative is a term used to describe a contract based on an underlying asset. 
## Options
> **Definition**: An option is a contract, which gives its holder, the right, but not the obligation, to buy or sell a specific quantity of underlying asset, at a specific price (strike/exercise price) on or before a specified date (Expiration date). 
- Unlike Forwards/Futures, we dont have the obligation to buy the asset.
	- We only exercise the option(buy the stock) if current stock price is higher than the exercise price.
	- Similarly, we only sell the stock if the current stock price is lower than the exercise price.
- **Exercise/Strike Price**, is the price at which you agree to buy/sell the asset.
- **Expiration Date**, is the date on/before which the owner must exercise the option.
- **Underlying Asset**, is the asset/instrument which the option is based on.
- **Payoff Function**, is a function of underlying asset at expiry, which tells us the maximum possible profitability.
- There are two types of Options:
	1. **Call Option**, is the right to **buy** a particular asset for an agreed amount, at a specified time in the future.
		$$\displaystyle{max(S-E, 0)}$$
		where, $S$ is the stock price at the expiry
		$E$, is the exercise/strike price.
	2. **Put Option**, is the right to **sell** a particular asset for an agreed amount, at a specified time in the future.
		$$max(E-S, 0)$$
- Unlike Futures/Forwards, there's an upfront payment you have to make for buying the option, called **Premium**, also called **Option Price (Value)**.
	$$Premium = Intrinsic\ Value + Extrinsic\ Value$$
- **Intrinsic Value**, is the profit if we exercise the option at its present value.
	- Intrinsic Value (profit) is either positive (If the market goes in our favour) or 0 (If it goes in opposite direction).
	- For a Call Option: $IV= max(S-E,0)$
	- For a Put Option: $IV= max(E-S,0)$
	- I.V. is also defined as how much option in In the Money (ITM)
- **Extrinsic Value**, is a function of two variables
	1. **Time Value[^5]**, is the major constituent of Extrinsic Value.
		- It refers to portion of option's premium that is attributable to amount of time remaining untill expiration of contract.
		- It is also defined as amount an investor is willing to pay above an option's intrinsic value in hope that the underlying security will become more profitable. 
			$Time\ Value = Premium - Intrinsic Value$
		- Generally, greater the time left till expiration, greater the time value of option.
	2. **Implied Volatility**
#### Relationship of Asset with Strike Price
An Option is either
1. **In the Money(I.T.M)** (profitable)
	- An option with positive intrinsic value.
	- Maximum probability of making a profit, hence large premium.
	- Big profits and Big losses.
	- More ITM the option is, greater the Intrinsic Value, lesser the time value.
2. **At the Money(A.T.M)** (Break-Even)
	- An option with 0 Intrinsic Value.
	- Moderate probability of making a profit, hence Moderate premium.
	- Moderate profits and Moderate losses.
	- Time Value of the Option is greatest at ATM (E=S), because current I.V. is 0 and Potential for Intrinsic Value to begin to rise is greatest at this point.
3. **Out of the Money(O.T.M.)** (In Loss)
	- An option with 0 Intrinsic Value.
	- Very low probability of making a profit, hence low premium.
	- Lesser profits and Lesser losses.
	- For deep OTM options, Time Value is less and Intrinsic Value is 0.

- For a fixed strike price $E$,

|      | ITM        | ATM       | OTM        |
| ---- | ---------- | --------- | ---------- |
| Call | $(S\gt E)$ | $(S = E)$ | $(S\lt E)$ |
| Put  | $(S\lt E)$ | $(S = E)$ | $(S\gt E)$ |


> **Example**: A stock is currently selling for $50.
> - If you buy the stock, and
> 	- stock goes to $80, you make a profit of $30. (60% profit on initial investment.)
> 	- stock falls to $30, you make a loss of $20. (40% loss on initial investment.)
> - If you buy a call option for $5, which specifies the strike price to be $60 and has an expiration of 1 month. If
> 	- stock rises to $80, you exercise the option, buy stock for $60, sell it for $80. Make a profit of $15 ($5 premium). (300% profit on i.i.)
> 	- stock falls to $30. You don't exercise the option. You make a loss of $5(premium). (100% loss on i.i.)
> - If you already own the stock for $50, and you buy a put option worth $4, with strike price of $37 and expiration date 1 month, and
> 	- stock falls to $25, you exercise the option. Sell the stock at $37, make a profit of $8. (200% profit on i.i.)
> 	- Stock rises to $70. You dont exercise the option. Make a loss of $4 (100% of i.i.)

- Options put a limit our losses, unlike Futures where you have to buy the asset for the specified price.
- Unike Futures, Options have a non-linear relationship with underlying asset
- Calls and Put are two simplest type of options. 
- **Long Position**, is a positive amount of quantity. (E.g. When someone owes us shares)
- **Short Position**, is a negative amoont of quantity. (E.g. when we owe someone shares)

### Relation between Strike Price and Options Premium
- If the Strike Price is higher, Premium for Put Option also increases and Premium on Call Option decreases.
- If the Strike Price is lower, Premium for Put Option also decreases and Premium on Call Option increases.
	$$Put\ Options\ Premium \propto Strike\ Price\propto \frac{1}{Call\ Options\ Premium}$$

## Payoff Diagrams
- We could visualise the value of the option at expiry as function of underlying stock price using payoff diagram.
![](img/Pasted%20image%2020221102132740.png) ![](img/Pasted%20image%2020221102132807.png)
- Payoff Diagrams only show value (not profit) of an option at expiry (using payoff functions.), since it does not take premium into account.
- Payoff Diagram is USeful since they simplify analysis of complex strategies involving multiple options.
### Profit Diagram
- It Visualises the profit from option at expiry.
- It is derived from payoff diagram where we also account for premium paid for option.
- We subtract the premium amount from payoff value (Shift the graph vertically in the negative direction by premium amount.)
- It shows how far ITM the asset must be at expiry before option turns profitable.
- ![](img/Pasted%20image%2020221102133517.png)
- In order to break-even, the option must be 
- Does not take into account the time-value of money

# References


[^1]: https://www.drwealth.com/cum-dividend-vs-ex-dividend/
[^2]: https://qr.ae/pvVYkT
[^3]: http://www.moneychimp.com/articles/finworks/continuous_compounding.htm
[^4]: http://www-stat.wharton.upenn.edu/~waterman/Teaching/IntroMath99/Class04/Notes/node13.htm
[^5]: https://www.investopedia.com/articles/optioninvestor/02/021302.asp