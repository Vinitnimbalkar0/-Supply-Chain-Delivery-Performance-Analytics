# Data Dictionary

## Dataset Grain

**One row = one order-line/item-level transaction.**

## Core Fields

| Column | Description | Business Use |
|---|---|---|
| `Order Id` | Order identifier | Distinct order counting |
| `Order Item Id` | Order-line identifier | Transaction analysis |
| `Order Status` | Order status | Order monitoring |
| `order date (DateOrders)` | Order date/time | Demand and trend analysis |
| `shipping date (DateOrders)` | Shipping date/time | Shipping analysis |
| `Shipping Mode` | Selected shipping method | Shipping performance |
| `Delivery Status` | Delivery outcome/status | Delivery analysis |
| `Late_delivery_risk` | Dataset-provided risk indicator | Risk comparison |
| `Days for shipping (real)` | Actual shipping duration | Actual performance |
| `Days for shipment (scheduled)` | Scheduled shipping duration | Commitment comparison |
| `Sales` | Recorded sales value | Revenue analysis |
| `Order Item Total` | Order-line total | Financial analysis |
| `Order Item Discount` | Discount amount | Discount analysis |
| `Order Item Discount Rate` | Discount rate | Discount analysis |
| `Order Item Profit Ratio` | Profit ratio | Profitability |
| `Order Profit Per Order` | Source profit measure | Profitability |
| `Benefit per order` | Source benefit measure | Financial analysis |
| `Order Item Quantity` | Item quantity | Volume analysis |
| `Product Price` | Product price | Product analysis |
| `Product Name` | Product name | Product analysis |
| `Category Name` | Product category | Category analysis |
| `Department Name` | Product department | Department analysis |
| `Customer Id` | Customer identifier | Customer analysis |
| `Customer Segment` | Customer segment | Segmentation |
| `Market` | Geographic market | Market analysis |
| `Order Region` | Geographic region | Regional analysis |
| `Order Country` | Country | Geographic analysis |
| `Order State` | State | Geographic analysis |
| `Order City` | City | Geographic analysis |

## Derived Fields

| Field | Definition |
|---|---|
| `Order_Date` | Date extracted from order datetime |
| `Order_Month` | First day of order month |
| `Order_Year` | Year extracted from order date |
| `Shipping_Variance` | Actual shipping days − scheduled shipping days |
| `Late_Delivery_Flag` | 1 when delivery status is Late delivery, otherwise 0 |
| `Shipping_Performance` | Early / On Schedule / Late |
| `Profit_Per_Order` | Validated source profit measure |
| `Profit_Margin` | Total profit ÷ total sales |
| `Order_Size` | Small / Medium / Large classification |
| `Discount_Bucket` | No / Low / Medium / High discount |

## Important Definitions

**Late Delivery Rate**

```text
Late Orders ÷ Distinct Orders
```

**AOV**

```text
Total Sales ÷ Distinct Orders
```

**Shipping Variance**

```text
Actual Shipping Days − Scheduled Shipping Days
```

**Profit Margin**

```text
Total Profit ÷ Total Sales
```

**Risk Index**

```text
Segment Late Rate ÷ Overall Late Rate
```

## Notes

- `Late_delivery_risk` is treated as a dataset-provided indicator.
- Percentage fields such as profit ratio should not be summed.
- Monetary values remain in the source dataset's units.
