---
description: >-
  This guide will help you set up and connect your Hyperliquid API to Copin to
  enable seamless copy trading through 2 steps.
---

# Connect Hyperliquid

{% hint style="info" %}
**Notes:**

1. If you don't have a Hyperliquid account yet, [register here ](https://app.hyperliquid.xyz/join/COPIN)(Referral code: COPIN)
2. API wallets (also known as agent wallets) can perform actions on behalf of your account without having withdrawal permissions. You must still use your account's public address for info requests.
{% endhint %}

## Step 1: Create a Hyperliquid API

1. Visit the Hyperliquid API page: [https://app.hyperliquid.xyz/API](https://app.hyperliquid.xyz/API) and connect your wallet.
2. Complete the API Details:

* Name: Choose a name, e.g., `Copin_Copytrade`.
* Generate a Wallet Address: Click **\[Generate]**.
* Authorize the API Wallet: Click **\[Authorize API Wallet]**.

<figure><img src="../../.gitbook/assets/image (2).png" alt=""><figcaption></figcaption></figure>

3. Save Your Private Key:

* Set Maximum Validity: Choose MAX for up to 180 days.
* Save your Private Key.
* Click **\[Authorize]** to complete.

<figure><img src="../../.gitbook/assets/image (2) (1).png" alt=""><figcaption></figcaption></figure>

## Step 2: Connect API to Copin

1. Visit Copin Wallet Management: [https://app.copin.io/wallet-management](https://app.copin.io/wallet-management) and log in.
2. **\[Connect]** to Hyperliquid Exchange.

<figure><img src="../../.gitbook/assets/image (3).png" alt=""><figcaption></figcaption></figure>

3. Enter API Details:

* Hyperliquid Account Address: The wallet address you use to log into Hyperliquid (Hyperliquid's Master Account).

> **Note**: Visit [https://app.hyperliquid.xyz/subAccounts](https://app.hyperliquid.xyz/subAccounts) to identify the Master Account wallet.

* API Wallet Private Key: The private key saved from API creation.
* Wallet Name: Optional.

<figure><img src="../../.gitbook/assets/image (4).png" alt=""><figcaption></figcaption></figure>

4. Select "I agree to let Copin use the API to place orders", sign, and confirm your agreement to pay a 0.05% trade size when open order.&#x20;

> Learn more about copy-trade fee structure here: [https://docs.copin.io/features/fees-structure#id-1.-fee-structure-for-copy-trading-on-hyperliquid](https://docs.copin.io/features/fees-structure#id-1.-fee-structure-for-copy-trading-on-hyperliquid)

> **Note**: Ensure that the correct wallet used for signing is the Master Account of Hyperliquid. You can verify by clicking on the icon as shown below before selecting "Confirm."

<figure><img src="../../.gitbook/assets/image (5).png" alt=""><figcaption></figcaption></figure>

## FAQs

**1. Why am I getting the error "Can't approve builder fee Hyperliquid"?**

This error appears if the wallet used to connect the API to Copin is not the Master Account on Hyperliquid. To fix it:

* Verify that you are using the correct Master Account wallet by visiting [Hyperliquid’s SubAccounts page](https://app.hyperliquid.xyz/subAccounts).
* Ensure this Master Account wallet is entered and used to sign the connection to Copin.

**2. Why wasn’t my order executed?**

Orders may fail if the wrong wallet was used to sign the API connection. Double-check that the correct Master Account wallet is used for signing and connected properly to avoid any missed API calls.

**3. Can I manually close my copy position on Copin?**

Currently, you cannot manually close copy trade orders on Copin. To close a position, do so directly on Hyperliquid. Afterward, go to [Copin Wallet Management](https://app.copin.io/me/management), select your Hyperliquid wallet, and **Unlink** the closed position to prevent errors.

**4. Why is there a discrepancy in leverage for my copy trade order?**

Hyperliquid enforces different leverage limits for each trading pair. Copin uses the minimum leverage between your chosen setting and the maximum allowed by Hyperliquid for that pair.

* Example: For a WIF/USD trade, if you set leverage at 20x but Hyperliquid allows only 5x, the trade will execute at 5x leverage.

**5. Why do I see a PnL discrepancy in the Copy Opening Position Detail?**

Copin uses the PYTH oracle to obtain price information, while Hyperliquid has its pricing system. This may cause temporary PnL discrepancies, but prices will sync when the order is closed, reflecting Hyperliquid’s final data.

**6. Why are there multiple entries in my activities log?**

Hyperliquid's system uses partial order matching, so each partial fill appears as a separate entry in the activity log, unlike other sources that may group these as a single copy order.

{% hint style="info" %}
Join the Copin Global community on Telegram to get support here: [https://t.me/Copin\_io](https://t.me/Copin_io).
{% endhint %}

