# Does Country Age Explain Corruption?
### A Data-Driven Study of Independence, Wealth, and Governance Quality

## Overview
This project examines whether years since independence provide meaningful explanatory power for corruption outcomes when compared with economic and institutional factors.

Rather than optimizing for prediction, the focus is on **hypothesis testing, feature relevance, and interpretability** — following the data even when it contradicts intuition.

---

## Research Hypothesis
**The level of corruption in a country is related to the number of years since its independence.**

### Definitions
- **Country age** → Years since independence  
- **Corruption / governance quality** → CPI 2024 and multiple independent institutional indices

---

## Data Sources
The analysis combines several globally recognized datasets capturing different dimensions of governance:

- Corruption Perceptions Index (CPI 2024)
- Economist Intelligence Unit Country Ratings
- Freedom House – Nations in Transit
- S&P / Global Insights Country Risk Ratings
- IMD World Competitiveness Yearbook
- PERC Asia Risk Guide
- PRS International Country Risk Guide
- Varieties of Democracy Project
- World Economic Forum Executive Opinion Survey
- World Justice Project Rule of Law Index
- World Bank GDP (USD)

Using multiple indices ensures that results are not driven by any single measurement framework.

---

## Methodology
The analysis proceeds in structured stages:

1. **Exploratory correlation analysis**  
   - Pearson and Spearman correlations between years since independence and each corruption / governance index

2. **Regional analysis**  
   - Examination of geographic and historical clustering effects

3. **Economic comparison**  
   - Relationship between GDP, country age, and governance outcomes

4. **Regression & residual analysis**  
   - Model specification: `CPI ~ log(GDP)`
   - Residuals interpreted as *governance performance beyond economic capacity*

---

## Key Findings

### 1. Country Age Has Very Weak Explanatory Power
Across all corruption and governance indices:
- Years since independence shows **consistently weak correlation**
- The strongest observed relationship is modest (≈ **0.27**, Economist Intelligence Unit)

**Conclusion:**  
> Time since independence alone is not a meaningful driver of corruption outcomes.

---

### 2. Governance Indicators Are Internally Consistent, Country Age Is Not
A correlation heatmap of all numerical indicators shows:

- Strong correlations among corruption and governance indices (≈ 0.75–0.95)
- Consistently weak correlation between **years since independence** and all governance measures

This confirms that:
- The indices capture a common latent concept of governance quality
- Country age contributes little independent explanatory signal

*(See correlation heatmap in the notebook for details.)*

---

### 3. Regional Effects Dominate Country Age
Governance outcomes cluster strongly by region:
- Countries of similar age often exhibit vastly different corruption levels
- Shared historical and institutional contexts explain far more variance than elapsed time

This indicates that **institutional trajectories matter more than chronology**.

---

### 4. GDP Is Strongly Associated with Governance Quality
GDP (log-transformed) shows **strong correlation** with corruption and governance measures across all indices.

However:
- Countries with similar income levels still display large governance differences
- Economic development explains much — but not everything

---

## Governance Performance Beyond Economic Capacity

Governance Performance Beyond Economic Capacity

To examine governance variation unexplained by income, a linear regression model is estimated:

CPI ~ log(GDP)


The residuals from this model represent deviations from the corruption level expected given a country’s economic capacity.

Positive residuals → stronger governance than GDP predicts

Negative residuals → weaker governance than GDP predicts

Residuals are interpreted as relative performance, not causal effects.

Overperforming Countries

(Higher CPI than Expected Given GDP)

These countries exhibit substantially better governance outcomes than predicted by their level of economic development, suggesting comparatively strong institutional effectiveness relative to economic capacity.

Country	CPI 2024	Predicted CPI	Residual
Bhutan	72	36.79	+35.21
Rwanda	57	23.25	+33.75
Finland	88	63.18	+24.82
Denmark	90	66.12	+23.88
Uruguay	76	54.77	+21.23
New Zealand	83	62.30	+20.70
Burkina Faso	41	22.79	+18.21
Estonia	76	57.84	+18.16
Benin	45	26.95	+18.05
Malawi	34	16.06	+17.94

These cases highlight that strong governance outcomes are achievable even at lower or mid-range income levels.

Underperforming Countries

(Lower CPI than Expected Given GDP)

These countries exhibit weaker governance outcomes than predicted by GDP, indicating institutional challenges relative to economic capacity.

Country	CPI 2024	Predicted CPI	Residual
Equatorial Guinea	13	44.04	−31.04
Turkmenistan	17	46.66	−29.66
Libya	13	42.64	−29.64
Venezuela	10	38.20	−28.20
Mexico	26	49.69	−23.69
Azerbaijan	22	43.01	−21.01
Panama	33	52.85	−19.85
Nicaragua	14	33.54	−19.54
Guyana	39	57.69	−18.69
Gabon	27	45.48	−18.48

A recurring pattern among underperformers includes reliance on resource rents, weak accountability mechanisms, or institutional instability.

---

## Impact & Interpretation
This analysis demonstrates that:
- Corruption is **not a simple function of country age**
- Economic development is a powerful baseline predictor
- Institutional quality varies substantially even among countries with similar GDP

**Key insight:**  
> Governance outcomes reflect institutional design, political incentives, and accountability mechanisms — not merely time or income.

---

## Limitations
- Cross-sectional snapshot
- Correlational analysis
- Measurement uncertainty across indices

Residuals are interpreted as *relative performance*, not causal effects.

---

## Repository Structure
- `Corruption_Index.ipynb` — full exploratory analysis, modeling, visualizations, and heatmaps  
- `data/` — cleaned datasets used in the study  
- `README.md` — project summary and findings  

---

## Author
Independent data analysis project exploring the intersection of governance, economics, and institutional quality.
