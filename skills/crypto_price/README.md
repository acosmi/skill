---
name: crypto-price
description: Get cryptocurrency token price and generate candlestick charts via CoinGecko API or Hyperliquid API. Use when user asks for token price, crypto price, price chart, or cryptocurrency market data.
metadata: {"clawdbot":{"emoji":"📈","requires":{"bins":["python3"]}}}
---

# Crypto Price & Chart

Get cryptocurrency token price and generate candlestick charts.

## Usage

Execute the script with token symbol and optional duration:

```bash
python3 {baseDir}/scripts/get_price_chart.py <SYMBOL> [duration]
```

**Examples:**
- `python3 {baseDir}/scripts/get_price_chart.py HYPE`
- `python3 {baseDir}/scripts/get_price_chart.py HYPE 12h`
- `python3 {baseDir}/scripts/get_price_chart.py BTC 3h`
- `python3 {baseDir}/scripts/get_price_chart.py ETH 30m`
- `python3 {baseDir}/scripts/get_price_chart.py SOL 2d`

**Duration format:** `30m`, `3h`, `12h`, `24h` (default), `2d`

## Output

Returns JSON with:
- `price` - Current price in USD/USDT
- `change_period_percent` - P
