
<h1 align="center">
	<img width="400" src="https://cdn-images-1.medium.com/max/1024/1*TY0eUcLT6us5Jz1VT1Tymg.jpeg" alt="Cryptocurrencies">
	<br>
	<br>
</h1>

[![contributions welcome](https://img.shields.io/badge/contributions-welcome-brightgreen.svg?style=flat)](https://github.com/ZoranPandovski/pycoincap/issues)
[![License](https://img.shields.io/badge/license-MIT%20License-brightgreen.svg)](https://opensource.org/licenses/MIT)
[![Build Status](https://travis-ci.org/ZoranPandovski/pycoincap.svg?branch=master)](https://github.com/ZoranPandovski/pycoincap)
[![Coverage Status](https://coveralls.io/repos/github/ZoranPandovski/pycoincap/badge.svg?branch=master)](https://coveralls.io/github/ZoranPandovski/pycoincap?branch=master)

# Pycoincap
Python module for getting data from Coinmarketcap, cryptocurrencies market cap, rankings, price, supply, circulating supply and other useful informations.



# Run tests
```
 python -m unittests pycoincap.tests.test_core
```

## Installation:

From source use
```
   git clone https://github.com/ZoranPandovski/pycoincap
   cd pycoincap
   python setup.py
   pip install -r requirements.txt
```

## Examples:
Retrieve informations from https://coinmarketcap.com/

Get coin informations
```python
from pycoincap import CryptoMarket as market

# Load data data from coinmarketcap
m = market()

# Returns coin object
BTC = m.coin('bitcoin')

print BTC
>>> Coin: Bitcoin
Ranked: 1
Price : 8334.59 $
Price BTC: 1.0
Circulating supply: 16856825.0
Total supply: 16856825.0
Percent changes:1h  = -1.68
                24h = -3.19
                7d  = -9.29

print BTC.price_usd
>>> 8334.59
```

Get stats
```python
from pycoincap import CryptoMarket as market

# Load data data from coinmarketcap
m = market()

#Returns stats
stats = m.stats()

print stats
>>>  Market value: 4.06888588391e+11$
 Bitcoin percentage: 34.53
 Active markets: 8716
 Active assets: 598
 Active currencies: 893
 Last day changes: 25323934215.0
```
