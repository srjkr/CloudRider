🤖 CloudRider Bot

An automated trading bot for MetaTrader 5 (MT5) that combines Ichimoku Cloud, ADX, EMA, and ATR for smart trade execution.
It sends real-time trade alerts to Telegram and manages trades with advanced risk management (break-even, ATR-based SL/TP, optional trailing stop).

✨ Features

✅ Connects directly to MetaTrader 5 (via Python API).

✅ Implements Ichimoku + EMA + ADX strategy for entries.

✅ Automatic ATR-based Stop Loss & Take Profit.

✅ Optional Trailing Stop Loss & Break-even logic.

✅ Telegram notifications for trade signals, executions, and errors.

✅ Flexible risk management: manual or automatic lot sizing.

✅ Logging for full trade history & debugging.

📂 Project Structure
cloudrider/
│── cloudrider.py       # Main bot script
│── cloudrider.log      # Auto-generated logs
│── requirements.txt    # Python dependencies
│── README.md           # Project documentation

🔧 Installation
1. Clone the repo
git clone https://github.com/yourusername/cloudrider.git
cd cloudrider

2. Install dependencies
pip install -r requirements.txt


requirements.txt:
MetaTrader5
pandas
requests

3. Configure settings
Open cloudrider.py and update:
MT5_ACCOUNT   = 12345678
MT5_PASSWORD  = "your_mt5_password"
MT5_SERVER    = "Broker-Server"
TELEGRAM_BOT_TOKEN = "your_telegram_token"
CHAT_ID = 123456789

▶️ Usage
Run the bot:
python cloudrider.py

It will:
Connect to MT5.
Fetch data every 60s.
Check for signals.
Place trades automatically.
Notify via Telegram.

📊 Strategy Overview

Entry: Tenkan/Kijun crossover + confirmation by Ichimoku Cloud, EMA 50, ADX filter.
Exit: ATR-based Stop Loss & Take Profit, optional trailing stop.
Risk: Configurable via RISK_PERCENT or manual lot size.

📈 Example Telegram Alerts
⚡ Signal detected: BUY at 2025-08-19 09:25 IST
📈 New Trade Opened
Direction: BUY
Lot Size: 0.01
Entry Price: 29250.50
Stop Loss: 29120.00
Take Profit: 29510.00
Time: 2025-08-19 09:25 IST

🛑 Safety Notes

Test on demo account first.
Make sure your MT5 terminal is running and logged in.
Always double-check broker execution rules.

🧑‍💻 Tech Stack

Python 3.10+
MetaTrader5 (official Python API)
Pandas

Requests (for Telegram API)

📜 License
MIT License – feel free to use and improve.