# Public API docs

1. ## Get trader statistics

<table data-header-hidden><thead><tr><th width="124"></th><th></th></tr></thead><tbody><tr><td><strong>URL</strong></td><td>https://api.copin.io/public/KWENTA/position/statistic/filter</td></tr><tr><td><strong>Method</strong></td><td>POST</td></tr><tr><td><strong>Body</strong><br></td><td><ul><li><p>pagination:</p><ul><li>limit: number of records</li><li>offset: number of skipped records</li></ul></li><li>sortBy: supported all <code>fieldName</code> in ranges</li><li>sortType: <code>desc</code>, <code>asc</code></li><li><p>queries: array of</p><ul><li>fieldName: <code>type</code> <code>account</code></li><li><p>value:</p><ul><li>type: <code>D7</code>, <code>D15</code>, <code>D30</code>, <code>D60</code></li><li>account: EVM address</li></ul></li></ul></li><li><p>ranges: array of</p><ul><li><p>fieldName:</p><ul><li><code>lastTradeAtTs</code>Timestamp of last trade</li><li><code>runTimeDays</code> Number of days since the first trade</li><li><code>pnl</code> PnL including fee</li><li><code>realisedPnl</code>PnL without fee</li><li><code>avgRoi</code> Average ROI including fee</li><li><code>realisedAvgRoi</code>Average ROI without fee</li><li><code>totalGain</code> Total gain including fee</li><li><code>realisedTotalGain</code> Total gain without fee</li><li><code>totalLoss</code> Total loss including fee</li><li><code>realisedTotalLoss</code> Total loss without fee</li><li><code>totalFee</code>Total fee</li><li><code>totalVolume</code> Total volume</li><li><code>avgVolume</code>Average volume</li><li><code>maxRoi</code> Maximum ROI including fee</li><li><code>realisedMaxRoi</code> Maximum ROI without fee</li><li><code>maxDrawdown</code> Max drawdown including fee</li><li><code>realisedMaxDrawdown</code> Max drawdown without fee</li><li><code>totalTrade</code> Total trades</li><li><code>totalWin</code> Total wins</li><li><code>totalLose</code> Total loses</li><li><code>totalLiquidation</code> Total liquidations</li><li><code>winRate</code> Win Rate -- percent</li><li><code>profitRate</code> Total gain / (Total gain + Total loss) -- percent, including fee</li><li><code>realisedProfitRate</code>Total gain / (Total gain + Total loss) -- percent, without fee</li><li><code>longRate</code>Long Positions / Total Positions -- percent</li><li><code>orderPositionRatio</code> Total Orders / Total Positions</li><li><code>profitLossRatio</code> (Total gain / Total win) / (Total loss / Total lose) -- including fee</li><li><code>realisedProfitLossRatio</code>(Total gain / Total win) / (Total loss / Total lose) -- without fee</li><li><code>gainLossRatio</code> Total gain / Total loss -- including fee</li><li><code>realisedGainLossRatio</code> Total gain / Total loss -- without fee</li><li><code>avgLeverage</code>Average leverage</li><li><code>maxLeverage</code> Maximum leverage</li><li><code>minLeverage</code> Minimum leverage</li><li><code>avgDuration</code> Average duration in seconds</li><li><code>minDuration</code>Minimum duration in seconds</li><li><code>maxDuration</code> Maximum duration in seconds</li></ul></li><li>gte: numeric value</li><li>lte: numeric value</li></ul></li></ul></td></tr><tr><td><strong>Example request</strong><br></td><td><pre class="language-JSON"><code class="lang-JSON">{"pagination":{"limit":20,"offset":0},"queries":[{"fieldName":"type","value":"D30"}],"ranges":[{"fieldName":"realisedPnl","gte":1000},{"fieldName":"lastTradeAtTs","gte":1696240506809},{"fieldName":"totalWin","gte":5},{"fieldName":"realisedAvgRoi","gte":20},{"fieldName":"winRate","gte":80},{"fieldName":"realisedMaxDrawdown","gte":-30}],"sortBy":"realisedPnl","sortType":"desc"}
</code></pre></td></tr><tr><td><strong>Example response</strong></td><td><pre class="language-JSON"><code class="lang-JSON">{
    "data": [
        {
            "id": "656291e14350fb0b6981e6ce",
            "account": "0x9f431A46149bab70373B9C6867d2dB8C2F45aa11",
            "totalTrade": 10,
            "totalWin": 10,
            "totalLose": 0,
            "totalGain": 57060.90483687067,
            "realisedTotalGain": 53926.13225839167,
            "totalLoss": 0,
            "realisedTotalLoss": 0,
            "totalVolume": 3504221.760537487,
            "avgVolume": 350422.1760537487,
            "avgRoi": 33.43488693937744,
            "realisedAvgRoi": 37.47677597570163,
            "maxRoi": 104.1059947215304,
            "realisedMaxRoi": 109.65725913031952,
            "pnl": 53926.13225839167,
            "realisedPnl": 57060.90483687067,
            "maxPnl": 16673.619290696948,
            "realisedMaxPnl": 17269.147842961316,
            "maxDrawdown": 0,
            "realisedMaxDrawdown": 0,
            "maxDrawdownPnl": 0,
            "realisedMaxDrawdownPnl": 0,
            "winRate": 100,
            "profitRate": 100,
            "realisedProfitRate": 100,
            "orderPositionRatio": 2.1,
            "profitLossRatio": 0,
            "realisedProfitLossRatio": 0,
            "longRate": 100,
            "gainLossRatio": 57060.90483687067,
            "realisedGainLossRatio": 53926.13225839167,
            "avgDuration": 68629,
            "minDuration": 11976,
            "maxDuration": 206986,
            "avgLeverage": 20.210503401712398,
            "minLeverage": 5.020509333784338,
            "maxLeverage": 30.179561022789816,
            "totalLiquidation": 0,
            "totalLiquidationAmount": 0,
            "runTimeDays": 139,
            "lastTradeAtTs": 1701696239000,
            "totalFee": 3134.772578479,
            "type": "D30",
            "statisticAt": "2023-12-05T00:05:59.524Z",
            "lastTradeAt": "2023-12-04T13:23:59.000Z",
            "createdAt": "2023-11-26T00:31:28.532Z",
            "isOpenPosition": true,
            "protocol": "KWENTA"
        },
        ...
    ],
    "meta": {
        "limit": 20,
        "offset": 0,
        "total": 15,
        "totalPages": 1
    }
}
</code></pre></td></tr></tbody></table>

