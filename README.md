# 📈 MT5 Prop Firm Trading Bot — Phase 1 Automation

Robust, fully automated MetaTrader 5 trading bot optimized for prop firm challenges (e.g. The5ers Phase 1). Designed for disciplined execution, daily drawdown compliance, and transparent audit logging.

## 🚀 Highlights

- 🔒 **Risk Management**: Daily and total drawdown guards to prevent challenge violations
- 📊 **Audit Logs**: CSV-based trade logging, error tracking, and restart-safe execution
- 🤖 **Full Automation**: Designed for unattended operation via Task Scheduler & `.bat` scripts
- 🧪 **Empirical Testing**: Strategy backed by months of backtesting and incremental improvements

## ⚙️ Bot Structure

- `live_trader_phase1.py` → Executes trades under strict Phase 1 risk rules  
- `live_trader_highrr.py` → High risk-reward variant for alternative accounts  
- `symbol_reader.py` → Dynamically reads active instruments for trading  
- `csv_cleaner.py` → Clears and resets trade logs daily to ensure auditability  
- `.bat` scripts → Used to auto-run bots and log files via Windows scheduler

## 🧠 Strategy Logic

- Entry and exit based on proven quantitative signals  
- No overfitting — core logic unchanged even as risk modules evolve  
- Filters optimized for prop firm volatility and slippage tolerance

## 🔧 Risk Controls

| Control Type      | Description                             |
|-------------------|------------------------------------------|
| Daily Drawdown    | Hard cap with auto-stop if breached      |
| Total Drawdown    | Safety net with conditional shutdown     |
| Spread Checker    | Filters poor liquidity conditions        |
| Symbol Watchlist  | Active symbol tracking and exclusions    |

## 🗂️ Sample Audit Logs

- Format: `date_time,symbol,action,volume,profit,error_code`
- Logged to: `phase1_trades.csv`
- Restart-safe via checkpointing and error recovery

## 🛠️ Deployment

- Windows Task Scheduler triggers bots and CSV cleaners at set intervals  
- Batch scripts (`run_bot_phase1.bat`, `clean_csv.bat`) manage automation  
- Can be adapted for VPS or server environments

## 📍 Notes

- All trading logic aligns with The5ers Phase 1 rules (as of July 2025)
- Core strategy is fixed — only wrappers and guards adapt to market behavior
- Errors like `10027`, `10030`, `10019` are handled gracefully

## 📫 Contact

For freelance automation, Python scripting, or prop bot consultation:
**GitHub**: [github.com/HDAVEEE]  
**Guru Profile**: [https://www.guru.com/freelancers/hamen-d]

### 📌 Code Disclosure Note

This repository showcases the automation shell, audit logging, and drawdown risk controls of an MT5 trading bot used in live prop firm challenges. 

➡️ **Proprietary strategy logic is omitted** for confidentiality and compliance reasons.  
The sample code highlights bot infrastructure, not trade signal generation.

For collaboration, freelance inquiries, or full logic review under NDA, please contact [https://www.guru.com/freelancers/hamen-d].
