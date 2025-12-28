# Does Country Age Explain Corruption?
### A Data-Driven Study of Independence, Wealth, and Governance Quality

## Overview
A common intuition is that countries with shorter post-independence histories may face greater challenges in building effective institutions.
This project empirically tests that assumption using global corruption, governance, and economic data.

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
   - Linear regression model: [ CPI ~ log(GDP) ]
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

### 2. Regional Effects Dominate Country Age
Governance outcomes cluster strongly by region:
- Countries of similar age often exhibit vastly different corruption levels
- Shared historical and institutional contexts explain far more variance than elapsed time

This indicates that **institutional trajectories matter more than chronology**.

---

### 3. GDP Is Strongly Associated with Governance Quality
GDP (log-transformed) shows **strong correlation** with corruption and governance measures across all indices.

However:
- Countries with similar income levels still display large governance differences
- Economic development explains much — but not everything

---

### 4. Residual Analysis Reveals Governance Efficiency
Residuals from the model:

\[
\text{CPI} \sim \log(\text{GDP})
\]

highlight:
- **Overperforming countries** with stronger governance than GDP predicts
- **Underperforming countries** with weak institutions despite economic capacity

These residuals capture **institutional effectiveness beyond wealth**.

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
- `Corruption_Index.ipynb` — full exploratory analysis, modeling, and visualizations
- `data/` — cleaned datasets used in the study
- `README.md` — project summary and findings

---

## Author
Independent data analysis project exploring the intersection of governance, economics, and institutional quality.