2. ## Get trader positions

<table data-header-hidden><thead><tr><th width="131"></th><th></th></tr></thead><tbody><tr><td><strong>URL</strong></td><td>https://api.copin.io/KWENTA/position/filter</td></tr><tr><td><strong>Method</strong></td><td>POST</td></tr><tr><td><strong>Body</strong><br></td><td><ul><li><p>pagination:</p><ul><li>limit: number of records</li><li>offset: number of skipped records</li></ul></li><li>sortBy: <code>closeBlockTime</code> <code>openBlockTime</code> <code>averagePrice</code> <code>size</code> <code>leverage</code> <code>durationInSecond</code> <code>orderCount</code> <code>roi</code> <code>realisedRoi</code> <code>pnl</code> <code>realisedPnl</code></li><li>sortType: <code>desc</code>, <code>asc</code></li><li><p>queries: array of</p><ul><li>fieldName: <code>account</code> <code>status</code></li><li><p>value:</p><ul><li>status: <code>CLOSE</code> <code>OPEN</code></li><li>account: EVM address</li></ul></li></ul></li></ul><p><br></p></td></tr><tr><td><strong>Example request</strong><br></td><td><pre class="language-JSON"><code class="lang-JSON">{"pagination":{"limit":20,"offset":0},"queries":[{"fieldName":"status","value":"CLOSE"},{"fieldName":"account","value":"0x9f431A46149bab70373B9C6867d2dB8C2F45aa11"}],"sortBy":"closeBlockTime","sortType":"desc"}
</code></pre></td></tr><tr><td><strong>Example response</strong><br></td><td><pre class="language-JSON"><code class="lang-JSON">{
    "data": [
        {
            "id": "656bd0e0d8fb813a7046c86a",
            "synthetixPositionId": "49170", // only Kwenta, Polynomial
            "reverseIndex": 0,// only Kwenta, Polynomial
            "account": "0x852610C4BD327C9c7fd93e06505173092f29a39c",
            "smartAccount": "0x375fa2B494208b0F4f3f5f0b85121844a929AE6C",  // only Kwenta, Polynomial
            "key": "0x375fa2B494208b0F4f3f5f0b85121844a929AE6C-0x2B3bb4c683BFc5239B029131EEf3B1d214478d93-LONG",
            "logId": 16,
            "openBlockNumber": 112982925,
            "openBlockTime": "2023-12-03T00:50:27.000Z",
            "closeBlockNumber": 113022125,
            "closeBlockTime": "2023-12-03T22:37:07.000Z",
            "indexToken": "0x2B3bb4c683BFc5239B029131EEf3B1d214478d93",
            "lastSizeNumber": 0, // only Kwenta, Polynomial
            "size": 150057.1415073778,
            "fee": 126.470238805,
            "lastCollateral": 12987.245139121, // only Kwenta, Polynomial
            "collateral": 9907.023471108,
            "averagePrice": 2165.370462136,
            "lastFunding": -202.30654613, // only Kwenta, Polynomial
            "funding": -158.90564217635142,
            "lastPriceNumber": 2212.595384719, // only Kwenta, Polynomial
            "pnl": 5958.737081751136,
            "realisedPnl": 6244.112962732488,
            "roi": 60.14659296133386,
            "realisedRoi": 63.02713404225081,
            "isLong": true,
            "isWin": true,
            "isLiquidate": false,
            "leverage": 15.146541435476728,
            "orderCount": 2,
            "orderIncreaseCount": 1,
            "orderDecreaseCount": 1,
            "durationInSecond": 78400,
            "status": "CLOSE",
            "createdAt": "2023-12-03T00:50:40.058Z",
            "protocol": "KWENTA"
        },
        ...
    ],
    "meta": {
        "limit": 20,
        "offset": 0,
        "total": 56,
        "totalPages": 3
    }
}
</code></pre></td></tr></tbody></table>

