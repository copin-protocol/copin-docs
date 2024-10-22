# Copin Integrators

## Protocol List

The list of Perp Dexs has been indexed from Copin Analyzer

<table data-header-hidden><thead><tr><th width="194">PROTOCOL</th><th width="130">SHORT KEY</th><th>NAME</th><th>CHAIN</th><th>ACTIVE</th><th>ALLOW COPY</th></tr></thead><tbody><tr><td><strong>PROTOCOL</strong></td><td><strong>SHORT KEY</strong></td><td><strong>NAME</strong></td><td><strong>CHAIN</strong></td><td><strong>ACTIVE</strong></td><td><strong>ALLOW COPY</strong></td></tr><tr><td>GMX</td><td>GMA</td><td>GMX</td><td>Arbitrum</td><td>Yes</td><td>Yes</td></tr><tr><td>GMX_V2</td><td>GMA2</td><td>GMX V2</td><td>Arbitrum</td><td>Yes</td><td>Yes</td></tr><tr><td>KWENTA</td><td>KWO</td><td>Kwenta</td><td>Optimism</td><td>Yes</td><td>Yes</td></tr><tr><td>POLYNOMIAL</td><td>POO</td><td>Polynomial</td><td>Optimism</td><td>Yes</td><td>Yes</td></tr><tr><td>DEXTORO</td><td>DEO</td><td>Dextoro</td><td>Optimism</td><td>Yes</td><td>Yes</td></tr><tr><td>CYBERDEX</td><td>CYO</td><td>CyberDEX</td><td>Optimism</td><td>Yes</td><td>Yes</td></tr><tr><td>SYNTHETIX_V3</td><td>SYB3</td><td>Synthetix V3</td><td>Base</td><td>Yes</td><td>No</td></tr><tr><td>GNS</td><td>GNA</td><td>gTrade</td><td>Arbitrum</td><td>Yes</td><td>Yes</td></tr><tr><td>GNS_POLY</td><td>GNP</td><td>gTrade</td><td>Polygon</td><td>Yes</td><td>Yes</td></tr><tr><td>LEVEL_BNB</td><td>LEB</td><td>Level</td><td>BNB Chain</td><td>Yes</td><td>Yes</td></tr><tr><td>LEVEL_ARB</td><td>LEA</td><td>Level</td><td>Arbitrum</td><td>Yes</td><td>Yes</td></tr><tr><td>MUX_ARB</td><td>MUA</td><td>MUX</td><td>Arbitrum</td><td>Yes</td><td>Yes</td></tr><tr><td>EQUATION_ARB</td><td>EQA</td><td>Equation</td><td>Arbitrum</td><td>Yes</td><td>Yes</td></tr><tr><td>APOLLOX_BNB</td><td>APB</td><td>ApolloX</td><td>BNB Chain</td><td>Yes</td><td>Yes</td></tr><tr><td>AVANTIS_BASE</td><td>AVB</td><td>Avantis</td><td>Base</td><td>Yes</td><td>Yes</td></tr><tr><td>LOGX_BLAST</td><td>LOB</td><td>LogX</td><td>Blast</td><td>Yes</td><td>No</td></tr><tr><td>LOGX_MODE</td><td>LOM</td><td>LogX</td><td>Mode</td><td>Yes</td><td>No</td></tr><tr><td>MYX_ARB</td><td>MYA</td><td>MYX</td><td>Arbitrum</td><td>Yes</td><td>No</td></tr><tr><td>HMX_ARB</td><td>HMA</td><td>HMX</td><td>Arbitrum</td><td>Yes</td><td>Yes</td></tr><tr><td>VELA_ARB</td><td>VEA</td><td>Vela</td><td>Arbitrum</td><td>Yes</td><td>Yes</td></tr><tr><td>KTX_MANTLE</td><td>KTM</td><td>KTX</td><td>Mantle</td><td>Yes</td><td>No</td></tr><tr><td>YFX_ARB</td><td>YFA</td><td>YFX</td><td>Arbitrum</td><td>Yes</td><td>No</td></tr><tr><td>KILOEX_OPBNB</td><td>KIO</td><td>KiloEx</td><td>opBNB</td><td>Yes</td><td>Yes</td></tr><tr><td>ROLLIE_SCROLL</td><td>ROS</td><td>Rollie</td><td>Scroll</td><td>Yes</td><td>Yes</td></tr><tr><td>PERENNIAL_ARB</td><td>PEA</td><td>Perennial</td><td>Arbitrum</td><td>Yes</td><td>No</td></tr><tr><td>MUMMY_FANTOM</td><td>MUF</td><td>Mummy</td><td>Fantom</td><td>Yes</td><td>Yes</td></tr><tr><td>MORPHEX_FANTOM</td><td>MOF</td><td>Morphex</td><td>Fantom</td><td>Yes</td><td>Yes</td></tr><tr><td>HYPERLIQUID</td><td>HLP</td><td>Hyperliquid</td><td>Hyperliquid L1</td><td>Yes</td><td>No</td></tr><tr><td>SYNFUTURE_BASE</td><td>SYB</td><td>Synfutures</td><td>Base</td><td>Yes</td><td>No</td></tr><tr><td>DYDX</td><td>DYD</td><td>dYdX</td><td>dydX Chain</td><td>Yes</td><td>No</td></tr><tr><td>BSX_BASE</td><td>BSB</td><td>BSX</td><td>Base</td><td>Yes</td><td>No</td></tr></tbody></table>

