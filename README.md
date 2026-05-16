# ⚡ Supply Buy Bot

Production-ready Telegram buy-alert bot with real-time monitoring, whale detection, trending system, BBNS name service, buy competitions, and a full web dashboard. Supports BSC, Ethereum, and Base — with Solana, TON, Monad, and Sui coming soon.

[![Python](https://img.shields.io/badge/Python-3.10+-3776AB?style=flat-square&logo=python&logoColor=white)](.)
[![Telegram](https://img.shields.io/badge/Telegram_Bot_API-26A5E4?style=flat-square&logo=telegram&logoColor=white)](.)
[![License](https://img.shields.io/badge/License-MIT-7c3aed?style=flat-square)](.)
[![Chains](https://img.shields.io/badge/Chains-BSC_·_ETH_·_Base-F3BA2F?style=flat-square)](.)

---

## ✨ Features

| Feature | Description |
|---|---|
| 🟢 **Buy Alerts** | Real-time alerts for every token buy in your group |
| 📈 **Trending System** | Organic top 10 by volume + paid spots, updated every 5 mins |
| 📛 **BBNS** | Buy Bot Name Service — register wallet display names ($5/year) |
| 🐋 **Whale Detection** | Special alerts when whale wallets buy above threshold |
| 🏆 **Buy Competitions** | Time-limited contests with auto leaderboards |
| ✅ **Auto-Verification** | DexScreener-based chat verification |
| 🖼️ **GIF Support** | Custom GIF or image on every buy alert |
| 🌐 **Web Dashboard** | Full admin panel — groups, BBNS, trending, tickets |
| 🎫 **Support Tickets** | Built-in ticket system with admin resolution |
| 🔒 **Rate Limiting** | Per-API and per-user anti-abuse protection |

---

## 🔗 Supported Chains

| Chain | Status | DEX Support |
|---|---|---|
| 🟡 BNB Chain (BSC) | ✅ Live | PancakeSwap, BiSwap, SushiSwap |
| 🔷 Ethereum | ✅ Live | Uniswap V2/V3, SushiSwap, 1inch |
| 🟦 Base | ✅ Live | Uniswap V3, Aerodrome |
| 🟣 Solana | 🔜 Soon | Raydium, Jupiter |
| 🟣 Monad | 🔜 Soon | TBD |
| 💎 TON | 🔜 Soon | DeDust, STON.fi |
| 🌊 Sui | 🔜 Soon | Cetus, BlueMove |

---

## 🚀 Quick Start

**Prerequisites:** Python 3.10+, Telegram Bot Token, free API keys for BSCScan / Etherscan / BaseScan

```bash
git clone <your-repo-url>
cd supply-buy-bot
pip install -r requirements.txt
cp .env.example .env
nano .env        # add your keys
python main.py   # start the bot
```

Dashboard runs separately:
```bash
python dashboard.py     # admin panel → localhost:5000/admin
python token_website.py # token site  → localhost:5001
```

---

## ⚙️ Environment Variables

```bash
TELEGRAM_BOT_TOKEN=your_bot_token
BSCSCAN_API_KEY=your_key
ETHERSCAN_API_KEY=your_key
BASESCAN_API_KEY=your_key
PAYMENT_WALLET_BSC=0x_your_wallet
PAYMENT_WALLET_ETH=0x_your_wallet
PAYMENT_WALLET_BASE=0x_your_wallet
ADMIN_USER_IDS=123456789
DASHBOARD_USERNAME=admin
DASHBOARD_PASSWORD=your_password
DB_PATH=buytech.db
```

---

## 📊 Buy Alert Format

```
🔷 @Supply_Buy_Bot | Ethereum ✅

ASTEROID Buy!
🐕🐕🐕🐕🐕

💵 0.039 ETH ($88.60)
🪙 329,608 ASTEROID
🔷 0xff00…2218 | Txn
✅ New Holder
🔼 Market Cap $113.09M

📊 Chart  🦄 Trade  🔹 Trending
```

---

## 📈 Trending System

**Organic (free)** — top 10 tokens by 24h buy volume, auto-updated every 5 mins.

**Paid spots:**

| Duration | Supply Option | ETH Option |
|---|---|---|
| 6 hours | 1% of supply | 0.1 ETH |
| 12 hours | 1.5% of supply | 0.15 ETH |
| 24 hours | 2% of supply | 0.2 ETH |
| 48 hours | 3% of supply | 0.3 ETH |

---

## 🗂️ Project Structure

```
supply-buy-bot/
├── main.py           # Entry point
├── bot.py            # Command handlers
├── monitor.py        # Buy monitoring + trending loops
├── formatter.py      # Alert formatting
├── database.py       # SQLite + migrations
├── chains.py         # Chain config + DEX routers
├── price.py          # DexScreener + CoinGecko
├── rate_limiter.py   # Rate limiting
├── dashboard.py      # Flask admin panel
└── token_website.py  # Token website
```

---

## 🔧 Tech Stack

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![Telegram](https://img.shields.io/badge/python--telegram--bot-26A5E4?style=flat-square&logo=telegram&logoColor=white)
![Flask](https://img.shields.io/badge/Flask-000000?style=flat-square&logo=flask&logoColor=white)
![SQLite](https://img.shields.io/badge/SQLite-07405E?style=flat-square&logo=sqlite&logoColor=white)
![aiohttp](https://img.shields.io/badge/aiohttp-2C5BB4?style=flat-square&logoColor=white)

- **Bot:** python-telegram-bot 21.x + aiohttp
- **Data:** DexScreener API + CoinGecko + BSCScan/Etherscan/BaseScan
- **DB:** SQLite with WAL mode
- **Dashboard:** Flask + Bootstrap 5

---

## 🛠️ Deployment

```bash
# Linux systemd
sudo cp supply-buy-bot.service /etc/systemd/system/
sudo systemctl enable supply-buy-bot
sudo systemctl start supply-buy-bot
```

---

## 📞 Support

- **Telegram:** [@Supply_Buy_Bot](https://t.me/Supply_Buy_Bot)
- **Tutorials:** [@SupplyBotTutorials](https://t.me/SupplyBotTutorials)
- **Trending:** [@SupplyTechTrending](https://t.me/SupplyTechTrending)

---

**Built by [@oxbobdev](https://github.com/0xbobdev) · [0xbob.vercel.app](https://0xbob.vercel.app) · [t.me/oxbobdev](https://t.me/oxbobdev)**
