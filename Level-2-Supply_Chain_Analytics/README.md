## 📌 Project Overview
Analyzed 100,000+ e-commerce transactions from Brazilian marketplace Olist to identify delivery performance issues, regional delays, and seller accountability. The project involved combining 5 separate data tables to build a unified analysis framework.

## 🎯 Business Problem
GlobalMart Distribution (simulated client) faced:
- Increasing stockouts and delivery delays
- Customer satisfaction issues
- Unreliable seller performance
- Inconsistent regional logistics

## 📊 Business Questions Answered

| # | Question | Answer |
|---|----------|--------|
| 1 | Total Revenue & Orders | R$ 15,843,553 / 98,667 orders |
| 2 | Average Shipping Time | 13 days |
| 3 | Top Categories by Sales | Health & Beauty, Watches & Gifts, Bed Bath Table |
| 4 | Regions with Most Delays | SP (6,002), PR (485), MG (431), RJ (354), SC (215) |
| 5 | Order Size vs Delays | Delays occur even with order size 1-6; 8% overall delay rate |
| 6 | Worst Performing Sellers | 215 sellers (7%) have >30% delay rate |
| 7 | Monthly Trends | Peak: May, Jun, Aug / Revenue peak: Dec 2017 |
| 8 | Delay Contributing Factors | Seller performance, Order size, Regional logistics (SP) |

## 🛠️ Tools & Skills Used

| Tool | Application |
|------|-------------|
| Microsoft Excel | Data analysis, Pivot Tables, Dashboard |
| Power Pivot | Data modeling, Table relationships |
| XLOOKUP | Joining data across tables |
| Pivot Charts | Visualization |
| Slicers | Interactive filtering |

## 📁 Data Sources

**Dataset:** Brazilian E-Commerce Public Dataset by Olist
**Source:** [Kaggle](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce)

| Table | Rows | Purpose |
|-------|------|---------|
| olist_orders_dataset | 99,441 | Order dates, status, delivery info |
| olist_order_items_dataset | 112,650 | Product, seller, price per order |
| olist_products_dataset | 32,951 | Product categories, measurements |
| olist_sellers_dataset | 3,095 | Seller location data |
| olist_order_payments_dataset | 103,886 | Payment method, value |

## 🧹 Data Quality & Cleaning

| Table | Issue Found | Action Taken |
|-------|-------------|--------------|
| order_items | No issues | No action needed |
| payments | 3 "not_defined" payment types | Removed rows |
| orders | 160 null in order_approved_at | Removed rows |
| orders | Null delivery dates | Kept — expected for cancelled orders |
| products | 601 null category names | Excluded from category analysis (1.8%) |
| sellers | 1 wrong datatype in city | Removed row |

## 📈 Key Insights

### Delivery Performance
- **8% of all orders are delayed** (7,827 of 96,477)
- **SP state has 12x more delays** than the next highest state
- **215 sellers (7%)** have delay rates exceeding 30%

### Revenue Patterns
- **Top Category:** Health & Beauty
- **Peak Months:** May, June, August
- **Revenue Peak:** December 2017

### Critical Finding
Delays occur even with **single-item orders**, suggesting the issue is **NOT order complexity** but rather **seller/logistics performance**.

## 💡 Recommendations

| # | Recommendation | Supporting Data |
|---|----------------|-----------------|
| 1 | **Audit SP state fulfillment centers** — 6,002 delays (12x higher than other states) | Q4 Analysis |
| 2 | **Implement seller performance scorecard** — Issue warnings to 215 sellers with >30% delay rate | Q6 Analysis |
| 3 | **Investigate single-item order delays** — Problem is not order size; check dispatch process | Q5 Analysis |
| 4 | **Allocate additional logistics resources during peak months** (May, Jun, Aug) | Q7 Analysis |

## 📊 Dashboard Preview

![Dashboard Screenshot](Dashboard_Screenshot.png)

### Dashboard Components:
- **KPI Cards:** Total Revenue, Total Orders, Avg Shipping Time, Delay Rate
- **Bar Chart:** Revenue by Top 5 Categories
- **Column Chart:** Delay Count by State
- **Line Chart:** Monthly Trends (with Year slicer)
- **Bar Chart:** Delay Count by Order Size


## 📝 Lessons Learned

| Lesson | Application |
|--------|-------------|
| Plan data model BEFORE building Pivot Tables | Ensures slicers work across all charts |
| XLOOKUP = SQL JOIN equivalent | Connects tables using common keys |
| Power Pivot for multi-table relationships | Visualizes and manages complex data models |
| Define thresholds explicitly | "Worst seller = >30% delay rate" — clear, defensible |
| Tie all insights to core business problem | Recommendations must address the original question |


## 🎯 Skills Demonstrated

- [x] Multi-table data management
- [x] XLOOKUP for data joining
- [x] Power Pivot data modeling
- [x] Pivot Tables & Pivot Charts
- [x] Dashboard design with slicers
- [x] Business KPI development
- [x] Actionable recommendations
- [x] Professional documentation

## 🚀 Future Improvements

- [ ] Connect all charts to single slicer using unified data source
- [ ] Add customer location analysis (using geolocation table)
- [ ] Calculate delivery distance correlation with delays
- [ ] Implement seller ranking system in dashboard

**Project completed as part of Excel Data Analysis Training — Level 2**

**Next:** Level 3 — Power BI Dashboard Development
