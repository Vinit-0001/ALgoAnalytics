**📊 NIFTY 50 Stock–Index Regression Analysis**

Objective-
To identify the most representative benchmark index (such as NIFTY IT, NIFTY BANK, or NIFTY FMCG) for each NIFTY 50 stock by performing linear regression. This helps in understanding sectoral alignment, evaluating index-tracking strategies, and improving portfolio attribution.

Tools Used-

   Tool	                     Purpose
Python + Jupyter	 |  Analysis environment
yfinance	         |  Fetching historical market data
pandas/numpy	     |  Data wrangling
scikit-learn	     |  Linear regression modeling
matplotlib/seaborn |  Visualizing regression results

Outputs-

      File Name	                                Description
regression_results_yfinance.csv	  | All stock–index regression results
best_index_per_stock_yfinance.csv	| Best index assigned to each stock
summary_by_index.csv	            | Average regression metrics per index

_**Run the jupyter notebook at your system to get all the plots.**_

Reasoning Behind Final Index Assignment-
The index assigned to each stock was selected using three criteria: highest R², high correlation, and a reasonable beta (to avoid overfitting or non-economic relationships). This ensures that the selected index not only fits statistically, but also reflects the stock’s underlying market or sector exposure.

**Final Conclusions per Stock**-

_🏦 NIFTY BANK (^NSEBANK)_-

These stocks showed high R², strong correlation, and reasonable beta values when regressed against the NIFTY BANK index:

ICICIBANK.NS
HDFCBANK.NS
SBIN.NS
AXISBANK.NS
KOTAKBANK.NS
SHRIRAMFIN.NS
INDUSINDBK.NS (lower R², but still most aligned with banking sector)

📌 Conclusion: These stocks are most influenced by movements in the banking sector, making ^NSEBANK the best explanatory index.

_💻 NIFTY IT (^CNXIT)_-

High-performing IT sector stocks exhibited strong R² (often > 0.7) and high correlation:

INFY.NS
TCS.NS
TECHM.NS
HCLTECH.NS
WIPRO.NS

📌 Conclusion: IT sector stocks are very tightly coupled with ^CNXIT, with some of the highest correlation and R² values in the entire analysis.

_🚘 NIFTY AUTO (^CNXAUTO)_-

Auto sector stocks showed strong sensitivity to the ^CNXAUTO index:

M&M.NS
TATAMOTORS.NS
MARUTI.NS
HEROMOTOCO.NS
EICHERMOT.NS

📌 Conclusion: Automotive companies are best explained by ^CNXAUTO, indicating they are strongly sector-driven.

_🧴 NIFTY FMCG (^CNXFMCG)_-

FMCG sector leaders aligned well with ^CNXFMCG:

ITC.NS
HINDUNILVR.NS
NESTLEIND.NS
TATACONSUM.NS

📌 Conclusion: Consumer goods companies follow the FMCG sector closely in both correlation and R², confirming the index’s relevance.

_💊 NIFTY PHARMA (^CNXPHARMA)_- 

Pharmaceutical stocks with high R² and correlation with pharma index:

SUNPHARMA.NS
CIPLA.NS
DRREDDY.NS

📌 Conclusion: These stocks are clearly explained by the pharma index, showing tight sectoral behavior.

_🌐 NIFTY 50 (^NSEI) – Broad Market Movers_-

These companies did not align strongly with a single sector index but showed their best fit with the overall NIFTY 50:

RELIANCE.NS
BAJAJFINSV.NS
BAJFINANCE.NS
JSWSTEEL.NS
GRASIM.NS
ADANIENT.NS
ADANIPORTS.NS
TATASTEEL.NS
ONGC.NS
NTPC.NS
POWERGRID.NS
LT.NS
TITAN.NS
ULTRACEMCO.NS
COALINDIA.NS
SBILIFE.NS
HDFCLIFE.NS
JIOFIN.NS

📌 Conclusion: These diversified or multi-sector companies are best explained by the general market movement rather than a single sector, making ^NSEI the most suitable index.

_ **Summary Takeaway**___ - 

1) Sector-specific stocks (IT, Banks, FMCG, Auto, Pharma) strongly align with their respective indices.
2) Diversified or conglomerate companies (e.g., Reliance, Grasim) are best explained by the overall NIFTY 50 index.
3) High R², strong correlation, and reasonable beta thresholds ensured that the assigned index is both statistically and economically sound.
