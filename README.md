# Income Distribution Analysis in Canada (1982–2018)

This repository contains applied econometrics and data analysis projects focusing on the evolution of wage inequality in Canada. The analysis is based on microdata from the Survey of Consumer Finances (1982, 1990) and the Canadian Income Survey (2016, 2018). 

The scripts process large-scale survey data, apply statistical rigor, and model complex systems to understand the underlying drivers of income disparity over a 36-year period.

## 🛠 Language & Libraries
* **Language:** Python
* **Data Manipulation:** `pandas`, `numpy`
* **Econometrics & Modeling:** `statsmodels` (WLS regressions, Variance Inflation Factor)
* **Visualization:** `matplotlib`

---

## 📊 Project 1: Wage Inequality Trends & Composition-Adjusted Wages
**File:** `hw2_script.py`

This project quantifies the evolution of Canadian wage inequality and applies the Autor, Katz, and Kearney (AKK) methodology to control for shifting labor force demographics.

### Methodology
* Cleaned and standardized hourly wage data across four distinct survey decades, adjusting for inflation (CPI) to calculate real wages in 2020 dollars.
* Computed weighted variance of log wages and Gini coefficients for Total Income, After-Tax Income, and Wages.
* Grouped the workforce into discrete demographic cells (Gender × Education × Experience) to compute composition-corrected mean log wages.

### Key Findings
* **The "Demographic Illusion":** Naive wage growth consistently overstates true wage growth because the Canadian workforce became significantly older and more educated over the sample period. 
* **Real Wage Stagnation:** By holding demographics constant, composition-adjusted wages reveal much smaller "true" wage gains and expose severe real wage stagnation for high-school graduates.

---

## 📈 Project 2: Human Capital & Mincer Earnings Functions
**File:** `hw3_script.py`

This project models the determinants of wages using Mincer regressions to isolate how the labor market's valuation of schooling and experience has changed.

### Methodology
* Engineered features for "Years of Schooling" and "Potential Experience" based on historical educational attainment codes.
* Fit multiple Weighted Least Squares (WLS) models to estimate the marginal returns to human capital.
* Conducted variance decomposition to isolate the "explained" vs. "unexplained" components of rising wage inequality.
* Extended models with robust controls, including gender dummies, marital status, geographic fixed effects (provinces), and industry codes.

### Key Findings
* **Rising Premium for Education:** The wage premium for an additional year of education increased from 8.4% in 1982 to roughly 9.95% in 2018.
* **The Role of Unobserved Factors:** Despite rising returns to human capital, the basic Mincer model explains very little of overall wage inequality. Unobserved factors (the regression residuals) account for approximately 90% of total wage variance across all decades.
* **Geography Matters:** Adding geographic fixed effects drastically improves model fit. Local labor market conditions, such as the resource boom in Alberta (which showed a massive 12.4% to 13.2% wage advantage in later decades), explain a substantial portion of Canadian wage inequality beyond basic education and experience.
