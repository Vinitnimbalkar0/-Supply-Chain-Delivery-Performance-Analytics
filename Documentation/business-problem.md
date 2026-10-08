# Supply Chain & Delivery Performance Analytics

## Business Problem

Management wants to improve order fulfillment and delivery performance while protecting revenue and profitability.

The analysis answers:

> **What operational factors are associated with delivery delays, where is the business most exposed, and which areas should management prioritize?**

## Key Business Questions

1. What is the overall delivery-performance level?
2. Which shipping modes have the highest late-delivery rates?
3. Are delivery problems concentrated in particular markets or regions?
4. Which products or categories show elevated delivery risk?
5. Do customer segments or order characteristics differ in delivery performance?
6. Is delivery performance changing over time?
7. Which areas have the greatest revenue exposure to delivery risk?
8. How does delivery performance compare with profitability?
9. Where should management investigate first?

## Data Grain

The dataset is at the **order-line/item level**. Repeated `Order Id` values are therefore not automatically duplicates.

Order-level KPIs should use distinct `Order Id`.

## Analytical Framework

```text
Business Problem
      ↓
Data Quality
      ↓
KPI Analysis
      ↓
Segmentation
      ↓
Root Cause Analysis
      ↓
Trend Analysis
      ↓
Financial Impact
      ↓
Risk × Business Impact
      ↓
Recommendations
```

## Expected Business Outcome

The analysis is designed to identify high-risk shipping modes, understand geographic variation, quantify revenue exposure associated with late deliveries, and prioritize operational investigations.

## Important Limitation

The dataset is observational. Observed relationships are treated as **associations, not proof of causation**.
