# Binance Portfolio Demo (CLI + GUI)
![Dashboard](assets/dashboard1.png)

### Buy Simulation
![Buy Example](dashboard2.png)
![Dashboard1](assets/dashboard3.png)



A portfolio-ready demo that simulates a Binance futures trading bot.  
Works in restricted regions by running in **mock mode** (no API keys required). If you have `python-binance` and testnet keys you can enable real testnet mode.

## Features
- CLI: buy/sell/prices/balance/calc-size/trade (simulated)
- GUI: Streamlit app to view prices, portfolio and simulate trades
- Mock fallback (file-backed JSON): runs anywhere without Binance API access

## Quick start (mock mode)
```bash
git clone https://github.com/redrex1034/binance-portfolio-demo.git
cd binance-portfolio-demo
python3 -m venv venv
source venv/bin/activate      # or venv\\Scripts\\activate on Windows
pip install -r requirements.txt
# Run CLI examples
python trading_bot.py prices
python trading_bot.py balance
python trading_bot.py buy BTCUSDT 0.001
python trading_bot.py sell BTCUSDT 0.001
# Run GUI
streamlit run gui_app.py

📘 README.md
# 💹 Binance Portfolio Demo (CLI + GUI)

A simulated **Binance trading bot** built with **Python** and **Streamlit**, designed for portfolio use and learning.  
Runs entirely in **mock mode** (no real API required) and works even in regions where Binance API creation is restricted.

<p align="center">
  <img src="assets/dashboard-dark.png" width="800" alt="Dashboard Screenshot">
</p>

---

## 🚀 Features

✅ **CLI Trading Bot**
- Simulated Buy/Sell orders  
- Portfolio balance management  
- Risk-based position sizing  
- Optional Binance Testnet API integration  

✅ **Streamlit GUI**
- Real-time mock price display  
- Interactive trade simulation  
- Portfolio visualization (pie chart)  
- Dark mode interface for presentation  

✅ **Safe & Offline**
- No real API keys required  
- Works with mock JSON data  
- Perfect for restricted countries and demo portfolios  

---

## 🧠 Project Structure



binance-portfolio-demo/
├── data/
│ ├── mock_prices.json
│ └── mock_balance.json
├── assets/
│ └── dashboard-dark.png
├── trading_bot.py # CLI bot (mock + optional real)
├── gui_app.py # Streamlit dashboard
├── requirements.txt
└── README.md


---

## ⚙️ Setup Instructions (Windows)

### 1️⃣ Install Python 3.11
> ⚠️ Python 3.14 is **not supported** by Streamlit or PyArrow.

- Download Python 3.11 from the official site:  
  👉 [https://www.python.org/downloads/release/python-3110/](https://www.python.org/downloads/release/python-3110/)
- During installation:
  - ✅ Check **“Add Python to PATH”**
  - ✅ Choose **“Install for all users”**

Verify installation:
```bash
python --version


You should see:

Python 3.11.x

2️⃣ Create a Virtual Environment

In your project folder:

python -m venv venv

🧩 Activating on Windows (PowerShell)

By default, PowerShell blocks scripts.
If you see this error:

.\venv\Scripts\Activate.ps1 cannot be loaded because running scripts is disabled on this system


👉 Run PowerShell as Administrator, then execute:

Set-ExecutionPolicy RemoteSigned


Type Y and press Enter.

Now activate the environment:

.\venv\Scripts\Activate


When active, you’ll see (venv) at the start of your prompt.

✅ Optional (for security): after you’re done, reset it:

Set-ExecutionPolicy Restricted

3️⃣ Install Dependencies
pip install --upgrade pip
pip install -r requirements.txt


If you don’t have a requirements.txt yet:

pip install streamlit matplotlib

💻 Run the App
▶️ Run the CLI

Simulate trades and view balances:

python trading_bot.py prices
python trading_bot.py buy BTCUSDT 0.01
python trading_bot.py balance

🌐 Run the GUI

Launch the Streamlit dashboard:

streamlit run gui_app.py


Then open your browser at http://localhost:8501
.

🧪 Optional: Binance Testnet Setup

If you later obtain Binance testnet API keys:

Copy .env.example → .env

Fill in:

BINANCE_API_KEY=your_testnet_key
BINANCE_API_SECRET=your_testnet_secret


Run CLI with:

python trading_bot.py --use-real --api-key YOUR_KEY --api-secret YOUR_SECRET --testnet prices


⚠️ Only use testnet keys — never live keys for demos.

🖼️ Screenshots
Dashboard Overview
<p align="center"> <img src="assets/dashboard-dark.png" width="800" alt="Dark Mode Dashboard"> </p>
💡 Troubleshooting
🔹 “Python was not found” error

Ensure Python 3.11 is installed and added to PATH.

If CMD still doesn’t recognize Python:

Open Settings → Apps → App Execution Aliases

Turn off all “Python” aliases.

🔹 “Activate.ps1 cannot be loaded” error

Fix by running:

Set-ExecutionPolicy RemoteSigned


Then:

.\venv\Scripts\Activate

🔹 Streamlit / PyArrow installation error

Ensure you’re using Python 3.10 or 3.11, not 3.14.
Then reinstall:

pip install streamlit matplotlib

🪄 Portfolio Tips

Add screenshots (assets/) to your README for a polished GitHub look.

Mention that the bot uses mock/testnet data due to Binance API restrictions.

You can demo this project safely without risking any funds.

🧾 License

MIT License © 2025 Donatus-ododemene chinecherem chimobim

👤 Author

Donatus-ododemene chinecherem chimobim
🔗 GitHub

