Overview:
Systematic FX research pipeline implementing carry, trend, and value signals with modular portfolio construction and backtesting.
Best standalone construction: inverse volatility, net Sharpe ~0.32.
All signals are constructed using lagged data to preserve causality

Pipeline Structure:
0. FX Data: Data ingestion, cleaning, alignment, and currency standardization
1a. FX Carry: Construction of carry signals using interest rate differentials and forward approximations
1b. FX Trend: Time-series momentum and trend extraction across multiple horizons
1c. FX Value: Price-based reversal proxy defined as the negative 50-day minus 200-day moving average of log price
2. Feature Discovery: Systematic extraction and testing of derived features from time series and cross-sectional structure
3. Portfolio Construction: Signal combination, risk scaling, and implementation of multiple weighting schemes
4. Diagnostics: Performance evaluation including Sharpe, drawdown, turnover, and robustness checks

Results:
Inverse volatility weighting provides the strongest standalone baseline with a net Sharpe of approximately 0.32.
Combining signals through portfolio construction improves risk-adjusted returns relative to individual sleeves.
Experimental scalar overlays and conditioning methods show potential but are not relied upon due to calibration limitations.
