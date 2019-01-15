# API Reference

***Host***
```http
https://bione.cc
```

### 1. Market list

**HTTP Request**

```http
    # Request
    GET /api/v2/markets
```
```json
    # Response
    {
      "code": 1,
      "data": [
        {
          "market": "bat_usdt",
          "coin_pre": "bat",
          "coin_suf": "usdt",
          "vol": "353.69584800",
          "change": "1.16000000"
        },
        {
          "market": "bcc_usdt",
          "coin_pre": "bcc",
          "coin_suf": "usdt",
          "vol": "12.00000000",
          "change": "-6.89000000"
        }
      ]
    }

```

**Response Details**

| Field | Descirption |
| ----------|:-------:|
| market        | market symbol |
| coin_pre   | coin pre |
| coin_suf  | coin suf |
| vol   | volume |
| change   | increase |


### 2. Market depth

**HTTP Request**

```http
    # Request
    GET /api/v2/depth/market/<coin_pair>
```
```json
    # Response
    {
      "code": 1,
      "data": {
        "asks": [
          [
            "3982.52000000",
            "0.41599400"
          ],
          [
            "3982.74000000",
            "0.37913500"
          ]
        ],
        "bids": [
          [
            "3967.37000000",
            "0.39190100"
          ],
          [
            "3967.24000000",
            "0.02511000"
          ]
        ],
        "currentPrice": "3967.38000000"
      }
    }
```
**Response Details**  

| Field | Descirption |
| ----------|:-------:|
| asks        | depth of sellers |
| bids   | depth of buyers |
| currentPrice  | latest price |

**Request Paramters**

| Name | Type  | Requited | Description |
| ------------- |-----|-----|-----|
| coin_pair | String | Y | Coin Pair, e.g. ltc_btc |

### 3. Tickers

**HTTP Request**

```http
    # Request
    GET /api/v2/tickers
```

```javascript
    # Response
    {
      "code": 1,
      "data": [
        {
          "symbol": "bat_usdt",
          "high": "0.14390000",
          "low": "0.13100000",
          "last": "0.13930000",
          "vol": "353.33036100",
          "change": "1.16000000"
        },
        {
          "symbol": "bcc_usdt",
          "high": "622.46000000",
          "low": "622.46000000",
          "last": "622.46000000",
          "vol": "12.00000000",
          "change": "-6.89000000"
        }
      ]
    }

```

**Response Details**

|Field|Description|
|--------| :-------: |
| symbol | market symbol |
| high | highest price |
| low | lowest price |
| last | latest price |
| vol | volume |
| change | increase |
