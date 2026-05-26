# Income Distribution Analysis in Canada (1982–2018)

This repository contains applied econometrics and data analysis projects focusing on the evolution of wage inequality in Canada. The analysis is based on microdata from the Survey of Consumer Finances (1982, 1990) and the Canadian Income Survey (2016, 2018). 

The scripts process large-scale survey data, apply statistical rigor, and model complex systems to understand the underlying drivers of income disparity over a 36-year period.

## 🛠 Technologies & Libraries
* **Language:** Python
* **Data Manipulation:** `pandas`, `numpy`
* **Econometrics & Modeling:** `statsmodels` (WLS regressions, Variance Inflation Factor)
* **Visualization:** `matplotlib`

---

## 📊 Project 1: Wage Inequality Trends & Composition-Adjusted Wages
**File:** `hw2_script.py`

[cite_start]This project quantifies the evolution of Canadian wage inequality and applies the Autor, Katz, and Kearney (AKK) methodology to control for shifting labor force demographics[cite: 631, 651, 652, 653, 654, 655, 656, 657, 658, 659, 660, 661, 662, 663, 664, 665, 666, 667, 668, 669, 670, 671, 672, 673, 674, 675, 676, 677, 678, 679, 680, 681, 682, 683, 684, 685, 686, 687, 688].

### Methodology
* [cite_start]Cleaned and standardized hourly wage data across four distinct survey decades, adjusting for inflation (CPI) to calculate real wages in 2020 dollars[cite: 441, 442, 443, 444, 445, 446, 447, 448, 449, 450, 451, 452, 453, 454, 455, 456, 457, 458].
* [cite_start]Computed weighted variance of log wages and Gini coefficients for Total Income, After-Tax Income, and Wages[cite: 512, 513, 514, 536].
* [cite_start]Grouped the workforce into discrete demographic cells (Gender × Education × Experience) to compute composition-corrected mean log wages[cite: 636, 667, 668, 669, 670, 671, 672, 673, 674, 675].

### Key Findings
* [cite_start]**The "Demographic Illusion":** Naive wage growth consistently overstates true wage growth because the Canadian workforce became significantly older and more educated over the sample period[cite: 690]. 
* [cite_start]**Real Wage Stagnation:** By holding demographics constant, composition-adjusted wages reveal much smaller "true" wage gains and expose severe real wage stagnation for high-school graduates[cite: 691, 692].

---

## 📈 Project 2: Human Capital & Mincer Earnings Functions
**File:** `hw3_script.py`

[cite_start]This project models the determinants of wages using Mincer regressions to isolate how the labor market's valuation of schooling and experience has changed[cite: 174, 175, 176, 177, 178, 179, 180, 181, 182, 183, 184, 185, 186, 187, 188, 189, 190, 191, 192, 193, 194, 195, 196, 197, 198, 199, 200, 201, 202, 203, 204, 205, 206, 207, 208, 209, 210, 211, 212, 213, 214, 215, 216, 217, 218, 219].

### Methodology
* [cite_start]Engineered features for "Years of Schooling" and "Potential Experience" based on historical educational attainment codes[cite: 152, 153, 154, 155, 156, 157, 158, 159, 160, 161, 162, 163, 164].
* [cite_start]Fit multiple Weighted Least Squares (WLS) models to estimate the marginal returns to human capital[cite: 183, 229, 251, 318].
* [cite_start]Conducted variance decomposition to isolate the "explained" vs. "unexplained" components of rising wage inequality[cite: 288, 289, 290, 345].
* [cite_start]Extended models with robust controls, including gender dummies, marital status, geographic fixed effects (provinces), and industry codes[cite: 396, 397, 398, 399, 400, 401, 402, 403, 404, 405, 406, 407, 408, 409, 410, 411].

### Key Findings
* [cite_start]**Rising Premium for Education:** The wage premium for an additional year of education increased from 8.4% in 1982 to roughly 9.95% in 2018[cite: 193, 206, 215].
* **The Role of Unobserved Factors:** Despite rising returns to human capital, the basic Mincer model explains very little of overall wage inequality. [cite_start]Unobserved factors (the regression residuals) account for approximately 90% of total wage variance across all decades[cite: 375].
* **Geography Matters:** Adding geographic fixed effects drastically improves model fit. [cite_start]Local labor market conditions, such as the resource boom in Alberta (which showed a massive 12.4% to 13.2% wage advantage in later decades), explain a substantial portion of Canadian wage inequality beyond basic education and experience[cite: 404, 406].
