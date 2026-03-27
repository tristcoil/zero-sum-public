<p align="center">
  <strong>θΣ×</strong>
</p>

<h1 align="center">The Zero Sum Times</h1>

<p align="center">
  A comprehensive, Wall Street Journal-inspired stock market analysis platform.<br/>
  Real-time quotes, interactive charting, fundamental analysis, sector correlations, and more — all in one place.
</p>

<p align="center">
  <a href="https://zero-sum-times.com"><img src="https://img.shields.io/badge/🌐_Live_Site-zero--sum--times.com-8B6914?style=for-the-badge" alt="Live Site" /></a>
</p>

<p align="center">
  <a href="https://github.com/tristcoil/zero-sum-public"><img src="https://img.shields.io/badge/GitHub-Source_Code-181717?style=for-the-badge&logo=github&logoColor=white" alt="GitHub" /></a>
  &nbsp;
  <a href="https://discord.gg/a89Ua6CQj"><img src="https://img.shields.io/badge/Discord-Join_Community-5865F2?style=for-the-badge&logo=discord&logoColor=white" alt="Discord" /></a>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Next.js-16-black?logo=next.js" alt="Next.js" />
  <img src="https://img.shields.io/badge/React-19-61dafb?logo=react" alt="React" />
  <img src="https://img.shields.io/badge/Flask-3-green?logo=flask" alt="Flask" />
  <img src="https://img.shields.io/badge/Python-3.12-blue?logo=python" alt="Python" />
  <img src="https://img.shields.io/badge/License-MIT-yellow" alt="MIT License" />
</p>

---

## Fundamental Analysis

Dive deep into any stock with a full-page breakdown: price history with moving averages, company profile, cash & debt overview, balance sheet visualizations (assets vs. liabilities vs. equity), ratings snapshot radar, and cash vs. debt trends. Key metrics — market cap, P/E, P/S, beta, dividend yield, 52-week range, and average volume — are displayed at a glance.

![Fundamental Analysis](img/fundamental_analysis.png)

---

## Landing Page & Market Dashboard

The home page provides a real-time market overview: major indices (S&P 500, Dow Jones, NASDAQ, Russell 2000, VIX), crypto & commodity tickers (Bitcoin, Ethereum, Gold, Crude Oil, 10Y Treasury), a color-coded sector performance heatmap, top market movers (gainers, losers, most active), curated market news, and an upcoming earnings calendar. A scrolling ticker bar with stock & crypto quotes rounds it off, along with random finance formulas and Wall Street quotes.

![Landing Page](img/landing_page.png)

---

## Advanced Charting Terminal

A professional-grade charting terminal with TradingView-powered interactive charts, multiple timeframes (intraday to 5Y), and extensive customization. Toggle chart types (Heikin Ashi, candlestick), overlays (Bollinger Bands, EMA, Ichimoku, VWAP, Fibonacci, SAR), structure tools (trendlines, ranges, volume profile, FVG), and studies (RSI, MACD, Stochastic, OBV, ADX/DMI, Williams %R, CCI). Includes drawing tools, chart presets (swing, trend, mean reversion), data export, replay mode, and a live watchlist sidebar with sector tabs.

![Advanced Charting](img/advanced_charting.png)

---

## Technical Analysis & Setup Detection

Automated technical analysis with an AI-generated scoring dashboard. Provides a composite BUY/SELL score, indicator scorecard (RSI, MACD, Bollinger %B, Stochastic, EMA), key price levels (stop-loss, SAR trailing stop, SMA, Fibonacci retracements, support/resistance), and contextual commentary on trend direction, momentum, and volatility. Compare performance vs. SPY and QQQ benchmarks at a glance.

![Technical Analysis](img/technical_analysis.png)

---

## Market Heatmap

An interactive treemap visualization of 500+ stocks, sized by market cap and colored by daily performance. Filter by S&P 500 or NASDAQ-100, switch between time periods (1D, 1W, 1M, YTD) and chart ranges (3M–5Y), group by sector or view flat, filter by sector, and search for any ticker. Toggle between map, sector summary, and table views.

![Market Heatmap](img/market_heatmap.png)

---

## Watchlist

A personalized watchlist with grid and chart views. Each card shows a TradingView price chart with moving average overlays, a revenue & profit mini-chart (net income, margin trend, revenue bars), and a dividend history chart with yield and growth indicators. Toggle visibility layers (MA, Revenue, Dividends), switch time periods, and manage tickers. A persistent sidebar tracks real-time prices and daily changes across your full watchlist.

![Watchlist](img/watchlist_grid.png)

---

## Stock Comparison

Compare any set of stocks side by side. Summary cards show price, YTD/1Y performance, 52-week range, and sector/industry. Includes a normalized price chart (rebased to 100) for direct performance comparison, a multi-period return table (1M through 5Y), a fundamentals radar chart (profit margin, operating margin, gross margin, ROE, ROA, liquidity), and a risk vs. return scatter plot (annualized volatility vs. annualized return).

