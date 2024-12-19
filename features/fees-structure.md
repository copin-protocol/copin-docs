---
description: Fee Structures for Copy Trading on Copin
---

# Fees Structure

Copin provides detailed information about the fee structures applied when users engage in copy trading on Copin through platforms such as Hyperliquid, gTrade, and centralized exchanges (CEXs) like Bybit, OKX, BingX, Bitget, and Gate.

## 1. Fee Structure for Copy Trading on Hyperliquid

When users copy trade through Hyperliquid, the following fees apply:

<table><thead><tr><th width="142">Fee type</th><th width="191">Fee formula</th><th width="188">When charging</th><th>How to check</th></tr></thead><tbody><tr><td>Copin Builder fee</td><td>0.05% trade size of open order</td><td>Charged when <strong>opening/increasing</strong> a copy trade order and no fee when closing/decreasing an order.</td><td>You can check the fees in the <strong>"Trade History"</strong> tab of your Hyperliquid account.</td></tr><tr><td>Hyperliquid Trading Fee</td><td>Taker fee: 0.035% trade size</td><td>Charged when an order is executed. <a href="https://hyperliquid.gitbook.io/hyperliquid-docs/trading/fees">Trading fee structure of hyperliquid.</a></td><td>You can check the fees in the <strong>"Trade History"</strong> tab of your Hyperliquid account.</td></tr></tbody></table>

These fees are charged directly on the Hyperliquid platform and can be reviewed in the **"Trade History"** tab of your Hyperliquid account.

<figure><img src="../.gitbook/assets/Screenshot 2024-12-19 at 14.49.50.png" alt=""><figcaption></figcaption></figure>

## 2. Fee Structure for Copy Trading on gTrade &#x20;

In the trading industry, fees are typically calculated based on the total trading size of a position (collateral x leverage). On Copin.io, there are three types of fees that users need to be aware of:

1. **Copin Fees**
2. **Execution Fees**
3. **PerpDEX/Liquidity Fees**

These fees cover the costs associated with using the Copin platform, executing copy trades, and utilizing the underlying PerpDEX platform (e.g., gTrade).

<table><thead><tr><th width="142">Fee type</th><th width="191">Fee formula ($)</th><th width="188">When charging</th><th>How to check</th></tr></thead><tbody><tr><td>Copin Fees</td><td>0.025% * trading size</td><td>Charged when an order is recorded as executed.</td><td><p>You can find this fee in the orders table of your copy position.</p><p>Alternatively, check the log of the wallet's transaction hash under <code>ChargeProtocolFee</code>. Example: <a href="https://arbiscan.io/tx/0xb9f6de683aef7df5dd5dd5096766b9d27c191783711cdb775aea224064ae5c1a#eventlog">Arbiscan Log</a>.</p></td></tr><tr><td>Execution Fees</td><td><p><strong>Order Fees</strong>: Calculated using a fast gas fee rate.</p><p><strong>SL/TP Fees</strong>: Calculated using a safe low gas fee rate.</p></td><td><p></p><p>Charged per order and for SL/TP execution.</p></td><td>You can find this fee in the log of the wallet's transaction hash under <code>ChargeExecutorFee</code>. Example: <a href="https://arbiscan.io/tx/0xb9f6de683aef7df5dd5dd5096766b9d27c191783711cdb775aea224064ae5c1a#eventlog">Arbiscan Log</a>.</td></tr><tr><td>PerpDEX Fees (e.g., gTrade)</td><td><p>0.08% * Trade Size</p><p>(minimum fee of $4)</p></td><td>Charged when an order is executed.</td><td><p>For open positions, this fee reduces the collateral.</p><p>For increase, decrease, or close positions, this fee is included in the PnL (Profit and Loss) calculation.</p></td></tr></tbody></table>

## 3. Fee Structure for Copy Trading on CEXs (Bybit, OKX, BingX, Bitget, Gate)

When users copy trade on CEXs, the following policy applies:

* **Copin Fees**: Copin does **not charge any fees** for copy trading through CEXs.
* **Exchange Fees**: Standard trading fees as defined by the respective exchange apply.

**Referral Program Benefits**

To maximize benefits and receive enhanced support, users are encouraged to register their accounts through Copin’s referral links. Registering via these links ensures you gain access to exclusive advantages provided by our exchange partners.

You can find the referral links to our partner exchanges here: [Official Exchange Partners](https://docs.copin.io/welcome/official-link/exchange-partners).

***

For any questions or further details, please refer to the official Copin documentation or contact our support team.
