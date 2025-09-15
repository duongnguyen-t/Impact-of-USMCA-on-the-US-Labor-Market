# 📌 Trade Policy & Tariff Impacts: A Data Analysis Approach

## Overview  
This project evaluates the economic effects of the U.S. trade war and the disbanding of NAFTA. It analyzes how tariffs influence industries, employment, and supply chains using econometric modeling and large-scale trade datasets.

## TL;DR (CHECK REPORT VISUALS)
- I link industry-level trade shocks to individual wages using IPUMS microdata (~2.87M rows) for 2019–2020.
- Raw wage means across shock bins are non‑monotonic; results become cleaner after trimming extremes, weighting, and adding controls.
- I document heterogeneity by border vs non-border areas and education.
- All figures are reproducible with the scripts below; a lightweight optional report is included.


## Key Findings
1) Trade contraction: largest declines in Petroleum & Coal (324), Transportation Equipment (336), and Computer & Electronic Products (334).
![Industries with the largest negative change in trade (named by NAICS)](graphs/industry%20with%20largest%20neg%20change.png)
2) Education gradient: higher education → higher log(wage), consistent across border status.
![Wages by education, border vs non-border (2019-2020)](graphs/wages%20by%20education.png)
3) Time shift: from 2019 to 2020, distributions move slightly with some group differences (see change‑bars).
![Change in mean log(wage), 2019-2020, border vs non-border](graphs/change%20in%20wage.png)
4) Shock gradient: raw decile means are jagged (composition); weighted medians are closer and more stable.
![Wages across trade-shock deciles (weighted mean & median, with sample size n)](graphs/wage%20across%20trade%20shock%20decile.png)


## Data Sources  
- U.S. Census Bureau (Trade & Employment Data)  
- Bureau of Economic Analysis (Industry Output Data)  
- World Bank (Tariff & Trade Data)  

## Technologies Used  
- **Python**: pandas, NumPy, BeautifulSoup (for web scraping)  
- **Data Cleaning & Analysis**: pandas, NumPy  
- **Statistical Modeling**: Stata, R  
- **Regression Analysis**: scikit-learn, statsmodels

## Limitations
- Observational design; not causal without stronger identification.
- Industry composition across exposure bins can confound raw means; we therefore show medians, weights, and controlled residual plots.
- Mapping between shocks and NAICS codes may miss a subset of industries; see notebook for coverage rates.

## How to Run  
1. Clone the repository:  
   ```bash
   git clone https://github.com/duongnguyen-t/Impact-of-USMCA-on-the-US-Labor-Market.git
   cd Impact-of-USMCA-on-the-US-Labor-Market
2. Install dependencies:
   ```bash
   pip install pandas numpy matplotlib seaborn statsmodels
3. Run it:
   ```bash
   python trade_analysis.py
Have fun!
