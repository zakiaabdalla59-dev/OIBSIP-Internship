# Task 2: Unemployment Analysis with Python

## 📌 Overview
Unemployment is a key socio-economic indicator. This project performs an in-depth exploratory data analysis (EDA) of the **Unemployment Rate in India** covering regional (state-level), sectoral (rural vs urban), and temporal (2019-2020) trends, specifically evaluating the impact of the **COVID-19 pandemic**.

---

## 📂 Files Included
- `Unemployment_Analysis.ipynb`: Fully executed Jupyter Notebook containing data cleaning, time-series line charts, bar plots, correlation heatmaps, and written observations.
- `Unemployment_in_India.csv`: Clean, representative dataset covering 28 Indian regions across Rural & Urban areas.
- `README.md`: Task documentation and summary of economic findings.

---

## 🔬 Analysis Methodology
1. **Data Cleaning & Preprocessing**:
   - Column header space trimming.
   - String value normalization across regions and areas.
   - Date parsing into standard datetime object (`Year`, `Month`, `Month_Year`).
   - Missing value identification and removal (14 null records dropped).
2. **Exploratory Data Analysis (EDA)**:
   - Time-series line chart tracking major state trends before and after lockdown (March 2020).
   - Ranking top 10 states by average unemployment rate.
   - Heatmap analysis of correlation between Unemployment Rate, Employed Count, and Labour Participation Rate (LPR).
   - Boxplot analysis comparing Rural vs Urban unemployment distribution.
3. **Pre-COVID vs. Post-COVID Comparison**:
   - Partitioned dataset into Pre-COVID (Jan 2019 – Feb 2020) and Post-COVID (Mar 2020 – Nov 2020).
   - Calculated mean percentage increase across regions.

---

## 📊 Summary of Findings

| Metric / Dimension | Pre-COVID Era (Jan 2019 - Feb 2020) | Post-COVID Era (Mar 2020 - Nov 2020) | Key Impact |
|---|---|---|---|
| **Peak Unemployment Rate** | ~12.5% | **> 35% - 40%** | Massive spike during April-May 2020 lockdown |
| **Urban vs. Rural Median** | Urban: ~9.2% | Urban: ~16.8% | Urban sector suffered higher employment volatility |
| **Top Affected Regions** | Puducherry, Tripura | Puducherry, Jharkhand, Delhi, Bihar | Severe industrial & service sector slowdown |

---

## 💡 Key Written Insights
- **Lockdown Impact:** A dramatic, immediate rise in unemployment occurred in April 2020 following nationwide physical movement restrictions.
- **Correlation:** Strong negative correlation exists between the estimated number of employed workers and the unemployment rate percentage.
- **Recovery:** A multi-month gradual economic recovery began around July 2020 as lockdown measures eased.

---
*Completed for Oasis Infobyte Data Science Internship (OIBSIP)*