3. ## Get position details

<table data-header-hidden><thead><tr><th width="123"></th><th></th></tr></thead><tbody><tr><td><strong>URL</strong></td><td>https://api.copin.io/KWENTA/position/detail/:positionId</td></tr><tr><td><strong>Method</strong></td><td>GET</td></tr><tr><td><strong>Example response</strong><br></td><td><pre class="language-JSON"><code class="lang-JSON">{
    "id": "656444f14350fb0b69bd6402",
    "synthetixPositionId": "48503", // only Kwenta, Polynomial
    "reverseIndex": 0, // only Kwenta, Polynomial
    "account": "0x852610C4BD327C9c7fd93e06505173092f29a39c",
    "smartAccount": "0x375fa2B494208b0F4f3f5f0b85121844a929AE6C", // only Kwenta, Polynomial
    "key": "0x375fa2B494208b0F4f3f5f0b85121844a929AE6C-0x2B3bb4c683BFc5239B029131EEf3B1d214478d93-LONG",
    "logId": 11,
    "openBlockNumber": 112735639,
    "openBlockTime": "2023-11-27T07:27:35.000Z",
    "closeBlockNumber": 112797988,
    "closeBlockTime": "2023-11-28T18:05:53.000Z",
    "indexToken": "0x2B3bb4c683BFc5239B029131EEf3B1d214478d93",
    "lastSizeNumber": 0, // only Kwenta, Polynomial
    "size": 299791.2220018517,
    "fee": 228.62124740700003,
    "lastCollateral": 13993.076127358, // only Kwenta, Polynomial
    "collateral": 16215.501363168,
    "averagePrice": 2022.9018492877242,
    "lastFunding": -195.163117027, // only Kwenta, Polynomial
    "funding": -112.83324162360957,
    "lastPriceNumber": 2063.625026153, // only Kwenta, Polynomial
    "pnl": 3993.0761273536705,
    "realisedPnl": 4334.53061638428,
    "roi": 24.625054988577602,
    "realisedRoi": 26.730783830278366,
    "isLong": true,
    "isWin": true,
    "isLiquidate": false,
    "leverage": 18.487940353346062,
    "orderCount": 6,
    "orderIncreaseCount": 3,
    "orderDecreaseCount": 3,
    "durationInSecond": 124698,
    "status": "CLOSE",
    "createdAt": "2023-11-27T07:27:45.029Z",
    "protocol": "KWENTA",
    "orders": [
        {
            "id": "656444f1c6583cc67b6985b6",
            "synthetixPositionId": "48503", // only Kwenta, Polynomial
            "account": "0x852610C4BD327C9c7fd93e06505173092f29a39c",
            "smartAccount": "0x375fa2B494208b0F4f3f5f0b85121844a929AE6C", // only Kwenta, Polynomial
            "txHash": "0xb6c1d05806205893e33e2248fb67a7701931126777d3e706d91d7503dd83b34e",
            "logId": 11,
            "blockNumber": 112735639,
            "blockTime": "2023-11-27T07:27:35.000Z",
            "key": "0x375fa2B494208b0F4f3f5f0b85121844a929AE6C-0x2B3bb4c683BFc5239B029131EEf3B1d214478d93-LONG",
            "indexToken": "0x2B3bb4c683BFc5239B029131EEf3B1d214478d93",
            "sizeDeltaNumber": 149884.05160703347,
            "sizeNumber": 73.5244,
            "collateralDeltaNumber": 9967.858290134,
            "priceNumber": 2038.562050245,
            "fundingRateNumber": 0.000209485,
            "fundingNumber": -194.18719593,
            "leverage": 15.036735800646957,
            "isLong": true,
            "isOpen": true,
            "type": "OPEN",
            "createdAt": "2023-11-27T07:27:45.026Z"
        },
        {
            "id": "6564c9d5c6583cc67b6a0a38",
            "synthetixPositionId": "48503", // only Kwenta, Polynomial
            "account": "0x852610C4BD327C9c7fd93e06505173092f29a39c",
            "smartAccount": "0x375fa2B494208b0F4f3f5f0b85121844a929AE6C", // only Kwenta, Polynomial
            "txHash": "0x2a555f29a93ecb9a99c849f25ff798edc69fb099d04e6dd586cb46db35f91f00",
            "logId": 22,
            "blockNumber": 112752648,
            "blockTime": "2023-11-27T16:54:33.000Z",
            "key": "0x375fa2B494208b0F4f3f5f0b85121844a929AE6C-0x2B3bb4c683BFc5239B029131EEf3B1d214478d93-LONG",
            "indexToken": "0x2B3bb4c683BFc5239B029131EEf3B1d214478d93",
            "sizeDeltaNumber": 0,
            "sizeNumber": 0,
            "collateralDeltaNumber": 3218.916340476,
            "priceNumber": 0,
            "fundingRateNumber": 0,
            "fundingNumber": 0,
            "leverage": 0,
            "isLong": true,
            "isOpen": false,
            "type": "MARGIN_TRANSFERRED",
            "createdAt": "2023-11-27T16:54:45.331Z"
        },
        {
            "id": "6564c9dac6583cc67b6a0a43",
            "synthetixPositionId": "48503", // only Kwenta, Polynomial
            "account": "0x852610C4BD327C9c7fd93e06505173092f29a39c",
            "smartAccount": "0x375fa2B494208b0F4f3f5f0b85121844a929AE6C", // only Kwenta, Polynomial
            "txHash": "0xd1749c1b3319fe2ea0e3da6aa7ea9633bc265dd5c1a0ec9ec7bb0a591b690dfb",
            "logId": 12,
            "blockNumber": 112752650,
            "blockTime": "2023-11-27T16:54:37.000Z",
            "key": "0x375fa2B494208b0F4f3f5f0b85121844a929AE6C-0x2B3bb4c683BFc5239B029131EEf3B1d214478d93-LONG",
            "indexToken": "0x2B3bb4c683BFc5239B029131EEf3B1d214478d93",
            "sizeDeltaNumber": 74977.61596141392,
            "sizeNumber": 37.1775,
            "collateralDeltaNumber": 159.73717763400055,
            "priceNumber": 2016.747117515,
            "feeNumber": 49.943313331,
            "fundingRateNumber": 0,
            "fundingNumber": -194.181960095,
            "leverage": 16.72779681583392,
            "isLong": true,
            "isClose": false,
            "type": "INCREASE",
            "createdAt": "2023-11-27T16:54:50.322Z"
        },
        ...,
        {
            "id": "6565d90bc6583cc67b6b0131",
            "synthetixPositionId": "48503", // only Kwenta, Polynomial
            "account": "0x852610C4BD327C9c7fd93e06505173092f29a39c",
            "smartAccount": "0x375fa2B494208b0F4f3f5f0b85121844a929AE6C", // only Kwenta, Polynomial
            "txHash": "0xa4ca3a4a5467868b31412e4b2c1f49ec920a599f686c0f2d6142edde51b0bda7",
            "logId": 8,
            "blockNumber": 112787364,
            "blockTime": "2023-11-28T12:11:45.000Z",
            "key": "0x375fa2B494208b0F4f3f5f0b85121844a929AE6C-0x2B3bb4c683BFc5239B029131EEf3B1d214478d93-LONG",
            "indexToken": "0x2B3bb4c683BFc5239B029131EEf3B1d214478d93",
            "sizeDeltaNumber": 74898.679078195,
            "sizeNumber": 37,
            "collateralDeltaNumber": 3813.289160432001,
            "priceNumber": 2024.288623735,
            "feeNumber": 84.28932395400001,
            "fundingRateNumber": 0,
            "fundingNumber": -194.971449737,
            "leverage": 11.238724609457813,
            "isLong": true,
            "isClose": false,
            "type": "DECREASE",
            "createdAt": "2023-11-28T12:11:55.022Z"
        },
        ...,
        {
            "id": "65662c12c6583cc67b6b55d1",
            "synthetixPositionId": "48503", // only Kwenta, Polynomial
            "account": "0x852610C4BD327C9c7fd93e06505173092f29a39c",
            "smartAccount": "0x375fa2B494208b0F4f3f5f0b85121844a929AE6C", // only Kwenta, Polynomial
            "txHash": "0x267f696c7e751ea6e39eeb576988f069f9535714331117954fb9c61838d637b6",
            "logId": 12,
            "blockNumber": 112797988,
            "blockTime": "2023-11-28T18:05:53.000Z",
            "key": "0x375fa2B494208b0F4f3f5f0b85121844a929AE6C-0x2B3bb4c683BFc5239B029131EEf3B1d214478d93-LONG",
            "indexToken": "0x2B3bb4c683BFc5239B029131EEf3B1d214478d93",
            "sizeDeltaNumber": 153118.087865516,
            "sizeNumber": 74.1986,
            "collateralDeltaNumber": 363.81130071199914,
            "priceNumber": 2063.625026153,
            "feeNumber": 228.62124740700003,
            "fundingRateNumber": 0,
            "fundingNumber": -195.163117027,
            "leverage": 18.487940353346062,
            "isLong": true,
            "isClose": true,
            "type": "CLOSE",
            "createdAt": "2023-11-28T18:06:10.036Z"
        }
    ]
}
</code></pre></td></tr></tbody></table>

