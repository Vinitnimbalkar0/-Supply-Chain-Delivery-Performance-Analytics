# Supply Chain & Delivery Performance Analytics

**Business Analytics Case Study | Microsoft Excel**

> Analyzing delivery risk, financial exposure, and operational priorities using transactional supply-chain data.

---

## 1. Business Problem

Management wants to improve **order fulfillment and delivery performance** while protecting **revenue and profitability**.

The key business question was:

> **What operational factors are associated with delivery delays, where is the business most exposed, and which areas should management prioritize for improvement?**

The analysis evaluates:

- Shipping-mode performance
- Market and regional delivery risk
- Product and category performance
- Customer segments
- Delivery trends over time
- Revenue and profitability exposure
- Root-cause indicators
- Risk vs. business impact

---

## 2. Executive Summary

### 🔴 Delivery performance varies significantly by shipping mode

**First Class** recorded an observed late-delivery rate of approximately **97.4%**, compared with approximately **57% overall**.

**Second Class** also showed elevated risk at approximately **79%**.

**Implication:** The delivery problem is substantially more pronounced for certain shipping modes than at the overall market level.

---

### 🌍 Geography alone does not explain the problem

Market-level late-delivery rates were relatively close, ranging from approximately **55.5% to 59.2%**.

In contrast, shipping-mode rates ranged from approximately **38% to 97.4%**.

**Implication:** Geography alone does not explain the observed variation in delivery performance.

---

### 🚚 First Class risk persists across markets

First Class showed very high observed late-delivery rates across the five major markets:

| Market | First Class Late Rate |
|---|---:|
| Africa | ~99.3% |
| Pacific Asia | ~97.8% |
| Europe | ~97.3% |
| USCA | ~97.3% |
| LATAM | ~96.7% |

**Implication:** The pattern is not isolated to one geography and warrants operational investigation at the shipping/fulfillment process level.

> These findings represent association, not proof of causation.

---

### 💰 Financial prioritization should go beyond late rate

A high late-delivery percentage does not automatically mean the segment has the greatest business impact.

The project therefore evaluates:

**Late Rate + Sales Exposure + Profitability**

to identify areas where operational problems could affect a larger portion of the business.

---

### 🌎 Europe and LATAM represent major revenue exposure

Approximate sales:

| Market | Sales |
|---|---:|
| Europe | 4.60M |
| LATAM | 4.22M |
| Pacific Asia | 3.02M |
| USCA | 1.57M |
| Africa | 0.70M |

**Implication:** Operational improvements in high-revenue markets could have greater potential business impact, provided delivery risk is also elevated.

---

## 3. Key Insights

| ID | Insight | Business Implication |
|---|---|---|
| **01** | First Class has an observed late rate of ~97.4% | Requires immediate operational investigation |
| **02** | Second Class has ~79% late deliveries | Indicates another high-risk shipping segment |
| **03** | Market late rates are relatively narrow | Geography alone does not explain delivery variation |
| **04** | First Class risk persists across markets | Problem may be related to shipping/fulfillment processes rather than one geography |
| **05** | High revenue + high delivery risk creates greater exposure | Prioritize based on business impact, not percentage alone |
| **06** | Europe and LATAM have the largest sales exposure | Delivery improvements here could affect a larger revenue base |
| **07** | Discounting should be evaluated against profitability | Higher sales do not necessarily mean better financial performance |
| **08** | Product categories should be evaluated using both sales and delivery risk | High-value/high-risk categories deserve greater attention |

---

## 4. Recommendations

### 1. Investigate First Class fulfillment performance

Review:

- Warehouse processing
- Scheduled shipping commitments
- Product mix
- Order characteristics
- Market/region
- Operational handoffs

The recommendation is to **investigate before changing the shipping policy**, because the dataset does not establish causality.

### 2. Prioritize using Risk × Business Impact

Use:

```text
High Late Rate
       +
High Revenue Exposure
       +
Weak Profitability
       ↓
CRITICAL PRIORITY
```

This prevents management from over-prioritizing small segments with extreme percentages but limited business exposure.

### 3. Investigate high-value product categories

Focus on categories combining:

- High sales
- High order volume
- Above-baseline late rate
- Weak or declining profitability

