# 🎯 Expectancy Heatmap — Interpretation Guide

This document outlines how the heatmap was generated, what its values represent, and why it enhances auditability in prop firm settings.

---

## 🔢 Grid Construction

- **Rows**: Signal Confidence Bands (e.g. low, medium, high)
- **Columns**: Market Volatility Segments (e.g. calm, neutral, aggressive)
- **Cell Value**: Average expected return per trade over N trials

All values are calculated from session-level logs, filtered and aggregated using Python and pandas.

---

## 🌈 Color Mapping

| Color | Meaning |
|-------|--------|
| 🔴 Red | Negative expectancy (avoid trading) |
| 🟠 Orange | Marginal outcome — needs risk screening |
| 🟢 Green | Positive expectancy — bot allowed entries |
| 🟣 Purple | High reward but flagged for elevated risk |

Colors guide the bot’s internal signal filtration. Zones with unstable expectancy trigger trade blocks or skip logic via restart-safe modules.

---

## 🔐 Compliance Notes

This heatmap was derived from:
- `phase1_trades.csv` (sample and anonymized)
- Bot actions logged via `log_trade()` handler
- Data validated using timestamp matching and outcome reconciliation

No proprietary entry logic disclosed. All visuals serve audit simulation only.
