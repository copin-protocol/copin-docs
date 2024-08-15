# Fees Structure

## Fee Structure Overview

In the trading industry, fees are typically calculated based on the total trading size of a position (collateral x leverage). On Copin.io, there are three types of fees that users need to be aware of:

1. **Copin Fees**
2. **Execution Fees**
3. **PerpDEX/Liquidity Fees**

These fees cover the costs associated with using the Copin platform, executing copy trades, and utilizing the underlying PerpDEX platform (e.g., gTrade).

<table><thead><tr><th width="142">Fee type</th><th width="191">Fee formula ($)</th><th width="185">When charging</th><th>How to check</th></tr></thead><tbody><tr><td>Copin Fees</td><td>0.025% * trading size</td><td>Charged when an order is recorded as executed.</td><td><p>You can find this fee in the orders table of your copy position.</p><p>Alternatively, check the log of the wallet's transaction hash under <code>ChargeProtocolFee</code>. Example: <a href="https://arbiscan.io/tx/0xb9f6de683aef7df5dd5dd5096766b9d27c191783711cdb775aea224064ae5c1a#eventlog">Arbiscan Log</a>.</p></td></tr><tr><td>Execution Fees</td><td><p><strong>Order Fees</strong>: Calculated using a fast gas fee rate.</p><p><strong>SL/TP Fees</strong>: Calculated using a safe low gas fee rate.</p></td><td><p></p><p>Charged per order and for SL/TP execution.</p></td><td>You can find this fee in the log of the wallet's transaction hash under <code>ChargeExecutorFee</code>. Example: <a href="https://arbiscan.io/tx/0xb9f6de683aef7df5dd5dd5096766b9d27c191783711cdb775aea224064ae5c1a#eventlog">Arbiscan Log</a>.</td></tr><tr><td>PerpDEX Fees (e.g., gTrade)</td><td><p>0.08% * Trade Size</p><p>(minimum fee of $4)</p></td><td>Charged when an order is executed.</td><td><p></p><p>For open positions, this fee reduces the collateral.</p><p>For increase, decrease, or close positions, this fee is included in the PnL (Profit and Loss) calculation.</p></td></tr></tbody></table>

By understanding these fees, you can better manage your costs and maximize your copy-trading efficiency.
