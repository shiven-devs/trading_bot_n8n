# Trading Bot (n8n)

An automated trading bot built with [n8n](https://n8n.io), a workflow automation tool. It pulls market data, checks it against trading rules, and sends alerts or places trades.

> ⚠️ **Disclaimer:** This project is for learning and experimentation only. It is not financial advice. Trading carries real risk, so test with paper trading before using real money.

## Features (planned)

- 📈 Fetch market prices from an exchange or data API
- 🧮 Apply trading strategy rules (e.g. moving averages, RSI)
- 🔔 Send trade signals and alerts (Telegram, Discord, email)
- 🤖 Place orders automatically through an exchange API
- 📝 Log trades and results for review

## Tech Stack

- **n8n**: workflow automation
- **Exchange / market data API**: e.g. Binance, Alpaca, or similar
- **Notifications**: Telegram / Discord / email

## Getting Started

### Prerequisites

- [Node.js](https://nodejs.org) 18+ or [Docker](https://www.docker.com)
- An exchange/broker account with API keys (use paper trading/testnet first)

### Run n8n

With npx:

```bash
npx n8n
```

Or with Docker:

```bash
docker run -it --rm -p 5678:5678 -v n8n_data:/home/node/.n8n docker.n8n.io/n8nio/n8n
```

Then open http://localhost:5678.

### Import the workflow

1. In n8n, go to **Workflows → Import from File**.
2. Select the workflow `.json` file from this repo.
3. Add your API credentials in n8n's **Credentials** section.
4. Activate the workflow.

## Security

- Never commit API keys or secrets to this repo.
- Store credentials in n8n's credential manager or in environment variables.
- Restrict exchange API keys (e.g. disable withdrawals, whitelist IPs).

## Roadmap

- [ ] Basic price-fetch workflow
- [ ] First strategy (moving average crossover)
- [ ] Alert notifications
- [ ] Paper trading integration
- [ ] Backtesting and performance logging

## License

TBD
