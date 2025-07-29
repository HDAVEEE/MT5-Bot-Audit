# 📁 Documentation & Assets

This folder contains visual references, code snippets, and audit logs to support the design, operation, and compliance of the MT5 Phase 1 Trading Bot.

---

## 📄 File Index

| File Name               | Description |
|------------------------|-------------|
| `bot_architecture.png` | Visual flowchart of bot logic: Signal → Risk → Execution |
| `audit_flowchart.pdf`  | Restart logic and audit safeguards for risk control |
| `phase1_trader_shell.py` | Shell script used to launch bot with error handlers |
| `Terminal_run.png`     | Screenshot of bot running in CMD/Batch environment |
| `live_trades_backup.csv` | Sample trade log with symbol, timestamps, actions |
| `README.md`            | This file — overview of folder contents and usage |

---

## ✅ Suggested Usage

- Recruiters and collaborators: Start here to understand structure and robustness.
- Prop firm reviewers: Reference flowchart and CSV logs for audit visibility.
- Developers: Fork the repo to extend logging, drawdown guards, or deployment logic.

- ## 🔍 Strategy Expectancy Heatmap

This visual reflects how the bot evaluates risk-reward expectancy across market conditions. Each cell represents average expected return per trade, segmented by volatility bins and signal confidence.

![Expectancy Heatmap](docs/expectancy_heatmap.png)

> 📌 *Why this matters*:  
The bot prioritizes high-confidence, low-drawdown entries — calibrated dynamically to meet prop firm rules. This heatmap demonstrates the algorithm’s intelligent filtering across live market phases.

*Last updated: July 29, 2025*
