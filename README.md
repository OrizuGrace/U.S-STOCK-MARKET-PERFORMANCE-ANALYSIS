# U.S-STOCK-MARKET-PERFORMANCE-ANALYSIS
### June–July 2025 Stock Market Analysis – 
#### Detailed Report 
### 1) Executive Summary 
This capstone analyzes June–July 2025 equity performance across sectors and tickers using 
Python (Pandas/NumPy) with Matplotlib/Seaborn visualizations. We quantify sector returns, 
isolate top gainers/losers, and examine volatility at both sector level and ticker level 
(alongside average market volatility). We also note average monthly dividend return 
movement and assess the relationship between Market Cap and P/E (weak positive 
correlation, r ≈ 0.19). 
### Key highlights: 
* Technology delivered positive returns in both months (leading cohort), while Healthcare 
was mixed. 
* Volatility was higher in June than July at the market level; Energy/Tech showed the 
widest swings at sector level. 
* Gainers: CRM (+0.76%), INTU (+0.70%) in June; KO (+0.66%), IBM (+0.60%) in July. 
* Losers: GILD (−0.69%), BLK (−0.64%) in June; PM (−0.50%), REGN (−0.48%) in July. 
* Dividend: Average monthly dividend return slightly higher in June than July. 
* Size vs Valuation: Market Cap and P/E only weakly correlated (r ≈ 0.19), so size is not 
a proxy for premium valuation. 
### 2) Dataset Overview 
* Rows/Columns: 4,346 rows × 14 columns (post-cleaning summary from your 
notebook). 
* Timeframe: June and July 2025; counts by month: June = 2,460 rows, July = 1,886 
rows. 
* Coverage: Multiple sectors; daily observations per ticker. 
* Core fields used: Date, Ticker, Sector, Open/Close, 52-Week High/Low, Market Cap, 
P/E Ratio, Dividend info, engineered Daily Return. 
Data quality: 
* Missing values: 0 across key columns after cleaning. 
* Dropped 0 rows due to critical missing fields (Date/Ticker/Open/Close/Sector). 
3) Methodology & Metrics 
### Data cleaning & typing 
* Parsed dates, standardized sector labels, ensured numeric types for prices, Market Cap, 
P/E, Dividend fields. 
Feature engineering 
* Daily Return = (Close − Previous Close) / Previous Close. 
* Monthly Aggregations: 
*○ Sector Performance: mean(Daily Return) by Sector & Month. 
*○ Volatility (Sector): std(Daily Return) by Sector & Month. 
○ Volatility (Market Average): mean or median of per-ticker std(Daily Return) by 
Month (your “average market volatility”). 
○ Volatility (Ticker): std(Daily Return) per ticker; compared to the market average. 
○ Top Gainers/Losers: rank by average Daily Return within each month. 
○ Dividend (Monthly Average): average dividend return by month (across the 
dataset). 
○ Correlation: Pearson correlation between Market Cap and P/E. 
Visualization 
● Side-by-side bar charts (June vs July) for sector performance. 
● Bar/heatmap for sector volatility. 
● Distribution/benchmark strip for ticker volatility vs market average. 
● Bar lists for top 5 gainers/losers by month. 
● Line/bar for average monthly dividend return. 
● Scatter: Market Cap vs P/E with Pearson r. 
### 4) Results & Interpretation 
#### 4.1 Sector Performance (June vs July) 
● Technology: Positive in both June and July → consistently among top performers. 
● Healthcare: Mixed profile across the two months → uneven momentum. 
● Cross-month shifts: Several sectors reversed direction from June to July, reflecting 
sensitivity to evolving market conditions. 
What it means: Sector rotation was present; Tech stayed resilient while Healthcare required 
selective exposure. 
#### 4.2 Volatility (Sector Level) 
● Highest volatility: Technology and Energy (largest std of Daily Returns). 
● Lowest volatility: Utilities and Consumer Staples (defensive posture). 
Implication: High-vol sectors offer tactical opportunities but call for tighter risk controls; low-vol 
sectors suit capital preservation/income strategies. 
#### 4.3 Volatility (Market Average & Ticker Level) 
● Average market volatility: Higher in June than in July → more turbulent early period. 
● Ticker deviations: 
○ Some stocks in “stable” sectors still showed above-average volatility 
(company-specific factors). 
○ Some stocks in “risky” sectors showed below-average volatility (idiosyncratic 
stability). 
Implication: Don’t infer ticker risk purely from sector; evaluate each company’s volatility against 
the market baseline. 
#### 4.4 Top Gainers & Losers 
Top Gainers – June 2025 
1. CRM +0.756% 
2. INTU +0.702% 
3. PYPL +0.645% 
4. XOM +0.629% 
5. UBER +0.545% 
Top Gainers – July 2025 
1. KO +0.656% 
2. IBM +0.599% 
3. UNP +0.596% 
4. ORCL +0.572% 
5. NOW +0.549% 
Top Losers – June 2025 
1. GILD −0.693% 
2. BLK −0.639% 
3. GOOGL −0.512% 
4. PEP −0.453% 
5. ELV −0.421% 
Top Losers – July 2025 
1. PM −0.497% 
2. REGN −0.478% 
3. GS −0.465% 
4. BRK.B −0.452% 
5. PFE −0.388% 
Interpretation: 
● June winners skewed to growth/energy momentum; July winners tilted 
defensive/industrial, hinting at risk-off rotation. 
● Losers concentrated in Healthcare/Financials in June and Consumer 
Staples/Healthcare in July—showing sector-specific headwinds that shifted 
month-to-month. 
#### 4.5 Dividend (Average Monthly Return) 
● Higher in June than July → slight month-to-month dip in income potential. 
Interpretation: Dividend yield conditions softened into July; income-focused strategies might 
time entries around stronger months or focus on stable payers. 
4.6 Market Cap vs P/E Ratio 
● Pearson r ≈ 0.19 (weak positive). 
Interpretation: Larger companies aren’t automatically priced at richer multiples; 
valuation must be assessed ticker-by-ticker. 
### 5) Potential Shareholder Applications 
● Sector Positioning: Tilt toward sectors with consistent 2-month strength (e.g., 
Technology) while using careful, selective exposure in mixed sectors (e.g., Healthcare). 
● Risk Calibration: Use sector vs ticker volatility to choose where to seek tactical alpha 
versus where to hold defensive positions. 
● Momentum Screening: Track the monthly Top 5 gainers/losers to surface candidates 
for follow-up research. 
● Dividend Awareness: Monitor average monthly dividend return shifts when planning 
income strategies. 
● Valuation Discipline: Apply fundamental review beyond size; weak cap-P/E link 
means no shortcuts on company analysis. 
### 6) Limitations 
● Two-month window limits generalization; potential monthly anomalies. 
● No macro overlay in this capstone (rates, CPI, earnings) → narrative for “why” is 
indicative, not definitive. 
● Historical/descriptive focus; no predictive modeling included. 
### 8) Tools & Environment 
● Python (analysis), Pandas (wrangling), NumPy (numeric ops), Matplotlib/Seaborn 
(viz), Jupyter Notebook (workflow). 
### 9) Appendix – Metric Definitions (for clarity) 
● Daily Return = (Close_t − Close_{t−1}) / Close_{t−1}. 
● Monthly Sector Performance = mean(Daily Return) per Sector, per Month. 
● Volatility (std) = standard deviation of Daily Return. 
● Average Market Volatility = average (or median) of per-ticker volatility in a month. 
● Top Gainers/Losers = top/bottom tickers by average Daily Return in a month. 
● Dividend (Monthly Average) = average dividend return across dataset by month. 
● Pearson r (Market Cap vs P/E) = linear correlation coefficient. 