4. ## Leaderboards

<table data-header-hidden><thead><tr><th width="125"></th><th></th></tr></thead><tbody><tr><td><strong>URL</strong></td><td>https://api.copin.io/leaderboards/page</td></tr><tr><td><strong>Method</strong></td><td>GET</td></tr><tr><td><strong>Query</strong></td><td><ul><li>protocol: <code>KWENTA</code> <code>GMX</code></li><li>queryDate: Date in timestamp</li><li>statisticType: <code>MONTH</code> <code>WEEK</code></li><li>limit: number of records</li><li>offset: number of skipped records</li><li>sort_by: <code>ranking</code> <code>totalPnl</code> <code>totalRealisedPnl</code> <code>totalVolume</code> <code>totalFee</code> <code>totalTrade</code> <code>totalWin</code> <code>totalLose</code> <code>totalLiquidation</code> <code>totalLiquidationAmount</code></li><li>sort_type: <code>asc</code> <code>desc</code></li></ul></td></tr><tr><td><strong>Example query</strong></td><td>https://api.copin.io/leaderboards/page?protocol=KWENTA&#x26;queryDate=1701835880676&#x26;statisticType=MONTH&#x26;limit=20&#x26;offset=0&#x26;sort_by=ranking&#x26;sort_type=asc</td></tr><tr><td><strong>Example response</strong><br></td><td><pre class="language-JSON"><code class="lang-JSON">{
    "data": [
        {
            "id": "656fb9897fdc207f19e4ef1f",
            "account": "0x92812499fF2c040f93121Aab684680a6e603C4A7",
            "protocol": "KWENTA",
            "statisticType": "MONTH",
            "rankingAt": "2023-12-06T00:00:08.841Z",
            "ranking": 1,
            "lastRanking": 1,
            "totalPnl": 2124229.3913290403,
            "totalRealisedPnl": 2137944.463823661,
            "totalVolume": 11012185.066084206,
            "totalFee": 13715.072494621,
            "totalTrade": 1,
            "totalWin": 1,
            "totalLose": 0,
            "totalLiquidation": 0,
            "totalLiquidationAmount": 0,
            "createdAt": "2023-12-06T00:00:09.748Z"
        },
        ...
    ],
     "meta": {
        "limit": 20,
        "offset": 0,
        "total": 728,
        "totalPages": 37
    }
}
</code></pre></td></tr></tbody></table>

\
