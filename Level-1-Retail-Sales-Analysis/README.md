# Retail Store Sales Analysis

## 📌 Project Overview
Analyzed 12,575 retail sales transactions to uncover revenue trends, 
category performance, and customer behavior for QuickCart Online Retail.

## 🎯 Business Questions Answered
1. What is the total revenue generated?
2. What is the average transaction value?
3. Which top 5 categories generate the most revenue?
4. Which sales channel performs better (Online vs In-store)?
5. What is the monthly sales trend?
6. How does discounting impact transaction value?
7. Who are the top 10 customers by spend?
8. What is the most common payment method?

## 🛠️ Tools Used
- Microsoft Excel
  - Pivot Tables
  - Data Cleaning (TRIM, PROPER, Formulas)
  - Charts & Dashboard Design

## 📊 Key Insights
| Metric | Value |
|--------|-------|
| Total Revenue | $1,552,071 |
| Average Transaction Value | $129.65 |
| Total Transactions | 11,971 |
| Top Category | Butchers ($208,118) |
| Best Channel | Online (4.03% higher than In-store) |
| Discount Usage | 50.34% of transactions |
| Top Payment Method | Cash (34.27%) |

## 🧹 Data Cleaning Performed
- Removed 604 rows with unrecoverable financial data (~4.8%)
- Calculated missing Price_Per_Unit using Total_Spent ÷ Quantity
- Calculated missing Quantity using Total_Spent ÷ Price_Per_Unit
- Standardized text formatting (TRIM + PROPER)
- Excluded Item column from analysis (10% missing, not required)

## 📈 Dashboard Preview
![Dashboard Screenshot](Dashboard_Screenshot.png)

## 📂 Dataset Source
[Kaggle - Dirty Retail Store Sales Dataset](https://www.kaggle.com/datasets/ahmedmohamed2003/retail-store-sales-dirty-for-data-cleaning/data)

## 🔑 Skills Demonstrated
- Data Cleaning & Validation
- Exploratory Data Analysis
- Pivot Table Analysis
- Business KPI Development
- Dashboard Design

## 📝 Lessons Learned
- Never replace missing values with zero — it injects false data
- Answer what the business ASKED, not what seems interesting
- Verify calculations before presenting
- Documentation matters as much as analysis

---
**Project completed as part of Excel Data Analysis Training**
