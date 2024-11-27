# Integration Docs

## Introduction

Welcome to the Copin Integration Guide! This guide helps developers, partners, and traders seamlessly connect with Copin’s features, such as trader profiles, position data, and leaderboards, to enhance their platforms.

Integrating with Copin unlocks trading insights, transaction data, and performance metrics, offering valuable information to your users and building transparency and trust. Leaderboard integration further boosts engagement by showcasing top traders and encouraging competition.

With clear steps, examples, and URLs, this guide ensures a smooth integration process, enabling you to fully utilize Copin’s data-rich ecosystem.

## Protocol List

Copin partners with a variety of perpetual exchanges, offering users access to detailed trading data and insights. Each integration provides unique benefits, allowing easy access to information from preferred protocols. Here is the current list of supported perpdex protocols:

<table data-header-hidden><thead><tr><th width="194">PROTOCOL</th><th width="130">SHORT KEY</th><th>NAME</th><th>CHAIN</th><th>ACTIVE</th><th>ALLOW COPY</th></tr></thead><tbody><tr><td><strong>PROTOCOL</strong></td><td><strong>SHORT KEY</strong></td><td><strong>NAME</strong></td><td><strong>CHAIN</strong></td><td><strong>ACTIVE</strong></td><td><strong>ALLOW COPY</strong></td></tr><tr><td>GMX</td><td>GMA</td><td>GMX</td><td>Arbitrum</td><td>Yes</td><td>Yes</td></tr><tr><td>GMX_V2</td><td>GMA2</td><td>GMX V2</td><td>Arbitrum</td><td>Yes</td><td>Yes</td></tr><tr><td>KWENTA</td><td>KWO</td><td>Kwenta</td><td>Optimism</td><td>Yes</td><td>Yes</td></tr><tr><td>POLYNOMIAL</td><td>POO</td><td>Polynomial</td><td>Optimism</td><td>Yes</td><td>Yes</td></tr><tr><td>DEXTORO</td><td>DEO</td><td>Dextoro</td><td>Optimism</td><td>Yes</td><td>Yes</td></tr><tr><td>CYBERDEX</td><td>CYO</td><td>CyberDEX</td><td>Optimism</td><td>Yes</td><td>Yes</td></tr><tr><td>SYNTHETIX_V3</td><td>SYB3</td><td>Synthetix V3</td><td>Base</td><td>Yes</td><td>No</td></tr><tr><td>GNS</td><td>GNA</td><td>gTrade</td><td>Arbitrum</td><td>Yes</td><td>Yes</td></tr><tr><td>GNS_POLY</td><td>GNP</td><td>gTrade</td><td>Polygon</td><td>Yes</td><td>Yes</td></tr><tr><td>LEVEL_BNB</td><td>LEB</td><td>Level</td><td>BNB Chain</td><td>Yes</td><td>Yes</td></tr><tr><td>LEVEL_ARB</td><td>LEA</td><td>Level</td><td>Arbitrum</td><td>Yes</td><td>Yes</td></tr><tr><td>MUX_ARB</td><td>MUA</td><td>MUX</td><td>Arbitrum</td><td>Yes</td><td>Yes</td></tr><tr><td>EQUATION_ARB</td><td>EQA</td><td>Equation</td><td>Arbitrum</td><td>Yes</td><td>Yes</td></tr><tr><td>APOLLOX_BNB</td><td>APB</td><td>ApolloX</td><td>BNB Chain</td><td>Yes</td><td>Yes</td></tr><tr><td>AVANTIS_BASE</td><td>AVB</td><td>Avantis</td><td>Base</td><td>Yes</td><td>Yes</td></tr><tr><td>LOGX_BLAST</td><td>LOB</td><td>LogX</td><td>Blast</td><td>Yes</td><td>No</td></tr><tr><td>LOGX_MODE</td><td>LOM</td><td>LogX</td><td>Mode</td><td>Yes</td><td>No</td></tr><tr><td>MYX_ARB</td><td>MYA</td><td>MYX</td><td>Arbitrum</td><td>Yes</td><td>No</td></tr><tr><td>HMX_ARB</td><td>HMA</td><td>HMX</td><td>Arbitrum</td><td>Yes</td><td>Yes</td></tr><tr><td>VELA_ARB</td><td>VEA</td><td>Vela</td><td>Arbitrum</td><td>Yes</td><td>Yes</td></tr><tr><td>KTX_MANTLE</td><td>KTM</td><td>KTX</td><td>Mantle</td><td>Yes</td><td>No</td></tr><tr><td>YFX_ARB</td><td>YFA</td><td>YFX</td><td>Arbitrum</td><td>Yes</td><td>No</td></tr><tr><td>KILOEX_OPBNB</td><td>KIO</td><td>KiloEx</td><td>opBNB</td><td>Yes</td><td>Yes</td></tr><tr><td>ROLLIE_SCROLL</td><td>ROS</td><td>Rollie</td><td>Scroll</td><td>Yes</td><td>Yes</td></tr><tr><td>PERENNIAL_ARB</td><td>PEA</td><td>Perennial</td><td>Arbitrum</td><td>Yes</td><td>No</td></tr><tr><td>MUMMY_FANTOM</td><td>MUF</td><td>Mummy</td><td>Fantom</td><td>Yes</td><td>Yes</td></tr><tr><td>MORPHEX_FANTOM</td><td>MOF</td><td>Morphex</td><td>Fantom</td><td>Yes</td><td>Yes</td></tr><tr><td>HYPERLIQUID</td><td>HLP</td><td>Hyperliquid</td><td>Hyperliquid L1</td><td>Yes</td><td>No</td></tr><tr><td>SYNFUTURE_BASE</td><td>SYB</td><td>Synfutures</td><td>Base</td><td>Yes</td><td>No</td></tr><tr><td>DYDX</td><td>DYD</td><td>dYdX</td><td>dydX Chain</td><td>Yes</td><td>No</td></tr><tr><td>BSX_BASE</td><td>BSB</td><td>BSX</td><td>Base</td><td>Yes</td><td>No</td></tr><tr><td>UNIDEX_ARB</td><td>UNA</td><td>UniDex</td><td>Arbitrum</td><td>Yes</td><td>No</td></tr><tr><td>VERTEX_ARB</td><td>VEA</td><td>Vertex</td><td>Arbitrum</td><td>Yes</td><td>No</td></tr></tbody></table>

