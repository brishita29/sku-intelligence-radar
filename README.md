# sku-intelligence-radar
**Predictive Funnel Leak Detection & Profit Recovery Engine for E-commerce Merchandising**

---

## Overview

**The SKU Intelligence Radar** is a full-stack decision support system built to help merchandising and pricing teams identify underperforming SKUs with hidden profit erosion. Based on raw user interaction data (views, carts, purchases), the project isolates high-traffic, low-conversion products, estimates potential financial recovery, and recommends data-backed actions at the SKU level.

Developed using a combination of **SQL (DuckDB)** for data transformation, **Python** for analysis and modeling, **A/B testing** for behavioral validation, and **Tableau** for executive visualization, the system delivers a structured pipeline from data to strategic recommendation.

---

## Project Goal  
To detect SKU-level margin loss, simulate realistic uplift scenarios, and produce prioritized, confidence-weighted SKU actions to support merchandising strategy.

---

## Pipeline Overview

- **Funnel Construction**: Traced SKU-level view → cart → purchase paths to identify conversion drop-offs
- **Margin Simulation**: Estimated cost and price to compute gross margin at SKU level
- **Erosion Flagging**: Tagged high-traffic, low-conversion, high-margin SKUs using threshold logic
- **Recovery Forecasting**: Simulated recoverable margin under benchmark and uplift scenarios
- **Action Logic**: Assigned Kill / Cut Promo / Keep based on confidence-weighted scores and urgency
- **Lifecycle & Risk Classification**: Labeled SKUs by maturity (early/growth/decline) and flagged removal risk
- **Predictive Modeling**: Used XGBoost, Logistic Regression, and Gradient Boosting to predict erosion likelihood and recovery potential
- **A/B Behavioral Testing**:  
  - Segmented users into Group A (buyers) and Group B (non-buyers)  
  - Applied **Chi-square test** for conversion rate differences  
  - Used **Mann-Whitney U test** to compare engagement distributions  
  - Aimed to validate whether observed funnel behavior differed statistically across user types  
- **Final Deliverables**:
  - Master SKU Strategy Sheet (CSV)
  - Recovery scorecards with confidence and lifecycle labels
  - **Tableau Dashboard** summarizing SKU priorities, category-level risk, and actionable filters

---

## Outcome

The result is a production-ready analytics solution that mirrors real-world merchandising workflows. It unifies behavioral analysis, financial modeling, risk forecasting, and strategy simulation into one decision-making layer. This system enables merchandising and pricing teams to act on high-impact SKU opportunities with clarity, speed, and confidence.


---

## Tools & Technologies

- **Python** (Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn)
- **SQL via DuckDB** (in-memory querying on large CSV files)
- **XGBoost & Logistic Regression**
- **Tableau** (for dashboard visualization)
- **Data**: Kaggle RetailRocket Events Dataset

---

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

---

## How to Run

1. Install requirements: pip install pandas duckdb xgboost scikit-learn matplotlib seaborn
2. Run the notebook SKU_Intelligence_Radar.ipynb step by step
3. Output CSVs and strategy sheets will be saved in the working directory

---

## Business Value

This project simulates a real merchandising analytics pipeline — turning millions of raw events into actionable SKU decisions. Ideal for e-commerce teams looking to reduce churn, improve profit margins, and optimize product-level performance.

---

## Author

**Rishita Boddu**  
