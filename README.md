# 📊 Online Retail Sales Analysis — 2011 Executive Dashboard (Power BI)

**Author:** Seema Kumari
**Tool Used:** Microsoft Power BI
**Project Type:** Business Intelligence / Executive Sales Analysis
**Dataset:** Online Retail Transactions 
---

# 🔷 Executive Summary

This project delivers a professional Power BI dashboard built to answer key strategic questions from executive leadership (CEO & CMO) regarding **2011 online retail performance**. The objective is to transform raw transactional data into actionable insights that support:

* Revenue trend forecasting
* Market expansion strategy
* Customer retention planning
* Country-level demand targeting

The dataset was rigorously cleaned and validated before analysis to ensure reliable decision-making outputs.

---

# 🎯 Business Requirements

Leadership requested visual analytics to answer the following:

1. **Monthly revenue trends for 2011** to identify seasonality patterns
2. **Top 10 revenue-generating countries (excluding UK)** with quantity sold
3. **Top 10 customers by revenue contribution**
4. **Global demand distribution** to guide expansion opportunities

Each requirement is delivered as a dedicated Power BI report page.

---

# 🗂 Dataset Description

The dataset contains transactional records from an online retail store, including:

* Invoice Number
* Product Code & Description
* Quantity Purchased
* Invoice Date
* Unit Price
* Customer ID
* Country
  
---

# 🧹 Data Preparation & Quality Controls

Data cleaning was performed in **Power Query Editor** before visualization.

## ✅ Mandatory Validation Rules Applied

### Quantity Validation

* Removed rows where Quantity ≤ 0
* Eliminated returns and erroneous entries

### Unit Price Validation

* Removed rows where UnitPrice ≤ 0
* Prevented distorted revenue calculations

### Customer Integrity

* Removed records with missing CustomerID
* Ensured accuracy in customer ranking visuals

## ✅ Data Type Corrections

| Column      | Data Type    |
| ----------- | ------------ |
| InvoiceDate | Date         |
| Quantity    | Whole Number |
| UnitPrice   | Decimal      |
| CustomerID  | Text         |

---

# 🧮 DAX Measures & Calculated Columns

## Revenue Measure

```DAX
Revenue =
SUMX(
    'Online Retail',
    'Online Retail'[Quantity] * 'Online Retail'[UnitPrice]
)
```

## Year Column

```DAX
Year = YEAR('Online Retail'[InvoiceDate])
```

## Month Column

```DAX
Month = FORMAT('Online Retail'[InvoiceDate], "MMM")
```

## Month Number (Sorting Column)

```DAX
Month Number = MONTH('Online Retail'[InvoiceDate])
```

**Sorting Applied:**
Month → Sort by Column → Month Number

---

## 📈 Page 1 — Monthly Revenue Trend (2011)

**Purpose:** Identify seasonality and revenue fluctuations in Year 2011

**Key Findings:**

* Peak revenue observed in November
* Lowest revenue in February
* Strong seasonal upward trend in Q4
* Useful for demand forecasting and inventory planning

---

## 🌍 Page 2 — Top 10 Countries by Revenue (Excluding UK)

* Excluded United Kingdom
* Top N = 10 by Revenue

**Key Findings:**

* Netherlands, EIRE, and Germany lead non-UK revenue
* Revenue not always proportional to quantity sold
* Indicates price and product mix differences

---

## 👤 Page 3 — Top 10 Customers by Revenue

**Purpose:** Identify high-value customers

**Key Findings:**

* Revenue concentration among a small customer group
* Top 2 customers contribute over 500K revenue
* Strong opportunity for loyalty & retention programs

---

## 🗺 Page 4 — Global Demand Distribution

**Metrics:**

* Quantity sold by country
* Revenue tooltip


* UK excluded to highlight expansion markets

**Key Findings:**

* High demand clusters in Europe, North America, Australia
* Several mid-tier countries show expansion potential

---

# 📌 Strategic Insights

* Revenue exhibits **clear seasonality**
* Non-UK European markets are strong revenue drivers
* Customer revenue is highly concentrated
* Demand is geographically clustered
* Several countries show scalable growth opportunity

---

# 🚀 Business Recommendations

* Increase marketing investment in top-performing countries
* Develop VIP programs for top customers
* Prepare inventory for Q4 demand spikes
* Test targeted campaigns in high-demand regions
* Investigate low-revenue months for operational gaps

---

# 🛠 Technology Stack

* Microsoft Power BI
* Power Query
* DAX Calculations
* Data Modeling
* Executive Dashboard Design

---

# ⭐ Project Value

This project demonstrates:

* Real-world executive analytics workflow
* Data cleaning & validation discipline
* Business-focused dashboard design
* Decision-driven visualization
* Professional Power BI implementation

---

**Prepared by:** Seema Kumari
**Role:** Data Analyst — Sales & Market Intelligence Project

If you found this project useful, please consider giving it a ⭐ on GitHub.
