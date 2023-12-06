---
description: Steps to set up copy trading with Copin Analyzer
---

# How to use Copy Trading?

### **Step 1: Select a trader to copy**

Click on the wallet address of the trader you want to copy. Then click on the **\[Copy Trader]** button on that wallet address's profile page.

<figure><img src="../../.gitbook/assets/Screen Shot 2023-09-18 at 14.40.40.png" alt=""><figcaption><p>Pick the trader you want to copy</p></figcaption></figure>

<figure><img src="../../.gitbook/assets/Screen Shot 2023-09-18 at 14.42.55.png" alt=""><figcaption><p>Click on the 'Copy Trader' to start Copy</p></figcaption></figure>

### **Step 2: Copy Trader Settings**

Select and fill in all the required information in the copy setup section.

<figure><img src="../../.gitbook/assets/Screen Shot 2023-09-18 at 15.02.07.png" alt=""><figcaption><p>Copy Trade Setting</p></figcaption></figure>

**Copy Information**

* **\[1] - Title:** Name the trader you choose to copy. The #copy-stats channel in Copin's Discord will have notifications about real-time copy orders. So, the more unique and memorable the name, the easier it will be for you to check.
* **\[2] - Max Margin Per Order:**&#x20;
* **\[3] - Trading Pair:** Select the pairs you want to copy. You should check if the trader you choose is performing well in trading altcoins before selecting to copy.
* **\[4] - Leverage slider**: Choose the leverage level you desire. Higher leverage involves higher risk; you should test at x20 or lower.
* **\[5] - Reverse Copy**: This is the reverse copy feature. Reverse copying requires you to know how to use backtesting to allocate capital appropriately to be profitable.

**Risk Management**

* **\[6] - Volume Protection**: Always open. Instead of setting a copy order for $100 and using up the entire $100, Copin will read the last 10 orders of the trader you choose to copy and allocate capital accordingly. For example, if they usually trade with $1000 but now only trade with $500 (which is 50%), when you copy, you will only place a $50 order (which is 50%) if you set Volume Per Order at $100.
* **\[7] - Stoploss Amount**: Enter the acceptable loss amount. You should use backtesting to determine appropriate stop loss levels for each trader (each trading style) to generate profits.
* **\[8] - Max Volume Multiplier:** Allows you to limit the amount you invest in a copied position.
* **\[9] - Skip Low Leverage:** Copin Analyzer will not execute the order that has leverage lower than the leverage you are setting.

**Copy Platform**

* **\[10] - Platform**: Currently, the default is BingX. Because Copin focuses on user profitability during beta testing, Copin prioritizes copying to CEX to optimize fees and slippage. If you want to copy to DEX, you can wait until Copin releases the official version.
* **\[11] - Your BingX API Key:** Enter your BingX API Key.
* **\[12] - Your BingX Secret Key:** Enter your BingX Secret Key.

{% hint style="info" %}
In this Beta version, Copin Analyzer only supports copy trading through our partner BingX. For detailed step-by-step instructions on connecting your BingX account, visit [**http://tutorial.copin.io/**](http://tutorial.copin.io/)
{% endhint %}
