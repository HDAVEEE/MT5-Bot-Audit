# 🛡️ Audit & Restart Logic Guide

This guide outlines the safety mechanisms implemented in the MT5 Phase 1 Trading Bot, designed for prop firm challenges and strict drawdown compliance.

---

## ⚠️ Risk Guards Implemented

- **Daily Drawdown Cap**: Trades are blocked if cumulative loss exceeds threshold.
- **Total Drawdown Cap**: Bot halts if total balance drops below predefined value.
- **Session-Based Limits**: Max trades per symbol and per time window.

---

## 🔁 Restart Conditions

| Trigger | Response |
|--------|----------|
| MT5 Error 10027 / 10030 | Retry logic + pause |
| Risk Violation | Skip trade + log entry |
| Symbol Offline | Delisted from active cycle |

---

## 🧪 Audit Visibility

- All trades logged in real-time
- CSV logs with timestamps and skipped reasons
- Shell and batch script compatibility for service restart
