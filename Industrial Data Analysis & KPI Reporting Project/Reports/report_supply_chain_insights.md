# Supply Chain Health & Risk Analysis – Final Insights Report
Wael Aboulkacem
Tools used: Python (Pandas, NumPy), Power BI
Dataset:  Supply Chain Analysis, an online csv file from Kaggle: https://www.kaggle.com/datasets/harshsingh2209/supply-chain-analysis 

## 1. Project Overview

#### This project analyzes the supply chain performance of a makeup/beauty product company.
#### The goal was to:

- Assess inventory health

- Monitor demand pressure

- Evaluate lead-time risks

- Measure quality performance

- Identify high-risk products and suppliers

- Create a business-ready dashboard in Power BI

A full KPI framework was built using Python, and a final interactive dashboard was created in Power BI.

## 2. Dataset Summary

#### The dataset covers several areas of the supply chain:

- Inventory levels
- Sales & demand
- Revenue
- Production & manufacturing
- Shipping & logistics
- Supplier performance
- Inspection & quality results
- Costs (manufacturing, shipping, etc.)
- A total of 100 unique SKUs were included.

## 3. KPI Framework

#### The following key KPIs were calculated:

- Inventory & Demand
- Stock Coverage Ratio (SCR)
- Stock-Out Flag
- Demand Pressure Index (DPI)
- Lead Time Risk
- Average Total Lead Time
- Manufacturing Lead Time Share
- Long Lead Time Flag
- Cost Performance
- Cost per Unit Sold
- Shipping Cost Intensity
- Cost per Revenue Percentage
- Quality
- Inspection Failure Rate
- Defect Rates
- Quality Cost Exposure

These KPIs were calculated in Python, exported as a structured dataset, and visualized in Power BI.

## 4. Key Findings & Insights
#### 4.1 Inventory Health

Average Stock Coverage Ratio was low, meaning many products risk stocking out.
1 product (1%) was already in stock-out, but several others showed very low coverage, signaling future issues.
The scatter plot showed high-demand products often had low inventory, which is a critical risk.

#####  Recommendation:

Increase safety stock for SKUs with high demand pressure and low coverage.
#### 4.2 Demand Pressure

The Demand Pressure Index(DPI) displayed a wide distribution.
Several items showed high DPI values, indicating risk of future shortages.

##### Recommendation:

Improve forecasting for products with high DPI variability.

#### 4.3 Lead Time Performance

Average total lead time ≈ 12.16 days
45% of products had long lead times (flag = 1)
Manufacturing lead time represented over 50% of total lead time for most items → bottleneck in production.

##### Recommendation:

Review supplier lead time reliability and production capacity constraints.

#### 4.4 Cost Analysis

Cost per revenue was low across products, meaning profitability is generally stable.
Shipping cost intensity varied significantly by product type and supplier.

##### Recommendation:

Optimize shipping modes and consolidate shipments for high-cost suppliers.

#### 4.5 Quality & Inspection

Inspection Results:
Pending: 41%
Fail: 36%
Pass: 23%

This means:
- More than one-third of products fail inspection.
- Almost half are stuck in pending state → delays and uncertainty.

##### Recommendation:

Work with suppliers with high fail rates, and improve quality checks upstream.

## 5. Power BI Dashboard Summary

The dashboard includes:

Inventory & Demand Visuals
- Stock Coverage distribution
- Demand Pressure distribution
- Stock vs Demand scatter plot

Lead Time Visuals
- Long lead time distribution
- Lead time per supplier

Quality & Cost Visuals
- Inspection results
- Defect rate distribution
- Quality cost exposure

The dashboard allows filtering by:
- Product Type
- Supplier
- SKU

## 6. Business Recommendations
#### Inventory & Demand
Increase safety stock for unstable high-demand items
Improve forecasting accuracy using DPI patterns

#### Lead Time
Collaborate with suppliers to reduce long lead times
Investigate high manufacturing lead time processes

#### Cost
Optimize shipping routes
Implement cost benchmarking between suppliers

#### Quality
Address high defect-rate suppliers
Reduce pending inspections and enforce faster approvals

## 7. Conclusion

This analysis uncovered clear supply chain risks in inventory levels, lead time reliability, and inspection performance.
