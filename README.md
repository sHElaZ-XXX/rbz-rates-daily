# RBZ Exchange Rates API (Developer Documentation)

## Overview
This Laravel package provides access to Zimbabwe's Reserve Bank (RBZ) daily exchange rates by scraping data from their PDF reports.

## Features
- Fetch USD rates specifically
- Fetch all available currency rates
- Automatic PDF parsing and data extraction
- Error handling for missing/invalid data

## Installation
1. Install via Composer:
```bash

 composer require smalot/pdfparser


### Get USD Rate
```bash
curl https://your-api.com/api/rbz-usd-rate

### Example output
{
  "currency": "USD",
  "indices": "",
  "bid": "1",
  "ask": "1",
  "mid_rate": "1.0000",
  "bid_zwg": "26.2721",
  "ask_zwg": "27.6193",
  "mid_rate_zwg": "26.9457",
  "source_url": "https://www.rbz.co.zw/documents/Exchange_Rates/2025/June/RATES_30_JUNE_2025.pdf"
}
### Get All Currency Rates
```bash
curl https://your-api.com/api/rbz-all-rate

### Example output
{
  "date": "2025-06-30",
  "rates": [
    {
      "currency": "USD",
      "indices": "",
      "bid": "1",
      "ask": "1",
      "mid_rate": "1.0000",
      "bid_zwg": "26.2721",
      "ask_zwg": "27.6193",
      "mid_rate_zwg": "26.9457"
    },
    {
      "currency": "ZAR",
      "indices": "",
      "bid": "17.7422",
      "ask": "17.7537",
      "mid_rate": "17.74795",
      "bid_zwg": "0.6423",
      "ask_zwg": "0.6757",
      "mid_rate_zwg": "0.6590"
    },
    {
      "currency": "GBP",
      "indices": "*",
      "bid": "1.3736",
      "ask": "1.3740",
      "mid_rate": "1.37380",
      "bid_zwg": "36.0873",
      "ask_zwg": "37.9489",
      "mid_rate_zwg": "37.0181"
    },
    {
      "currency": "JPY",
      "indices": "",
      "bid": "143.8400",
      "ask": "143.8500",
      "mid_rate": "143.84500",
      "bid_zwg": "5.2079",
      "ask_zwg": "5.4753",
      "mid_rate_zwg": "5.3416"
    },
    {
      "currency": "ZMW/ZMK",
      "indices": "",
      "bid": "23.6979",
      "ask": "23.7479",
      "mid_rate": "23.72290",
      "bid_zwg": "0.8580",
      "ask_zwg": "0.9039",
      "mid_rate_zwg": "0.8810"
    },
    {
      "currency": "BWP",
      "indices": "",
      "bid": "0.0746",
      "ask": "0.0751",
      "mid_rate": "0.07485",
      "bid_zwg": "1.9598",
      "ask_zwg": "2.0742",
      "mid_rate_zwg": "2.0170"
    },
    {
      "currency": "CHF",
      "indices": "",
      "bid": "0.7973",
      "ask": "0.7978",
      "mid_rate": "0.79755",
      "bid_zwg": "20.9467",
      "ask_zwg": "22.0346",
      "mid_rate_zwg": "21.4907"
    },
    {
      "currency": "MWK",
      "indices": "",
      "bid": "1716.6600",
      "ask": "1751.0000",
      "mid_rate": "1,733.83000",
      "bid_zwg": "62.1543",
      "ask_zwg": "66.6486",
      "mid_rate_zwg": "64.4015"
    },
    {
      "currency": "AUD",
      "indices": "*",
      "bid": "0.6551",
      "ask": "0.6552",
      "mid_rate": "0.65515",
      "bid_zwg": "17.2108",
      "ask_zwg": "18.0961",
      "mid_rate_zwg": "17.6535"
    },
    {
      "currency": "SDR",
      "indices": "*",
      "bid": "1.373380",
      "ask": "1.373380",
      "mid_rate": "1.37338",
      "bid_zwg": "37.0066",
      "ask_zwg": "37.0066",
      "mid_rate_zwg": "37.0066"
    },
    {
      "currency": "MZN/MET",
      "indices": "",
      "bid": "63.2500",
      "ask": "64.5200",
      "mid_rate": "63.88500",
      "bid_zwg": "2.2900",
      "ask_zwg": "2.4558",
      "mid_rate_zwg": "2.3729"
    },
    {
      "currency": "NOK",
      "indices": "",
      "bid": "10.0419",
      "ask": "10.0475",
      "mid_rate": "10.04470",
      "bid_zwg": "0.3635",
      "ask_zwg": "0.3824",
      "mid_rate_zwg": "0.3730"
    },
    {
      "currency": "SEK",
      "indices": "",
      "bid": "9.4594",
      "ask": "9.4628",
      "mid_rate": "9.46110",
      "bid_zwg": "0.3424",
      "ask_zwg": "0.3601",
      "mid_rate_zwg": "0.3513"
    },
    {
      "currency": "CAD",
      "indices": "*",
      "bid": "1.3662",
      "ask": "1.3666",
      "mid_rate": "1.36640",
      "bid_zwg": "0.0494",
      "ask_zwg": "0.0520",
      "mid_rate_zwg": "0.0507"
    },
    {
      "currency": "EUR",
      "indices": "*",
      "bid": "1.1735",
      "ask": "1.1736",
      "mid_rate": "1.17355",
      "bid_zwg": "30.8303",
      "ask_zwg": "32.4140",
      "mid_rate_zwg": "31.6222"
    },
    {
      "currency": "CNY",
      "indices": "",
      "bid": "7.1635",
      "ask": "7.1637",
      "mid_rate": "7.16360",
      "bid_zwg": "0.2593",
      "ask_zwg": "0.2726",
      "mid_rate_zwg": "0.2660"
    },
    {
      "currency": "INR",
      "indices": "",
      "bid": "85.5100",
      "ask": "85.5200",
      "mid_rate": "85.51500",
      "bid_zwg": "3.0960",
      "ask_zwg": "3.2551",
      "mid_rate_zwg": "3.1756"
    },
    {
      "currency": "NZD",
      "indices": "*",
      "bid": "0.6083",
      "ask": "0.6087",
      "mid_rate": "0.60850",
      "bid_zwg": "15.9813",
      "ask_zwg": "16.8118",
      "mid_rate_zwg": "16.3966"
    },
    {
      "currency": "DKK",
      "indices": "",
      "bid": "6.3574",
      "ask": "6.3578",
      "mid_rate": "6.35760",
      "bid_zwg": "0.2301",
      "ask_zwg": "0.2419",
      "mid_rate_zwg": "0.2360"
    },
    {
      "currency": "XAU",
      "indices": "",
      "bid": "3288.0454",
      "ask": "3288.7646",
      "mid_rate": "3,288.40500",
      "bid_zwg": "86383.8575",
      "ask_zwg": "90833.3761",
      "mid_rate_zwg": "88608.6168"
    },
    {
      "currency": "AFN",
      "indices": "",
      "bid": "70.1300",
      "ask": "70.3300",
      "mid_rate": "70.23000",
      "bid_zwg": "2.5391",
      "ask_zwg": "2.6769",
      "mid_rate_zwg": "2.6080"
    },
    {
      "currency": "THB",
      "indices": "",
      "bid": "32.5000",
      "ask": "32.5300",
      "mid_rate": "32.51500",
      "bid_zwg": "1.1767",
      "ask_zwg": "1.2381",
      "mid_rate_zwg": "1.2074"
    },
    {
      "currency": "ETB",
      "indices": "",
      "bid": "134.6800",
      "ask": "139.6800",
      "mid_rate": "137.18000",
      "bid_zwg": "4.8763",
      "ask_zwg": "5.3166",
      "mid_rate_zwg": "5.0965"
    },
    {
      "currency": "SZL",
      "indices": "",
      "bid": "17.7510",
      "ask": "17.7539",
      "mid_rate": "17.75245",
      "bid_zwg": "0.6427",
      "ask_zwg": "0.6757",
      "mid_rate_zwg": "0.6592"
    },
    {
      "currency": "MUR",
      "indices": "",
      "bid": "44.9200",
      "ask": "45.2200",
      "mid_rate": "45.07000",
      "bid_zwg": "1.6263",
      "ask_zwg": "1.7212",
      "mid_rate_zwg": "1.6738"
    },
    {
      "currency": "MYR",
      "indices": "",
      "bid": "4.2140",
      "ask": "4.2180",
      "mid_rate": "4.21600",
      "bid_zwg": "0.1525",
      "ask_zwg": "0.1605",
      "mid_rate_zwg": "0.1565"
    },
    {
      "currency": "LSL",
      "indices": "",
      "bid": "17.7510",
      "ask": "17.7539",
      "mid_rate": "17.75245",
      "bid_zwg": "0.6427",
      "ask_zwg": "0.6757",
      "mid_rate_zwg": "0.6592"
    },
    {
      "currency": "CYP",
      "indices": "*",
      "bid": "0.3975",
      "ask": "0.3980",
      "mid_rate": "0.39775",
      "bid_zwg": "0.0143",
      "ask_zwg": "0.0151",
      "mid_rate_zwg": "0.0147"
    },
    {
      "currency": "EGP",
      "indices": "",
      "bid": "49.6500",
      "ask": "49.7500",
      "mid_rate": "49.70000",
      "bid_zwg": "1.7976",
      "ask_zwg": "1.8936",
      "mid_rate_zwg": "1.8456"
    },
    {
      "currency": "BRL",
      "indices": "",
      "bid": "5.4777",
      "ask": "5.4787",
      "mid_rate": "5.47820",
      "bid_zwg": "0.1983",
      "ask_zwg": "0.2085",
      "mid_rate_zwg": "0.2034"
    },
    {
      "currency": "TZS",
      "indices": "",
      "bid": "2620.0000",
      "ask": "2680.0000",
      "mid_rate": "2,650.00000",
      "bid_zwg": "94.8612",
      "ask_zwg": "102.0093",
      "mid_rate_zwg": "98.4353"
    },
    {
      "currency": "RUB",
      "indices": "",
      "bid": "78.6000",
      "ask": "78.6200",
      "mid_rate": "78.61000",
      "bid_zwg": "2.8458",
      "ask_zwg": "2.9925",
      "mid_rate_zwg": "2.9192"
    },
    {
      "currency": "KES",
      "indices": "",
      "bid": "129.0000",
      "ask": "129.5000",
      "mid_rate": "129.25000",
      "bid_zwg": "4.6706",
      "ask_zwg": "4.9291",
      "mid_rate_zwg": "4.7999"
    },
    {
      "currency": "DEM",
      "indices": "",
      "bid": "2.2150",
      "ask": "2.2175",
      "mid_rate": "2.21625",
      "bid_zwg": "0.0801",
      "ask_zwg": "0.0844",
      "mid_rate_zwg": "0.0823"
    },
    {
      "currency": "ESP",
      "indices": "",
      "bid": "188.4300",
      "ask": "188.6500",
      "mid_rate": "188.54000",
      "bid_zwg": "6.8224",
      "ask_zwg": "7.1806",
      "mid_rate_zwg": "7.0015"
    },
    {
      "currency": "ITL",
      "indices": "",
      "bid": "2192.8300",
      "ask": "2195.3200",
      "mid_rate": "2,194.07500",
      "bid_zwg": "79.3948",
      "ask_zwg": "83.5608",
      "mid_rate_zwg": "81.4778"
    },
    {
      "currency": "FRF",
      "indices": "",
      "bid": "7.4287",
      "ask": "7.4372",
      "mid_rate": "7.43295",
      "bid_zwg": "0.2689",
      "ask_zwg": "0.2830",
      "mid_rate_zwg": "0.2760"
    },
    {
      "currency": "HKD",
      "indices": "",
      "bid": "7.7495",
      "ask": "7.8498",
      "mid_rate": "7.79965",
      "bid_zwg": "0.2805",
      "ask_zwg": "0.2987",
      "mid_rate_zwg": "0.2896"
    },
    {
      "currency": "ARS",
      "indices": "",
      "bid": "1187.5000",
      "ask": "1189.0000",
      "mid_rate": "1,188.25000",
      "bid_zwg": "42.9952",
      "ask_zwg": "45.2571",
      "mid_rate_zwg": "44.1262"
    },
    {
      "currency": "XAF",
      "indices": "",
      "bid": "559.6900",
      "ask": "565.5500",
      "mid_rate": "562.62000",
      "bid_zwg": "20.2644",
      "ask_zwg": "21.5266",
      "mid_rate_zwg": "20.8955"
    }
  ],
  "source_url": "https://www.rbz.co.zw/documents/Exchange_Rates/2025/June/RATES_30_JUNE_2025.pdf"
}
