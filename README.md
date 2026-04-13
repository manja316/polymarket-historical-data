# Polymarket Historical Prices Dataset

**8,701 markets | 7.17M price records | $10.8B total volume**

The largest publicly available dataset of Polymarket prediction market data. Covers politics, sports, crypto, geopolitics, science/tech, economics, weather, and entertainment markets.

## What's Included

### markets.csv (8,701 rows)
Market metadata for every tracked Polymarket market.

| Column | Description |
|--------|-------------|
| `id` | Unique market identifier (CLOB token) |
| `question` | The market question (e.g., "Will Bitcoin hit $100K by June 2026?") |
| `category` | Market category (politics, crypto, sports, etc.) |
| `tags` | Comma-separated tags |
| `slug` | URL slug on polymarket.com |
| `volume` | Total lifetime trading volume (USD) |
| `volume_24h` | 24-hour trading volume |
| `liquidity` | Current order book liquidity |
| `end_date` | Market resolution date |
| `created_date` | Market creation date |
| `outcomes` | Possible outcomes (e.g., "Yes, No") |
| `outcome_prices` | Current prices per outcome |
| `best_bid` / `best_ask` / `spread` | Order book data |
| `last_trade_price` | Last traded price |
| `active` | Whether market is still active |
| `resolved` | Whether market has resolved |
| `resolved_outcome` | Resolution result if resolved |

### prices_sample.csv (100K rows)
Sample of the full 7.17M price history records. Most recent 100K records.

| Column | Description |
|--------|-------------|
| `market_id` | Links to markets.csv `id` |
| `outcome` | Which outcome this price is for |
| `price` | Price (0.00 to 1.00, representing probability) |
| `ts` | Timestamp (ISO 8601 UTC) |

## Dataset Statistics

| Metric | Value |
|--------|-------|
| Total Markets | 8,701 |
| Total Price Records | 7,170,986 |
| Total Volume Traded | $10.8 Billion |
| Date Range (markets) | Mar 2025 - Apr 2026 |
| Date Range (prices) | Mar 2026 - Apr 2026 |
| Categories | 10 (politics, crypto, sports, geopolitics, etc.) |

### Category Breakdown

| Category | Markets |
|----------|---------|
| Other | 4,657 |
| Crypto | 1,217 |
| Sports | 1,162 |
| Politics | 821 |
| Geopolitics | 374 |
| Science & Tech | 153 |
| Economics | 125 |
| Weather | 112 |
| Entertainment | 78 |

## Full Dataset

This repository contains a **sample** (100K price records). The full dataset includes:
- All 7.17M price records
- Raw SQLite database (2.2GB) for easy querying
- Additional tables: orderbooks, market snapshots, market features

**Get the full dataset:** [Polymarket Historical Data on Gumroad](https://manja316.gumroad.com/)

## Use Cases

- **Backtesting** prediction market trading strategies
- **Academic research** on information aggregation and forecasting
- **Analytics dashboards** for prediction market performance
- **Machine learning** models for price prediction
- **Event study analysis** on how markets react to news
- **Calibration research** comparing market probabilities to outcomes

## Data Format

- All files are UTF-8 encoded CSV with headers
- Timestamps are ISO 8601 format in UTC
- Prices are decimal values between 0.00 and 1.00
- Volume and liquidity are in USD

## Updates

This dataset is updated weekly. Star/watch this repo for notifications.

## License

CC0 1.0 Universal - Public Domain. Use for any purpose.

## Citation

```
@dataset{polymarket_historical_2026,
  title={Polymarket Historical Prices Dataset},
  author={manja316},
  year={2026},
  url={https://github.com/manja316/polymarket-historical-data}
}
```
