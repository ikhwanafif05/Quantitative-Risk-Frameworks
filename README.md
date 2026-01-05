# Quantitative Risk Frameworks (Python)

### Executive Summary
This repository contains algorithmic tools designed to stress-test equity portfolios against systemic macro-shocks. Developed to bridge the gap between fundamental valuation (DCF) and quantitative risk management.

**Core Engines:**
1.  **FX Sensitivity Scanner (The "Trade War" Engine):** Quantifies portfolio beta relative to USD/MYR fluctuations.
2.  **Historical Stress Tester (The "Liquidity" Engine):** Simulates capital preservation capabilities during black swan events (e.g., Covid-19 Crash).

---

## 1. FX Sensitivity Scanner (Trade War Hedge)
**Objective:** Identify "Natural Hedges" in a Malaysian equity portfolio.
* **Logic:** Calculates the rolling beta of assets against `MYR=X` (USD/MYR).
* **Metric:** `Beta > 0` indicates the asset acts as a hedge (gains value when Ringgit weakens). `R-Squared` measures the reliability of this correlation.

**Visual Output:**
*<img width="1187" height="690" alt="Unknown-2" src="https://github.com/user-attachments/assets/64697964-1b6a-45e4-b040-28f7bf19beb7" />*

---

## 2. Portfolio Stress Tester (Historical Replay)
**Objective:** Test liquidity resilience against a known systemic crash (Feb-Apr 2020).
* **Logic:** Reconstructs portfolio performance using historical price data during the Covid-19 liquidity crunch.
* **Metric:** `Max Drawdown (%)` vs. `KLCI Benchmark`.

**Visual Output:**
*<img width="1384" height="783" alt="Unknown" src="https://github.com/user-attachments/assets/525283d0-9097-4254-bde5-9441504c58b8" />*

---

### Technical Stack
* **Language:** Python 3.9+
* **Libraries:** `yfinance` (Data Ingestion), `pandas` (Time-Series), `scipy.stats` (Linear Regression), `matplotlib/seaborn` (Visualization).
* **Data Source:** Yahoo Finance API (Adjusted Close).
