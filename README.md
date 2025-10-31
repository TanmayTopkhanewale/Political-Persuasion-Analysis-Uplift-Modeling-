# Political Persuasion Analysis: Uplift Modeling with Causal ML

This repository presents a causal machine learning analysis of voter persuasion using uplift modeling. The project estimates the incremental effect of campaign contact on voter persuasion probability and builds a data-driven targeting framework to improve outreach efficiency through causal inference and segmentation.

---

## Overview

Traditional predictive models identify who supports, not who can be persuaded.  
Uplift modeling reframes this by estimating the causal impact of campaign contact, identifying individuals most likely to change behavior when reached.

The analysis uses a validated dataset of 4,052 voter records containing demographic, community, and political attributes. Models were implemented using CausalML, Gradient Boosting, and SHAP interpretation to quantify and explain heterogeneity in persuasion outcomes.

---

## Objectives

1. Estimate individual-level uplift (treatment effect) from campaign contact.  
2. Identify features driving differential persuasion response.  
3. Evaluate multiple uplift models and select an interpretable, high-performing candidate.  
4. Translate model results into actionable targeting tiers.

---

## Methodology

**Data Preparation**
- Validated 4,052 voter entries with demographic, geographic, and political features.  
- Controlled data leakage by excluding post-treatment variables and correlated outcomes.  
- Engineered interpretable features such as marital status flags, community indicators, and registration recency.  

**Modeling**
- Implemented uplift models using CausalML (Gradient Boosting, CatBoost, LightGBM, and meta-learners).  
- Computed uplift importance and SHAP values for interpretability.  
- Compared models using AUC, precision, recall, and F1 metrics.  

**Best Model:** Gradient Boosting (AUC = 0.905) trained on top 20 causal features.

---

## Key Results

| Metric | Result |
|--------|---------|
| Positive Uplift (beneficial impact) | 98.5% of voters |
| Mean Uplift | +2.17 percentage points |
| Top Decile Uplift | +4.05% with 50.3% conversion |
| ROI Improvement | 1.6x vs. mass contact |
| Best Model | Gradient Boosting (Top 20 features) |

**Top Predictors:** marital status, community type, registration recency, and education level.

---

## Targeting Strategy

| Tier | Deciles | Priority | Recommendation |
|------|----------|-----------|----------------|
| Tier 1 | 8-9 | Highest | Focus contact and personalized messaging |
| Tier 2 | 6-7 | High | Include if budget allows |
| Tier 3 | 3-5 | Moderate | Use automated or low-frequency contact |
| Tier 4 | 0-2 | Low | Deprioritize to save resources |

Targeting the top three deciles achieved 1.6x higher conversion efficiency compared to mass outreach.

---

## Insights

- Causal ML provides actionable uplift-based segmentation, improving targeting efficiency.  
- Marital and community structure are strong predictors of persuadability.  
- Models using top 20 features balance performance, interpretability, and simplicity.

---

## Tech Stack

**Languages and Libraries:**  
Python, CausalML, scikit-learn, LightGBM, XGBoost, CatBoost, Pandas, NumPy, Matplotlib, SHAP

---

## Authors

- Tanmay Topkhanewale  
- Aditya Jain  
- Ayush Lingwal

---

## Citation

If you use this repository, please cite:  
Topkhanewale, T., Jain, A., & Lingwal, A. (2025). *Political Persuasion Campaign: Uplift Modeling Analysis.*
