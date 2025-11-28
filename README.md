# NIFTY 50 Trading Analysis (2015–2025)

This project performs a complete beginner-friendly trading analysis on the **NIFTY 50 Index (^NSEI)** using **10 years of historical data** (2015-11-28 to 2025-11-28).  
It includes data cleaning, indicator computation, signal generation, backtesting, performance comparison, and trade-log creation.

This project demonstrates skills in **Python**, **Pandas**, **Financial Data Analysis**, **Backtesting**, and **Time-Series Visualization**.

---

## 🚀 Project Overview

This notebook implements a simple **trend-following trading strategy** using:

### ✔ 20-Day Simple Moving Average (SMA20)  
### ✔ 50-Day Simple Moving Average (SMA50)

It compares the performance of this strategy against the NIFTY 50 market return.

### The workflow includes:
- Downloading historical NIFTY 50 data  
- Fixing MultiIndex columns returned by Yahoo Finance  
- Cleaning and preparing the dataset  
- Calculating SMA20 and SMA50  
- Generating Buy/Sell trading signals  
- Backtesting a simple long-only strategy  
- Calculating cumulative returns  
- Saving clean data and trade logs  
- Plotting signals and performance  

---

## 📂 Project Files

| File | Description |
|------|-------------|
| `nifty_trading_analysis.ipynb` | Main notebook containing full analysis |
| `nifty_10yr_clean_signals.csv` | Clean dataset with SMA indicators + signals |
| `nifty_trade_log.csv` | Generated trade log from SMA strategy |
| `README.md` | Full project documentation |

---

## 📊 Data Source
This project uses **Yahoo Finance** through the `yfinance` library.

```
Ticker: ^NSEI  
Index: NIFTY 50  
Interval: 1 Day  
```

---

## 🧠 Technical Stack

- **Python 3**
- **Pandas** — data cleaning & manipulation  
- **NumPy** — numerical calculations  
- **Matplotlib** — plotting  
- **yfinance** — data source  
- **Jupyter Notebook / Google Colab** — development environment  

---

## 📈 Strategy Logic (SMA Crossover)

### Indicators:
- **SMA20** = 20-day moving average  
- **SMA50** = 50-day moving average  

### Trading rule:
```
If SMA20 > SMA50 → BUY (Signal = 1)
If SMA20 < SMA50 → EXIT (Signal = 0)
```

To avoid “look-ahead bias”, signals are shifted by **1 day** (trade happens next day).

---

## 📉 Performance Metrics

The notebook computes:

- **Annualized Market Return**
- **Annualized Strategy Return**
- **Sharpe Ratio (Market vs Strategy)**
- **Cumulative Returns**
- **Total number of trades executed**

A trade-by-trade log is saved to `nifty_trade_log.csv`.

---

## 📊 Visualizations

The notebook plots:

1. **NIFTY 50 Price Chart with SMA20, SMA50, Buy & Sell markers**  
2. **Cumulative Performance: Market vs Strategy**  

These are automatically generated when running the notebook.

---

## ▶️ How to Run the Project

### **Option 1 — Google Colab (Recommended)**
1. Open https://colab.research.google.com  
2. Upload `nifty_trading_analysis.ipynb`  
3. Run all cells  

---

### **Option 2 — Jupyter Notebook**
Install dependencies:

```bash
pip install pandas numpy yfinance matplotlib notebook
```

Start Jupyter:

```bash
jupyter notebook
```

Open the notebook and run all cells.

---

### **Option 3 — VS Code**
1. Install “Python” extension  
2. Open the `.ipynb` file  
3. Click “Run All”  

---

## 📊 Power BI (Optional)

You can build a dashboard using:

- `nifty_10yr_clean_signals.csv`
- `nifty_trade_log.csv`

Suggested visuals:
- Price + SMA chart  
- Signal chart  
- Trade log table  
- KPI cards (returns, Sharpe ratio)  
- Market vs Strategy chart  

---

## 🚀 Future Enhancements
Potential improvements:

- Add more indicators: RSI, MACD, Bollinger Bands  
- Add stop-loss / take-profit logic  
- Portfolio-level backtesting  
- Hyperparameter tuning for SMA lengths  
- Deploy dashboard using Streamlit  

---

## 👤 Author
This project was created as a hands-on data analysis and algorithmic trading exercise.  
Feel free to fork, star, or modify the repository.

---

## ⭐ If you found this project useful, please give it a star on GitHub!


![Python](https://img.shields.io/badge/Python-3.9+-blue)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-yellowgreen)
![Matplotlib](https://img.shields.io/badge/Matplotlib-Visualization-orange)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-red)
![Status](https://img.shields.io/badge/Project-Complete-brightgreen)
