# Hourly-Distro
Price Distribution
![screenshot]([https://github.com/Desiringmachine/Hourly-Distro/blob/main/hourly%20distro%20scren.png])

# Hourly Distro [Desiringmachine]

**Hourly Distro** is an advanced statistical price-distribution mapping and volatility regime monitoring indicator for TradingView, written in Pine Script v6. It tracks and compares historical return distributions across specific time windows to give real-time insights into market volatility regimes and standard deviation percentiles.

[**🔗 View and Install on TradingView**](https://www.tradingview.com/script/YUPkgcZw-Hourly-Distro-Desiringmachine/)

---

## 📊 Core Concept
This indicator maps out how the current active price action compares to historical norms. By tracking a long-term **Base** statistical distribution (e.g., 5 Years) against a short-term **Roll** distribution (e.g., 20 Days), it instantly visualizes whether the current market for a specific time-of-day or session is in a state of volatility compression or expansion. 

## ✨ Key Features

* **Multi-Timeframe & Time-of-Day Specific**: Tracks independent distributions for individual Hours (H00-H23), Trading Sessions (Asia, London, NY AM, NY PM), Daily (D), Weekly (W), Monthly (M), and Yearly (Y) intervals.
* **Base vs. Roll Comparison (Sx vs Dx)**: Compares a long-term statistical baseline (Base/Sx) against a short-term rolling window (Roll/Dx) to identify shifting volatility trends.
* **Real-Time Standard Deviation Percentiles**: Calculates the exact normal percentile (`p`) of the currently forming candle/session relative to the historical standard deviation (+/- 1SD, 1.5SD, 2SD bounds).
* **Regime Detection**: Automatically flags the volatility state of each active time window:
  * **Compression**: Short-term volatility is significantly lower than the baseline (Ratio < 0.95).
  * **Expansion**: Short-term volatility is significantly higher than the baseline (Ratio > 1.05).
  * **Normal**: Short-term volatility aligns with historical norms.
  * **Warming**: Gathering historical sample data.
* **Highly Optimized Execution**: Engineered using advanced Pine Script v6 tuple-consolidation techniques (e.g., `f_allSessions_HD`, `f_allHours_HD`) to bypass strict `request.security()` call limits. This prevents memory limit exceptions and allows massive amounts of multi-timeframe data to be processed natively on any chart timeframe (1m, 5m, etc.).

## ⚙️ Configuration
The indicator is highly customizable via the TradingView inputs panel:
* **Toggle Visibility**: Turn columns ON/OFF individually (H, S, D, W, M, Y).
* **Distribution Samples**: Adjust the lookback windows (in Years and Days) independently for the Base and Roll datasets.
* **Dedicated Yearly Window Settings**: The Yearly (Y) column features entirely independent sampling settings (Base Years, Roll Bars, Min Samples) to ensure accurate statistical sampling without affecting the higher-frequency columns.
* **Display Settings**: Fully customizable UI colors, column widths, standard deviation lines, regime ranges, and text sizes.

## 🤝 Credits & Acknowledgements

* **Author / Code:** [x.com/Desiringmachine](https://x.com/Desiringmachine) · GitHub: [@Desiringmachine](https://github.com/Desiringmachine)
* **Concept:** [nqstats.com](https://nqstats.com/) ([x.com/@probablechris](https://x.com/probablechris))

---
*Disclaimer: This indicator is for informational and statistical purposes only and does not constitute financial advice.*
