# Data Quality

## Objective

Ensure that the data is reliable before KPI calculation and business analysis.

## Quality Checks

| Check | Purpose |
|---|---|
| Row count | Confirm dataset completeness |
| Blank Order ID | Validate identifiers |
| Blank Product | Identify missing product information |
| Blank Sales | Validate financial completeness |
| Blank Order Date | Validate time analysis |
| Blank Shipping Date | Validate shipping analysis |
| Blank Shipping Mode | Validate shipping segmentation |
| Negative Quantity | Investigate unusual records |
| Zero Quantity | Investigate unusual records |
| Negative Sales | Investigate unusual financial records |
| Shipping date < Order date | Identify date inconsistencies |
| Duplicate records | Separate true duplicates from valid order lines |
| Delivery Status values | Validate categories |
| Geographic labels | Remove inconsistent whitespace |
| Data grain | Prevent incorrect order-level KPIs |

## Critical Grain Rule

Repeated `Order Id` values are **not automatically duplicates**.

One order may contain multiple order lines:

```text
Order 1001
 ├── Product A
 ├── Product B
 └── Product C
```

Therefore:

- Row count = order-line volume
- Distinct Order ID = order volume

## Cleaning Rules

1. Preserve the raw dataset.
2. Create a separate clean analytical table.
3. Trim geographic text fields.
4. Standardize dates.
5. Create `Order_Date`, `Order_Month`, and `Order_Year`.
6. Create `Shipping_Variance`.
7. Create `Late_Delivery_Flag`.
8. Investigate missing values instead of automatically deleting them.
9. Validate financial-field grain before aggregation.
10. Apply minimum-volume thresholds when ranking segments.

## Financial Data Safeguard

Profit-related fields must be checked for whether they represent order-level or order-line-level values.

Do not sum a repeated order-level profit field across every item row without validation.

## Analytical Safeguards

The analysis uses:

- Distinct Order ID for order-level metrics.
- Percentage-point differences for rate comparisons.
- Total Profit ÷ Total Sales for overall margin.
- Revenue-exposure terminology rather than unsupported revenue-loss claims.
- Association language rather than causal claims.

## Limitations

Useful missing operational variables include:

- Carrier
- Warehouse
- Picking time
- Packing time
- Handover time
- Transportation time
- Logistics cost
- Refunds
- Customer complaints
- Compensation
- Cancellation reason
