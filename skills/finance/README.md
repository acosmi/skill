---
name: finance
description: Track stocks, ETFs, indices, crypto (where available), and FX pairs with caching + provider fallbacks.
metadata: {"clawdbot":{"config":{"requiredEnv":["TWELVEDATA_API_KEY","ALPHAVANTAGE_API_KEY"],"stateDirs":[".cache/finance"],"example":"# Optional (only if you add a paid provider later)\n# export TWELVEDATA_API_KEY=\"...\"\n# export ALPHAVANTAGE_API_KEY=\"...\"\n"}}}
---

# Market Tracker Skill

This skill helps you fetch **latest quotes** and **historical series** for:
- Stocks / ETFs / Indices (e.g., AAPL, MSFT, ^GSPC, VOO)
- FX pairs (e.g., USD/ZAR, EURUSD, GBP-JPY)
- Crypto tickers supported by the chosen provider (best-effort)

It is optimized for:
- fast “what’s the price now?” queries
- lightweight tracking with a local watchlist
- caching to avoid rate-limits

## When to use
Use this skill when the user asks:
- “What’s the latest price of ___?”
- “Track ___ and ___ and show me daily changes.”
- “Give me a 30-day series for ___.”
- “Convert USD to
