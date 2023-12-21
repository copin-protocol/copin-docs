# Backtesting

Backtesting simulates trades made by a trader using real-time data and the capital allocation method of the system.

<figure><img src="../.gitbook/assets/image (43).png" alt=""><figcaption></figcaption></figure>

Backtests play a vital role within the Copin copy trading usecase by enabling users to assess the historical performance of traders or trading strategies before making the decision to copy them. These features offer valuable insights into how a specific trader or strategy has performed in the past, allowing users to evaluate its potential for future success. **Key features of backtesting in Copin Analyzer include:**

* Evaluating the performance of traders and selecting suitable traders based on historical data.
* Customizing backtest parameters and selecting specific intervals for testing.
* Analyzing backtest results to identify the most suitable trader or trading strategy.

## Single-backtesting

Single backtest is a great way to find traders who match your specific trading style. For example, if you're a risk-averse trader, you can use a single backtest to find traders with a low-risk tolerance.

<figure><img src="../.gitbook/assets/image (45).png" alt=""><figcaption></figcaption></figure>

To start backtesting any trader, please click on the **\[Backtest]** button next to the **\[Copy Trader]** button.

<figure><img src="../.gitbook/assets/image (46).png" alt=""><figcaption></figcaption></figure>

To initiate a backtest, you can specify the following parameters:

* **\[1] - Investment capital:** The initial amount of funds you intend to allocate for the backtested trader.
* **\[2] - Max Margin Per Order:** The amount you wish to allocate for the first order or position in the backtest.
* **\[3] - Trading pairs:** Select the specific trading pairs (such as BTC, ETH, UNI, LINK) that you want to include in the backtest.
* **\[4] - Leverage Slider:** Adjust the leverage level to simulate the trading conditions you wish to test.
* **\[5] - Reverse Copy:** Copin will execute the order that is the inverse of the trader's order.
* **\[6] - Look back to Protect Volume**: Average the trader's trading volume over the most recent 'X' orders as a protection mechanism. If the trader places an order much smaller than the average volume of 'X' orders, your account will also copy a percentage of the initially set volume.
* **\[7] - Stoploss Amount Per Position:** You can simulate the amount of money you can lose when the trade you copy reaches this threshold.
* **\[8] - Max Volume Multiplier:** Allows you to limit the amount you invest in a copied position. (Example: With a coefficient of x3 and a maximum amount per order of $100, the maximum volume of the copied position is $300 ($100 x 3). Any new trade volume of the trader exceeding this threshold will not be performed.)
* **\[9] - Start time - End time:** Define the desired time range for the backtest, specifying the start and end times to evaluate the trader's performance during that period.

By setting these parameters, you can conduct a backtest that reflects your investment capital, preferred position size, choice of trading pairs, leverage, and the specific time period you want to analyze. Once you have filled in the desired parameters, you can initiate the backtesting process by clicking on the **\[Simulate]** button.This action triggers the system to start running the backtest using the specified parameters and historical data. The platform will analyze the trader's performance based on the provided inputs and generate the backtest results, allowing you to evaluate the trader's historical performance and assess its suitability for your investment strategy.

<figure><img src="../.gitbook/assets/image (47).png" alt=""><figcaption></figcaption></figure>

After completing the backtest, you will receive the following results:

* **\[1] - Backtest Setting:** Show what you have set up before backtesting (Time Period, Investment Capital, Amount Per Position, Leverage, Max Volume Multiplier, Volume Protection, Stoploss).
* **\[2] - Suggestion & Backtest Results**
* **\[3] - Position Chart:** Show your trading activity on candlestick charts. You can see more intuitively how traders enter orders along with market fluctuations.
  * **Red arrow pointing down**: Short position is opened.
  * **Green arrow pointing up**: Long position is opened.
  * **White square**: Order closing point.

## Multi-backtesting

Multi-backtest allows you to quickly backtest multiple traders at the same time, making it easier for you to choose which trader best suits your strategy.

<figure><img src="../.gitbook/assets/image (48).png" alt=""><figcaption></figcaption></figure>

Once you've finished filtering traders in Trader Explore, you can select them all and start backtesting them immediately. This is a great way to quickly compare the performance of different traders.

<figure><img src="../.gitbook/assets/image (49).png" alt=""><figcaption></figcaption></figure>

Once you have set your strategy, you can view the backtest results with the traders. From here, you can easily compare, sort, or click the arrow button to see more details. The Backtest Result interface is similar to the Single Backtest section.

<figure><img src="../.gitbook/assets/image (50).png" alt=""><figcaption></figcaption></figure>

{% hint style="warning" %}
Make sure you backtest with any traders you already have or can filter out, to make sure you have a safe capital management allocation!
{% endhint %}