## How to integrate Copin?

Integrators can access key features such as the **Trader Profile**, **Position Details**, and **Leaderboard** via the following URLs.

### 1. Trader Profile

The trader profile endpoint allows integrators to access detailed information about individual traders. To retrieve this data, use the following URL format:

```bash
https://app.copin.io/trader/[trader_address]/[protocol]?utm_source=[protocol]
```

Parameters:

* **`trader_address`**: Address of the trader.\
  Example: `0xCf9D6C81167b183A384964d0A2ed2234feF81BDC`
* **`protocol`**: Selected protocol from the [protocol list](https://docs.copin.io/features/developer/integration-docs#protocol-list).\
  Example: `KILOEX_OPBNB`

Example URL:

```bash
https://app.copin.io/trader/0xCf9D6C81167b183A384964d0A2ed2234feF81BDC/kiloex_opbnb?time=FULL&utm_source=GNS
```

### 2. Position Details

To view specific position details, you can use the following endpoint:

```bash
https://app.copin.io/[protocol]/position/[order_tx_hash]?account=[trader_address]&tx_hash=[order_tx_hash]&log_id=[event_log_id]&side=[side]&utm_source=[protocol]
```

Parameters:

* **`protocol`**: Selected protocol from the protocol list.\
  Example: `GMX_V2`
* **`trader_address`**: Address of the trader.\
  Example: `0x08c788aFdACF6cf81180D2bBBE42A7434D0C7A92`\

* **`order_tx_hash`**: Transaction hash of the order.\
  Example: `0xd8779a7c74a71f6c9f049fe83957fb90d76cf0fef687cb25773cb4d713ad6eae`\

* **`event_log_id`**: Log ID of the event.\
  Example: `43`
* **`side`**: \[long | short]\
  Example: `long`

Example URL:

```bash
  - https://app.copin.io/GMX_V2/position/0xd8779a7c74a71f6c9f049fe83957fb90d76cf0fef687cb25773cb4d713ad6eae?account=0x08c788aFdACF6cf81180D2bBBE42A7434D0C7A92&log_id=43&side=long&utm_source=GMX_V2=
```

> **Note:** The following protocols do not support this feature:
>
> * Hyperliquid

### 3. Leaderboard

The leaderboard endpoint provides access to weekly or monthly trader rankings. Use the following URL format to retrieve leaderboard data:

```bash
https://app.copin.io/[protocol]/leaderboard?leaderboard_type=[type]&utm_source=[protocol]
```

* **`protocol`**: Selected protocol from the protocol list.\
  Example: `GNS`
* **`leaderboard_type`**: Type of leaderboard. Can be `WEEK` or `MONTH` (default: `MONTH`).

Example URLs:

```bash
https://app.copin.io/GNS/leaderboard?utm_source=GNS
```

```bash
https://app.copin.io/GNS/leaderboard?leaderboard_type=WEEK&utm_source=GNS
```

## **Media Kit**

For branding and promotional purposes, please refer to the official media files, which should not be altered. You can access them here: [Media Kit](https://drive.google.com/drive/folders/1DVz6YyimUK6qX8ztRCge3B5Gj-wzeyxX?usp=sharing)

## **Contact Information**

For further inquiries or technical support, please contact us via Telegram: [Telegram: LeeCopin](https://t.me/leecopin)
