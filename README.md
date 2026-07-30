"""# Retail Sales Analysis & Price Elasticity Case Study

An end-to-end data analysis project assessing daily retail store trading performance, unit pricing dynamics, profitability metrics, and Price Elasticity of Demand (PED) for key promotional periods.

---

## 📌 Project Overview

This project analyzes aggregated daily trading data for a key retail product. The objective is to derive operational and strategic insights regarding daily pricing, gross profit margins, demand sensitivity to promotional pricing, and long-term sales performance.

### Key Objectives
1. **Daily Unit Pricing**: Calculate the daily realized sales price per unit.
2. **Average Unit Price**: Determine the overall baseline average selling price across the trading history.
3. **Profitability Analysis**: Derive daily Gross Profit percentage ($\\% GP$) and assess unit-level margin efficiency.
4. **Promotional & Elasticity Analysis**: Identify 3 distinct promotional windows and compute the **Price Elasticity of Demand (PED)** to determine if promotional discounting drives volume/revenue growth or margin erosion.
5. **Strategic Insights & Recommendations**: Provide actionable data-backed business insights for inventory, dynamic pricing, and promotional planning.

---

## 📊 Summary of Key Findings & Metrics

| Metric / Dimension | Value / Finding | Business Context |
| :--- | :--- | :--- |
| **Average Unit Selling Price** | $R_{Avg} = \frac{\sum \text{Sales}}{\sum \text{Quantity Sold}}$ | Evaluated across the complete dataset timeframe |
| **Daily Gross Profit %** | $GP\% = \frac{\text{Sales} - \text{Cost of Sales}}{\text{Sales}} \times 100$ | Evaluates store-level daily gross margin performance |
| **Daily Unit GP %** | $\frac{\text{Price/Unit} - \text{Cost/Unit}}{\text{Price/Unit}} \times 100$ | Verifies consistency of margin across varying order sizes |
| **Promotional Elasticity** | Analyzed across 3 Promo Windows | Evaluates volume responsiveness ($\% \Delta Q / \% \Delta P$) |

---

## 🔬 Methodology & Formulations

### 1. Pricing & Profitability Equations
* **Daily Sales Price per Unit**:
  $$P_{daily} = \frac{\text{Sales}}{\text{Quantity Sold}}$$

* **Daily Gross Profit Margin (%)**:
  $$GP\% = \frac{\text{Sales} - \text{Cost of Sales}}{\text{Sales}} \times 100$$

* **Unit Gross Profit Margin (%)**:
  $$\text{Unit } GP\% = \frac{P_{daily} - \text{Unit Cost}}{P_{daily}} \times 100$$

### 2. Price Elasticity of Demand (PED)
For each identified promotional period relative to a pre-promo baseline period:
$$PED = \frac{\% \Delta Q}{\% \Delta P} = \frac{(Q_1 - Q_0) / Q_0}{(P_1 - P_0) / P_0}$$

* **Interpretation Guide**:
  * $\vert{}PED\vert{} > 1$: Elastic (Volume growth outpaces price cuts — promo is effective).
  * $\vert{}PED\vert{} < 1$: Inelastic (Volume gain does not offset price drop — margin erosion).
  * $\vert{}PED\vert{} = 1$: Unitary Elasticity.

---
[Click to View interactive Sales Performance Dashboard](https://profit-palooza-17.lovable.app)

## 📁 Repository Structure

```text
├── data/
│   └── Sales Case Study.xlsx       # Raw daily trading dataset
├── notebooks/
│   └── sales_analysis.ipynb        # Exploratory Data Analysis & Elasticity models
├── scripts/
│   ├── calculate_metrics.py        # Core transformation & KPI functions
│   └── visualize_trends.py         # Dashboard & chart generation script
├── outputs/
│   ├── figures/                    # Exported visuals & dashboard components
│   └── summary_report.pdf          # Final presentation of analytical findings
├── README.md                       # Project documentation
└── requirements.txt                # Python environment dependencies


