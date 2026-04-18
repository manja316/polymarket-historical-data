# Polymarket Historical Prices Dataset

**9,550 markets | 8.9M data points | $11.7B total volume**

The largest publicly available Polymarket prediction market dataset. 30 days of 15-minute price snapshots across politics, sports, crypto, geopolitics, economics, and more.

> **Full dataset (8.1M prices + 792K orderbooks) available on [Gumroad →](https://manja8.gumroad.com/l/polymarket-data)**

## What's Included (free)

### markets.csv (9,550 rows)
Every tracked Polymarket market with metadata.

| Column | Description |
|--------|-------------|
| `market_id` | Unique market identifier |
| `question` | The market question |
| `category` | politics, sports, crypto, geopolitics, economics, etc. |
| `volume` | Total lifetime trading volume (USD) |
| `volume_24h` | 24-hour trading volume |
| `liquidity` | Current order book liquidity |
| `end_date` | Market resolution date |
| `best_bid` / `best_ask` / `spread` | Order book pricing |
| `last_trade_price` | Last traded price |
| `one_day_change` | 24h price change |
| `active` | Whether market is still active |

### prices_sample.csv (100,000 rows)
Latest 100K price snapshots — preview of the full 8.1M dataset.

| Column | Description |
|--------|-------------|
| `market_id` | Links to markets.csv |
| `outcome` | "Yes" or "No" |
| `price` | 0.00 to 1.00 (implied probability) |
| `timestamp` | ISO 8601 UTC timestamp |

## Category Breakdown

| Category | Markets | Volume |
|----------|---------|--------|
| AI/LLM & Other | 5,326 | $3.3B |
| Politics | 868 | $3.7B |
| Sports | 1,291 | $2.3B |
| Geopolitics | 388 | $919M |
| Crypto | 1,356 | $579M |
| Economics | 134 | $715M |
| Science/Tech | 157 | $117M |

## Full Dataset (paid)

The free sample includes market metadata + 100K price previews.

**[Get the full dataset on Gumroad →](https://manja8.gumroad.com/l/polymarket-data)**

| Tier | Price | What You Get | Link |
|------|-------|-------------|------|
| Sample | $1 | markets.csv + 100K prices | [Gumroad](https://manja8.gumroad.com/l/polymarket-data) |
| **Full** | **$9** | **8.1M prices + 792K orderbooks (SQLite)** | **[Buy Now](https://checkout.dodopayments.com/buy/pdt_0NcwYHQb6UoiZb41mnshx)** |
| **Subscription** | **$29/mo** | **Weekly updates + new markets** | **[Subscribe](https://checkout.dodopayments.com/buy/pdt_0NcwYR0akzPEQoh1leSk9)** |

The full dataset includes:
- **8,158,672 price snapshots** at 15-minute intervals
- **792,527 orderbook depth snapshots** (top 10 levels, top 200 markets)
- **SQLite database** ready for pandas, DuckDB, or Polars
- 30 days of continuous data (March 18 — April 17, 2026)

## Use Cases

- **Backtest trading strategies** — our crash recovery strategy shows 75% WR on 6,225 simulated trades
- **Mean reversion analysis** — after a >20% drop, average return is +6.6% within 15 minutes
- **Spread dynamics** — study bid/ask behavior across categories
- **ML training data** — predict outcome probabilities from price patterns
- **Research** — information aggregation efficiency in prediction markets

## Data Pipeline

Data collected every 15 minutes by an automated pipeline:
- Gamma API → market metadata + prices
- CLOB API → orderbook depth for top markets
- SQLite storage → optimized for analytical queries

## Contact

- Email: LuciferForge@proton.me
- Website: [protodex.io](https://protodex.io)
- GitHub: [@manja316](https://github.com/manja316)

## License

CC-BY-4.0. Free to use with attribution.

---
*Updated: April 17, 2026. Data refreshes weekly.*
