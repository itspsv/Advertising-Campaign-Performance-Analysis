# Advertising Campaign Performance Analysis  
### **Facebook vs AdWords – Clicks, Conversions & Cost-Effectiveness**

This project analyzes and compares the performance of **Facebook** and **AdWords** ad campaigns using daily data from 2019.  
The aim is to identify which platform delivers better **clicks**, **conversions**, and **overall cost efficiency**, enabling optimized marketing strategies.

---

## Project Objectives
- Compare campaign performance based on clicks, conversions, and cost.  
- Measure the relationship between clicks and conversions.  
- Conduct hypothesis testing to validate platform performance differences.  
- Build a regression model to predict Facebook conversions.  
- Analyze weekly/monthly trends in conversions.  
- Study long-term equilibrium via cointegration.

---

## Dataset Description
- **365 daily records** (Jan–Dec 2019)
- Includes metrics for both **Facebook** and **AdWords** campaigns.

### Key Features:
- `Date`  
- `Ad Views`  
- `Ad Clicks`  
- `Ad Conversions`  
- `Cost per Ad`  
- `CTR (Clicks / View)`  
- `Conversion Rate (Conversions / Click)`  
- `Cost per Click`

---

## Technologies Used
- Python  
- Pandas, NumPy  
- Matplotlib, Seaborn  
- SciPy  
- scikit-learn  
- statsmodels  

---

## Data Cleaning
- Converted date to datetime  
- Removed `%` and `$` symbols from metrics  
- Converted CTR, conversion rate, CPC & cost to numeric values  

---

## Exploratory Data Analysis (EDA)

### Distribution Analysis
- Facebook shows **more high-conversion days** than AdWords.  
- AdWords conversions mostly fall below 10 per day.

### Conversion Categories
Conversions grouped as: `<6`, `6–10`, `10–15`, `>15`

Facebook dominates the higher ranges.

### Clicks vs Conversions Correlation
| Platform | Correlation |
|----------|-------------|
| **Facebook** | **0.87 (strong)** |
| **AdWords** | **0.45 (moderate)** |

More Facebook clicks → more conversions.

---

## Hypothesis Testing

**H₀:** Facebook conversions ≤ AdWords conversions  
**H₁:** Facebook conversions > AdWords conversions  

- **Mean Facebook conversions:** 11.74  
- **Mean AdWords conversions:** 5.98  
- **p-value:** 9.35e−134 → **Reject H₀**

**Facebook produces significantly more conversions.**

---

## Linear Regression (Facebook)

**Model:** Conversions ~ Clicks  
- **R² Score:** 76.35%  
- Strong predictive ability  

Example predictions:  
- 50 clicks → ~9.66 conversions  
- 80 clicks → ~14.24 conversions  

---

## Time-Series Analysis (Facebook Only)

### Weekly Trends
- Conversions highest on **Monday & Tuesday**  
- Engagement consistent across days

### Monthly Trends
- Overall upward trend  
- Dip in Feb, Apr, May, Jun, Aug, Nov

### Cost Per Conversion (CPC)
- **Lowest CPC:** May, November  
- **Highest CPC:** February  

---

## Cointegration Test
Checks long-term equilibrium between **Facebook Cost** and **Conversions**.

- p-value < 0.05 → **Reject null**

**Cost and conversions move together over long periods.**

---

## 🏁 Key Insights
- Facebook outperforms AdWords in almost every metric.  
- Strong link between Facebook clicks & conversions → reliable platform.  
- Hypothesis testing confirms significant conversion difference.  
- Facebook should receive a higher share of ad budget.  
- CPC varies across months → seasonal optimization possible.
