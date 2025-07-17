# sku-intelligence-radar
**Predictive Funnel Leak Detection & Profit Recovery Engine for E-commerce Merchandising**

## Overview

This project builds a full-funnel intelligence engine for an e-commerce/DTC retailer to detect conversion leaks, simulate lost profit, and prioritize SKUs based on potential recovery value.It blends funnel analytics, statistical testing, and decision strategy into a practical tool for merchandising teams.

## Project Goal  
To detect SKU-level margin loss, simulate realistic uplift scenarios, and produce prioritized, confidence-weighted SKU actions to support merchandising strategy.

## Business Problem
In most retail businesses, high-traffic SKUs don’t always convert well — leading to invisible revenue leaks and missed profit opportunities.

This project answers:

Which SKUs are leaking the most money due to funnel drop-offs?

Which ones are worth fixing?

How confident are we that the fixes will work?

What would be the uplift if we fix them?

## Pipeline Overview

- Funnel Construction: Traced SKU-level view → cart → purchase paths to identify conversion drop-offs
- Margin Simulation: Estimated cost and price to compute gross margin at SKU level
- Erosion Flagging: Tagged high-traffic, low-conversion, high-margin SKUs using threshold logic
- Recovery Forecasting: Simulated recoverable margin under benchmark and uplift scenarios
- Action Logic: Assigned Kill / Cut Promo / Keep based on confidence-weighted scores and urgency
- Lifecycle & Risk Classification: Labeled SKUs by maturity (early/growth/decline) and flagged removal risk
- Predictive Modeling: Used XGBoost, Logistic Regression, and Gradient Boosting to predict erosion likelihood and recovery potential
- A/B Behavioral Testing:  
  - Segmented users into Group A (buyers) and Group B (non-buyers)  
  - Applied Chi-square test for conversion rate differences  
  - Used Mann-Whitney U test to compare engagement distributions  
  - Aimed to validate whether observed funnel behavior differed statistically across user types  
- Final Deliverables:
  - Master SKU Strategy Sheet (CSV)
  - Recovery scorecards with confidence and lifecycle labels
  - Tableau Dashboard summarizing SKU priorities, category-level risk, and actionable filters

## Tools & Techniques
SQL – for funnel logic, grouping, and transformation

Python – for statistical tests, uplift simulation, priority scoring

Pandas / NumPy / Scipy / Statsmodels – modeling and analysis

Tableau – interactive executive dashboard

Business logic layers – Erosion type classification, Clean Action flags, Strategic recommendations

## Files in This Repository

| File | Description |
|------|-------------|
| SKU_Intelligence_Radar.ipynb | Full notebook with all 75+ steps |
| final_strategy_master_sheet.csv | Final strategy table for stakeholder use |
| profit_erosion_sku_analysis.csv | Core erosion tagging & funnel metrics |
| uplift_final.csv | Uplift simulations under multiple recovery scenarios |
| Tableau Dashboard.png | Visual summary of SKU recovery, erosion flags, confidence scores, and category-wise impact|

### View Full Tableau Dashboard
([https://public.tableau.com/app/profile/rishita.boddu/viz/ProfitLeakageRecoveryMap/Dashboard3])
> - Top priority SKUs by adjusted recovery
> - Erosion risk flags and removal risk
> - Recommended actions: Kill, Cut Promo, Keep
> - Category-wise impact analysis
> - Confidence & lifecycle filters

## How to Run

1. Install requirements: pip install pandas duckdb xgboost scikit-learn matplotlib seaborn
2. Run the notebook SKU_Intelligence_Radar.ipynb step by step
3. Output CSVs and strategy sheets will be saved in the working directory

## Business Value

Helped identify high-potential SKU recoveries worth up to 5–10% of total category margin loss.
Enabled merchandising and pricing teams to focus on SKUs with both financial upside and high statistical confidence, avoiding wasted effort.

## Author

Rishita Boddu
