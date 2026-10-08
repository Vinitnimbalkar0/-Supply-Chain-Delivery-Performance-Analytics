# Supply Chain & Delivery Performance Analytics

## Business Analytics Case Study | Excel

### 📌 Project Overview

This project analyzes supply chain and delivery performance using the **DataCo Smart Supply Chain dataset**.

The objective was to understand **what is driving delivery delays, where operational risk is concentrated, and which areas could have the greatest business impact**.

Rather than building a dashboard based only on descriptive KPIs, the analysis follows a business-driven approach:

**Business Problem → KPI Analysis → Segmentation → Root Cause Analysis → Financial Impact → Recommendations**

---

## 🎯 Business Problem

Management wants to improve order fulfillment and delivery performance while protecting revenue and profitability.

The analysis answers:

- What is the overall delivery performance?
- Which shipping modes have the highest delay rates?
- Are delays concentrated in specific markets or regions?
- Which products and customer segments show higher delivery risk?
- Is delivery performance changing over time?
- Which areas have the greatest financial exposure?
- Where should management prioritize operational improvements?

---

## 📊 Dataset

**Dataset:** DataCo Smart Supply Chain

The dataset contains approximately **71K order-line records** covering:

- Orders & order items
- Shipping and delivery performance
- Products & categories
- Customers
- Markets & regions
- Sales
- Discounts
- Profit-related metrics

> **Important:** The dataset is at an order-line level. Distinct `Order ID` is therefore used when calculating order-level KPIs.

---

# 🔎 Key Insights

### 1. Shipping Mode is the strongest observed delivery-risk signal

First Class showed an approximately **97.4% late-delivery rate**, compared with approximately **57% overall**.

Second Class also showed elevated delivery risk at approximately **79%**.

**Insight:** The delivery problem is substantially more pronounced for certain shipping modes than at the overall market level.

---

### 2. The First Class pattern persists across markets

First Class maintained a very high observed late-delivery rate across the major markets:

- Africa: ~99.3%
- Pacific Asia: ~97.8%
- Europe: ~97.3%
- USCA: ~97.3%
- LATAM: ~96.7%

**Insight:** The pattern is not isolated to one geography and requires operational investigation at the shipping-process level.

> These findings represent association, not proof of causation.

---

### 3. Geography alone does not explain the delivery problem

Market-level late-delivery rates were relatively close:

**~55.5% – 59.2%**

while shipping-mode late rates ranged from approximately:

**~38% – 97.4%**

**Insight:** Shipping-mode differences appear substantially larger than market-level differences, suggesting that geography alone does not explain the observed variation.

---

### 4. Revenue exposure should determine operational priorities

The analysis combines:

**Sales Exposure + Late Rate + Profit Margin**

rather than ranking operational problems using late rate alone.

**Insight:** A segment with a slightly lower late rate but substantially higher revenue exposure may represent a greater business priority than a small segment with an extremely high late rate.

---

### 5. Europe and LATAM have the largest sales exposure

Approximate sales:

| Market | Sales |
|---|---:|
| Europe | 4.60M |
| LATAM | 4.22M |
| Pacific Asia | 3.02M |
| USCA | 1.57M |
| Africa | 0.70M |

**Insight:** Delivery improvements in high-revenue markets could have greater business impact, provided operational risk is also elevated.

---

# 💡 Recommendations

### 1. Investigate First Class fulfillment performance

Review the First Class process across:

- Fulfillment operations
- Scheduled shipping commitments
- Warehouse processing
- Product mix
- Market/region
- Order characteristics

Do not immediately eliminate the shipping mode based only on its late rate.

---

### 2. Prioritize by Risk × Business Impact

Use a two-dimensional prioritization framework:

**High Late Rate + High Revenue Exposure → Critical Priority**

**High Late Rate + Low Revenue Exposure → Investigate / Monitor**

This prevents management from focusing only on extreme percentages.

---

### 3. Investigate high-value categories with delivery risk

Identify categories combining:

- High sales
- High order volume
- Above-baseline late rate
- Weak profitability

These categories should receive greater operational attention.

---

### 4. Evaluate discounting against profitability

Compare discount levels with:

- Sales
- Profit
- Profit Margin
- Order volume

The objective is to determine whether additional sales generated through discounts justify the associated margin reduction.

---

### 5. Monitor delivery performance over time

Track:

- Monthly late-delivery rate
- Order volume
- Shipping variance
- Sales
- Shipping-mode performance

Periods with **high demand + high late-delivery rates** should be investigated for potential capacity or fulfillment pressure.

---

# 📈 Analytical Framework

The project follows this analytical flow:

```text
Business Problem
       ↓
KPI Analysis
       ↓
Shipping Mode
       ↓
Market & Region
       ↓
Product & Customer
       ↓
Root Cause Analysis
       ↓
Time Trend Analysis
       ↓
Financial Impact
       ↓
Risk × Business Impact
       ↓
Recommendations