### 4. Monitor high-demand periods

Compare:

- Monthly order volume
- Late-delivery rate
- Shipping variance
- Sales
- Shipping-mode mix

Periods with **high demand + high late-delivery rates** should be investigated for potential fulfillment or capacity pressure.

### 5. Evaluate discount effectiveness

Compare:

**Discount → Sales → Profit → Profit Margin**

The objective is to determine whether additional sales generated through discounting justify the reduction in profitability.

---

## 5. Business Impact

The project transforms transactional supply-chain data into an **operational decision framework**.

Instead of asking only:

> **"What is the late-delivery rate?"**

the analysis answers:

> **"Where is delivery performance weakest, how much business is exposed, what characteristics are associated with the problem, and where should management investigate first?"**

This allows management to prioritize improvement opportunities using both:

**Operational Risk + Financial Impact**

---

## 6. Analytical Approach

```text
Business Problem
       ↓
Data Understanding
       ↓
Data Cleaning & Quality Checks
       ↓
KPI Analysis
       ↓
Shipping Mode Analysis
       ↓
Market & Regional Analysis
       ↓
Product Analysis
       ↓
Root Cause Analysis
       ↓
Trend & Time Analysis
       ↓
Financial Impact Analysis
       ↓
Risk × Business Impact
       ↓
Executive Recommendations
```

---

## 7. Dataset

**Dataset:** DataCo Smart Supply Chain

The dataset contains approximately **71K order-line records** covering:

- Orders
- Order items
- Shipping
- Delivery status
- Products
- Categories
- Customers
- Markets
- Regions
- Sales
- Discounts
- Profit-related metrics

### Data Grain

> **One row represents an order-line/item-level transaction.**

Therefore, order-level KPIs use distinct `Order ID` rather than simply counting rows.

---

## 8. Tech Stack

| Technology | Purpose |
|---|---|
| **Microsoft Excel** | Analysis and reporting |
| **Power Query** | Data cleaning and transformation |
| **Excel Tables** | Structured analytical model |
| **PivotTables** | Segmentation and aggregation |
| **Excel Formulas** | KPI and financial calculations |
| **Conditional Formatting** | Risk identification |
| **Excel Charts** | Business visualization |

### Key Excel Techniques

- `SUMIFS`
- `COUNTIFS`
- `FILTER`
- `UNIQUE`
- `COUNTA`
- `AVERAGEIFS`
- `CORREL`
- `IFS`
- Percentage-point analysis
- Rolling averages
- PivotTables
- Heatmaps
- Risk × Impact analysis

---

## 9. Project Structure

```text
supply-chain-delivery-analytics/
│
├── README.md
│
├── excel/
│   └── Supply_Chain_Delivery_Analytics.xlsx
│
├── documentation/
│   ├── business-problem.md
│   ├── data-dictionary.md
│   ├── data-quality.md
│   ├── insights.md
│   └── recommendations.md
│
├── screenshots/
│   ├── executive-dashboard.png
│   ├── shipping-analysis.png
│   ├── market-analysis.png
│   ├── product-analysis.png
│   ├── root-cause-analysis.png
│   └── financial-analysis.png
│
└── LICENSE
```

---

## 10. Analytical Limitations

- The dataset is observational; relationships do not establish causation.
- Late-delivery rate does **not** represent financial loss.
- Revenue associated with late orders should be interpreted as **revenue exposure**, not lost revenue.
- Profit calculations must respect the order-line vs. order-level grain.
- Small segments can produce unstable rates; volume thresholds should be applied.
- Additional data such as carrier performance, warehouse processing time, refunds, customer complaints, logistics costs and cancellations would strengthen root-cause analysis.

---

## 11. Portfolio Takeaway

> **The key analytical finding is that supply-chain priorities should not be determined by delivery rate alone. Combining delivery risk with revenue exposure and profitability provides a more effective framework for identifying where management should investigate first.**

---

## 👤 Author

**Vinit Nimbalkar**

Data Science Engineering Student  
Aspiring Data Analyst | Business Analytics | Excel | SQL | Power BI

---

### ⭐ Project Focus

**Business Problem → Insights → Financial Exposure → Recommendations**

**Not just a dashboard. A decision-oriented analytics case study.**
