# binanceusr

### Work in progress ###
This code is based on https://github.com/daroczig/binancer package
Use it at your own risk
### TODO
Change `binance.com` with `binance.us`

An R client to some Cryptocurrency exchanges:

* Binance US API docs: https://github.com/binance-us/binance-official-api-docs/blob/master/rest-api.md
* Huobi API docs: https://github.com/huobiapi/API_Docs_en/wiki

Example on getting data from Binance on the most recent Bitcoin/USDT changes:

```r
library(binancer)
binance_klines('BTCUSDT', interval = '1m')
```

Extend this to multiple pairs:

```r
rbindlist(lapply(c("ETHBTC", "LTCBTC"), binance_klines, interval = "1d", limit = 200))
```

Same on Huobi:

```r
huobi_klines('btcusdt')
```