![Stock Comparison](img/stock_comparison.png)

---

## Sector Analysis

Cross-sector correlation analysis across all 11 S&P 500 sectors. Features a color-coded correlation matrix showing how sectors move together, with cap-weighted and equal-weighted views over 3M–5Y windows. Includes normalized sector performance charts (rebased to $100) to visualize cumulative returns, helping identify diversification opportunities and hedging strategies.

![Sector Analysis](img/sector_correlation.png)

---

## Sector Hexagonal Density Plot

An interactive hexbin scatter plot showing daily return correlations between any two sectors. Pairs are categorized by correlation strength (strong positive, moderate, weak, near zero) and selected via the correlation matrix or quick-pick buttons. Displays regression line, R² value, and data point count — useful for visualizing sector co-movement patterns and tail-risk events.

![Correlation Density Plot](img/correlation_analysis.png)

---

## Congress Trading Tracker

Track stock trades disclosed by U.S. Congress members under the STOCK Act. Dashboard shows total trades, unique tickers, buy/sell breakdown by party (Democrats vs. Republicans), buy/sell sentiment donut chart, and monthly trading activity. Tables highlight the most bought and most sold stocks with estimated volumes, plus best and worst performing trades ranked by excess return vs. S&P 500.

![Congress Trading Tracker](img/congress_trade_tracker.png)

---

## Tech Stack

| Layer | Technology |
|-------|-----------|
| **Frontend** | Next.js 16, React 19, TypeScript, Tailwind CSS |
| **Backend** | Python 3, Flask 3, pandas, NumPy, yfinance |
| **Charts** | TradingView Lightweight Charts, Recharts, D3.js |
| **Data** | Yahoo Finance API, batch caching, scheduled updates |
| **Infra** | Docker, Docker Compose, Nginx reverse proxy |

## Quick Start (Docker)

Run the entire app locally with just **Git** and **Docker**. No Node.js, Python, or other dependencies needed on your machine.

### 1. Clone the repo

```bash
git clone https://github.com/tristcoil/zero-sum-public.git
cd zero-sum-public
```

### 2. Create the config file

```bash
cp backend/.env.example backend/.env
```

That's it — the defaults work out of the box. The app runs fully without any API keys.

> **Optional:** If you want AI-generated stock analysis summaries, open `backend/.env` and add your [OpenAI API key](https://platform.openai.com/api-keys). Everything else (charts, market data, heatmaps, screeners, etc.) works without it.

### 3. Start the app

```bash
docker compose up --build
```

First build takes a few minutes (downloading dependencies, building images). Subsequent starts are fast.

### 4. Open in your browser

- **Frontend:** [http://localhost:3000](http://localhost:3000)
- **Backend API:** [http://localhost:5000/api/health](http://localhost:5000/api/health)

> **Note:** On first start, the background scheduler begins fetching market data. Give it a minute or two for the landing page, heatmap, and other sections to populate.

### Stopping

```bash
# Stop all containers (data is preserved in ./data/)
docker compose down
```

### Updating

```bash
git pull
docker compose up --build
```

---

## What's Inside

| Container | Description |
|-----------|-------------|
| **backend** | Flask API — serves market data, fundamentals, analysis |
| **scheduler** | Background worker — fetches & caches Yahoo Finance data on a schedule |
| **frontend** | Next.js UI — the full dashboard and charting terminal |

All market data is cached in the `./data/` directory on your machine and persists across restarts.

---

## Configuration

All configuration lives in `backend/.env`. Edit it to customize:

| Variable | Default | Description |
|----------|---------|-------------|
| `OPENAI_API_KEY` | *(empty)* | OpenAI key for AI analysis (optional) |
| `OPENAI_ORG_ID` | *(empty)* | OpenAI org ID (optional) |
| `ANALYSIS_MODEL` | `gpt-4o` | Which OpenAI model to use |
| `ANALYSIS_CACHE_HOURS` | `24` | How long to cache AI analysis results |

The scheduler timing and cache TTL can be tuned via `docker-compose.yml` environment variables — the defaults are sensible for local use.

---

## Development (without Docker)

If you prefer running things natively for development:

```bash
# Backend
cd backend
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
cp .env.example .env
python app.py

# Frontend (in a separate terminal)
cd frontend
npm install
npm run dev
```

The frontend runs on `http://localhost:3000` and the backend API on `http://localhost:5000`.

---

## Community

<p align="center">
  <a href="https://github.com/tristcoil/zero-sum-public"><img src="https://img.shields.io/badge/GitHub-Source_Code-181717?style=for-the-badge&logo=github&logoColor=white" alt="GitHub" /></a>
  &nbsp;
  <a href="https://discord.gg/a89Ua6CQj"><img src="https://img.shields.io/badge/Discord-Join_Community-5865F2?style=for-the-badge&logo=discord&logoColor=white" alt="Discord" /></a>
</p>

## License

[MIT](LICENSE)
