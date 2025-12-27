# country-newness-vs-corruption
Exploring the relationship between country age, GDP, and corruption


# Governance, GDP, and Corruption

This project explores whether a country's age (years since independence) is associated with corruption outcomes.

## Motivation
My hypothesis was that "newness" of country or the years since independence of the country influences corruption level in that country.
I used dataset from Transparency International and World Economic Outlook.

## Data
- Corruption Perceptions Index (CPI 2024)
- World Bank GDP per capita
- Country independence years

## Methodology
- Exploratory data analysis
- Correlation analysis (Pearson & Spearman)
- Linear regression: CPI ~ log(GDP)
- Residual analysis to identify governance performance beyond wealth

## Key Findings
- Years since independence shows no meaningful correlation with corruption
- GDP per capita is strongly associated with corruption outcomes
- Residual analysis reveals countries that over- and under-perform
  in governance relative to economic development

## Limitations
This analysis is correlational and cross-sectional.
No causal claims are made.

## Notebook
See `analysis.ipynb` for full code and results.