## How to integrate Copin?

Integrators can use for exploration are the trader profile, position details and leaderboard from Copin via URL with format below:

1. ### Trader Profile

{% hint style="info" %}
https://app.copin.io/trader/\[trader\_address]/\[protocol]?utm\_source=\[protocol]
{% endhint %}

* trader\_address:
  * Ex: 0xCf9D6C81167b183A384964d0A2ed2234feF81BDC
* protocol:
  * \[PROTOCOL] from [Protocol List](https://decentralab.larksuite.com/docx/DW2gdRTyooA0Drx1x0Bu9lvesUc#share-VVAYdv8uqoHSLZxFV9ruRAZIs8b)
  * Ex: KILOEX\_OPBNB
* Example:
  * https://app.copin.io/trader/0xCf9D6C81167b183A384964d0A2ed2234feF81BDC/kiloex\_opbnb?time=FULL\&utm\_source=GNS

2. ### Position Details

{% hint style="info" %}
https://app.copin.io/\[protocol]/position/\[order\_tx\_hash]?account=\[trader\_address]\&tx\_hash=\[order\_tx\_hash]\&log\_id=\[event\_log\_id]\&utm\_source=\[protocol]
{% endhint %}

* protocol:
  * \[PROTOCOL] from [Protocol List](https://decentralab.larksuite.com/docx/DW2gdRTyooA0Drx1x0Bu9lvesUc#share-VVAYdv8uqoHSLZxFV9ruRAZIs8b)
  * Ex: GMX\_V2
* trader\_address:
  * Ex: 0x08c788aFdACF6cf81180D2bBBE42A7434D0C7A92
  * https://arbiscan.io/address/0x08c788aFdACF6cf81180D2bBBE42A7434D0C7A92
* order\_tx\_hash:
  * Ex: 0xd8779a7c74a71f6c9f049fe83957fb90d76cf0fef687cb25773cb4d713ad6eae
  * https://arbiscan.io/tx/0xd8779a7c74a71f6c9f049fe83957fb90d76cf0fef687cb25773cb4d713ad6eae
* event\_log\_id:
  * Ex: 43
* Example:
  * https://app.copin.io/GMX\_V2/position/0xd8779a7c74a71f6c9f049fe83957fb90d76cf0fef687cb25773cb4d713ad6eae?account=0x08c788aFdACF6cf81180D2bBBE42A7434D0C7A92\&log\_id=43\&utm\_source=GMX\_V2

{% hint style="warning" %}
List of protocols that do not support this feature include:

* Hyperliquid
{% endhint %}

3. ### Leaderboard

{% hint style="info" %}
https://app.copin.io/\[protocol]/leaderboard?leaderboard\_type=\[type]\&utm\_source=\[protocol]
{% endhint %}

* protocol:
  * \[PROTOCOL] from [Protocol List](https://decentralab.larksuite.com/docx/DW2gdRTyooA0Drx1x0Bu9lvesUc#share-VVAYdv8uqoHSLZxFV9ruRAZIs8b)
  * Ex: GNS
* type:
  * Trader rankings by week or month
  * Value: WEEK | MONTH
  * Default: MONTH
* Example:
  * https://app.copin.io/GNS/leaderboard?utm\_source=GNS
  * https://app.copin.io/GNS/leaderboard?leaderboard\_type=WEEK\&utm\_source=GNS

## Media Kit

For branding purposes, please do not modify these files: [https://drive.google.com/drive/folders/1DVz6YyimUK6qX8ztRCge3B5Gj-wzeyxX?usp=sharing](https://drive.google.com/drive/folders/1DVz6YyimUK6qX8ztRCge3B5Gj-wzeyxX?usp=sharing)

## Contact

Telegram: [https://t.me/leecopin](https://t.me/leecopin)
