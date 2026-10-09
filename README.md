# 📈 Sales & Profit Performance Analytics Dashboard

An interactive and executive-level **Power BI** analytics dashboard designed to monitor sales volume, analyze profitability, track order quantities, and evaluate customer trends to optimize commercial strategy and revenue growth.

---

## 📌 Project Overview

This business intelligence solution delivers end-to-end visibility into overall sales performance. By consolidating transactional sales, profit margins, and customer data, the dashboard equips decision-makers with actionable insights to identify high-margin opportunities, top-tier customer segments, and product growth drivers.

---

## 📑 Dashboard Architecture & Pages

The dashboard provides structured multi-level reporting across dedicated analytical views[cite: 3]:

1. **Executive Overview (`Overview Page`):**[cite: 3]
   * Core KPIs at a glance: **Total Sales**, **Total Profit**, **Total Quantity Sold**, and **Active Customers**[cite: 3].
   * High-level trend tracking across monthly, quarterly, and annual performance.
   * Visual comparisons between revenue generated and bottom-line profit margins.

2. **Granular Breakdown (`Detail Page`):**[cite: 3]
   * Deep-dive transaction and category performance analysis[cite: 3].
   * Customer distribution and order breakdown by geography/region and product lines.
   * Interactive cross-filtering and drill-down capabilities for operational analysis.

---

## 🛠️ Tools & Technical Workflow

* **Microsoft Power BI Desktop:** User interface layout, KPI card formatting, custom icons, and interactive visual design[cite: 3].
* **Power Query (ETL):** Data cleansing, type validation, merging tables, and dimensional schema structuring.
* **Data Modeling:** Optimized Star Schema architecture connecting transactional fact data with Date, Product, and Customer dimensions.
* **DAX (Data Analysis Expressions):** Calculated measures for sales revenue, profit margins, quantity aggregates, and time-intelligence metrics.

---

## 💡 Key DAX Measures

```dax
// Total Sales Revenue
Total Sales = SUM('Sales'[SalesAmount])

// Total Profit
Total Profit = SUM('Sales'[Profit])

// Profit Margin Percentage
Profit Margin % = 
DIVIDE([Total Profit], [Total Sales], 0)

// Total Quantity Sold
Total Quantity = SUM('Sales'[Quantity])
Author
Marwan Hamdy Alsweny - Data Analyst & BI Developer

// Total Distinct Customers
Total Customers = DISTINCTCOUNT('Customers'[CustomerID])
