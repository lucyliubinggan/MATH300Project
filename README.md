# MATH300Project  
## Discovering Non-linearity in Stock Fundamental Factors  
### MA300 – Mathematics of Data Science | Emory University  
**Team Members:**  
- Eric Zhang (eric.zhang@emory.edu)  
- Lucy Liu (lucy.liu@emory.edu)  

---

## 1. Problem Description and Research Motivation

Factor investing has been a cornerstone of empirical asset pricing for decades. Classical fundamental factors—such as year-over-year growth, leverage ratios, or profitability metrics—are often modeled under *linear* assumptions. In practice, however, financial ratios frequently exhibit nonlinear dynamics due to market regimes, reporting frequency, scaling effects, and investor behavior.

This project aims to investigate:

**To what extent do nonlinear structures exist among commonly used fundamental factors in the Chinese A-share market, and does modeling such nonlinearities improve predictive power for future stock returns?**

We study seven fundamental factors constructed from historical corporate financial data and evaluate whether nonlinear modeling (deep learning, decision trees, boosting methods) yields measurable improvements over the traditional linear baseline.

---

## 2. Dataset Description

- **Dataset name:** A-Share Fundamental Data  
- **Size:** Approx. 8 million samples, 7 features  
- **Factors included:**  
  - `cfo2cl` (Operating Cash Flow / Current Liabilities)  
  - `dta2ev` (Debt to Enterprise Value)  
  - `NNP_SD` (Net Profit Standard Deviation)  
  - `ocfa4q` (Operating Cash Flow – Annualized)  
  - `r_nta` (Return / Net Tangible Assets)  
  - `roic4q` (Return on Invested Capital – 4Q)  
  - `yoy_s` (Year-over-Year Sales Growth)

**Important limitation:**  
Financial statement data is reported quarterly. Many observations remain constant for long stretches, requiring careful feature engineering to avoid bias in modeling.

The merged and preprocessed factor dataset used for exploratory analysis is stored in:data/merged_factors.ft

