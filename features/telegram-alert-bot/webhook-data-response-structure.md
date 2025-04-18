---
description: >-
  This document describes the structure of the webhook data response payload.
  The payload is typically sent via an HTTP POST request to a configured webhook
  endpoint.
---

# Webhook Data Response Structure

## 📘 Unified Webhook Structure

### **1. Watchlist Trader Alert**

```json
{
  "type": "TRADER",
  "name": "WH - Watchlist",
  "webhookUrl": "https://webhook.site/587b89ca-ea4b-4742-9993-6fc040e8dc72",
  "data": {
    "id": "6801bed617b6efe92ce65d15",
    "account": "0x3893209E93c68E7457ef722A4D974861F92859E8",
    "type": "OPEN",
    "isLong": true,
    "leverage": "2.0x",
    "token": "ETH",
    "volume": 9.9887,
    "price": 1587.5997,
    "positionId": "6801bed617b6efe92ce65d2a",
    "protocol": "GMX_V2",
    "time": "2025-04-18T02:54:09.000Z"
  },
  "timestamp": "2025-04-18T02:54:15.155Z"
}
```

### **2. Custom Trader Alert**

```json
{
  "type": "CUSTOM",
  "name": "WH - Custom Trader",
  "webhookUrl": "https://webhook.site/587b89ca-ea4b-4742-9993-6fc040e8dc72",
  "data": {
    "id": "6801c3a117b6efe92ce90c0e",
    "account": "0x3893209E93c68E7457ef722A4D974861F92859E8",
    "type": "OPEN",
    "isLong": true,
    "leverage": "2.0x",
    "token": "BTC",
    "volume": 9.9928,
    "price": 84820.9382,
    "positionId": "6801c3a117b6efe92ce90c17",
    "protocol": "GMX_V2",
    "time": "2025-04-18T03:14:36.000Z"
  },
  "timestamp": "2025-04-18T03:14:45.085Z"
}
```

### **3. Copy Trader Alert**

```json
{
  "type": "COPY_TRADE",
  "name": "Cold face",
  "webhookUrl": "https://webhook.site/587b89ca-ea4b-4742-9993-6fc040e8dc72",
  "data": {
    "activityLogId": "6801bedb2fa5dc9ca2d91268",
    "type": "OPEN",
    "token": "ETH",
    "account": "0x3893209E93c68E7457ef722A4D974861F92859E8",
    "isLong": true,
    "isReverse": false,
    "walletName": "Default 0x26C",
    "exchange": "HYPERLIQUID",
    "leverage": "2.00",
    "volume": 19.97,
    "price": "1,585.10",
    "isSuccess": true,
    "copyTradeTitle": "Cold face",
    "pnl": 0,
    "roi": 0,
    "userRef": "45657657567657567657",
    "protocol": "GMX_V2"
  },
  "timestamp": "2025-04-18T02:54:30.029Z"
}
```

***

## I. Root-Level Fields

<table data-header-hidden><thead><tr><th width="127.85546875"></th><th width="101.64453125"></th><th></th><th width="121.76171875"></th></tr></thead><tbody><tr><td><strong>Field Name</strong></td><td><strong>Type</strong></td><td><strong>Description</strong></td><td><strong>Applies To</strong></td></tr><tr><td>type</td><td>string</td><td><ul><li>TRADER – Track manual trader activity</li><li>CUSTOM – Triggered when trader matches custom filters</li><li>COPY_TRADE – Auto-executed trades copied from a trader</li></ul></td><td>All</td></tr><tr><td>name</td><td>string</td><td>Name of the alert group or custom label</td><td>All</td></tr><tr><td>webhookUrl</td><td>string</td><td>Webhook delivery URL</td><td>All</td></tr><tr><td>data</td><td>object</td><td>Payload containing full trade information</td><td>All</td></tr><tr><td>timestamp</td><td>string</td><td>When the webhook was sent (ISO 8601, UTC)</td><td>All</td></tr></tbody></table>

## II. Data Object Fields

<table data-header-hidden><thead><tr><th width="132.47265625"></th><th width="97.67578125"></th><th></th><th width="173.90234375"></th></tr></thead><tbody><tr><td><strong>Field Name</strong></td><td><strong>Type</strong></td><td><strong>Description</strong></td><td><strong>Applies To</strong></td></tr><tr><td>id</td><td>string</td><td>Unique ID for the trader action</td><td>TRADER, CUSTOM</td></tr><tr><td>activityLogId</td><td>string</td><td>Unique ID for copytrade log</td><td>COPY_TRADE</td></tr><tr><td>account</td><td>string</td><td>Trader's address</td><td>All</td></tr><tr><td>type</td><td>string</td><td><ul><li>OPEN: Opened a new position</li><li>INCREASE: Added more volume to current trade</li><li>DECREASE: Reduced partial volume</li><li>MODIFY: Modified position</li><li>CLOSE: Closed the position entirely</li></ul></td><td>All</td></tr><tr><td>isLong<br></td><td>boolean</td><td><ul><li>true = Long</li><li>false = Short</li></ul></td><td>All</td></tr><tr><td>leverage</td><td>string</td><td>Leverage used in the trade</td><td>All</td></tr><tr><td>token</td><td>string</td><td>Token being traded</td><td>All</td></tr><tr><td>volume</td><td>number</td><td>Trade size</td><td>All</td></tr><tr><td>price</td><td>number/string</td><td>Executed price<br></td><td>All</td></tr><tr><td>positionId</td><td>string</td><td>Position ID linked to this trade</td><td>TRADER, CUSTOM</td></tr><tr><td>protocol</td><td>string</td><td>Trading protocol/platform used</td><td>All</td></tr><tr><td>time</td><td>string</td><td>Trade execution time (ISO 8601, UTC)</td><td>TRADER, CUSTOM</td></tr><tr><td>exchange</td><td>string</td><td>Name of the exchange</td><td>COPY_TRADE</td></tr><tr><td>walletName</td><td>string</td><td>Name of the user’s wallet used in copytrade</td><td>COPY_TRADE</td></tr><tr><td>isReverse</td><td>boolean</td><td>Whether the copy is in reverse mode</td><td>COPY_TRADE</td></tr><tr><td>isSuccess</td><td>boolean</td><td>Whether the copy trade was successfully executed</td><td>COPY_TRADE</td></tr><tr><td>errorMsg</td><td>string</td><td>Error message (if copy trade failed)</td><td>COPY_TRADE(on fail)</td></tr><tr><td>copyTradeTitle</td><td>string</td><td>Campaign title for copy trade</td><td>COPY_TRADE</td></tr><tr><td>userRef</td><td>string</td><td>User 's reference code</td><td>COPY_TRADE</td></tr><tr><td>roi</td><td>number</td><td>Return on investment (decimal: 0.04 = 4%)</td><td>COPY_TRADE, TRADER (on CLOSE)</td></tr><tr><td>pnl</td><td>number</td><td>Profit or loss (in token units)</td><td>COPY_TRADE, TRADER (on CLOSE)</td></tr></tbody></table>

\
