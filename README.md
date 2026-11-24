# Retail Transaction & Star-Schema Analytics

An end-to-end retail data engineering and business intelligence project modeling large-scale transaction records into a normalized **Star Schema** (`Fact_Transactions`, `Dim_Products`, and `Bridge_Transaction_Products`) using **Python** and **Power BI**.

---

## Project Overview

Raw retail transaction logs often store nested multi-item baskets within single records, making product-level aggregation slow and error-prone in BI tools. This project transforms raw retail transaction data into a relational **Star Schema with a Bridge Table**, enabling fast, accurate analysis of basket composition, product affinity, revenue performance, and customer purchasing trends.

---

## Data Architecture & Repository Contents

| File | Description |
| :--- | :--- |
| `Fact_Transactions.csv` | Core fact table containing transaction-level metrics, timestamps, and order totals |
| `Dim_Products.csv` | Product dimension table containing unique SKU attributes and product metadata |
| `Bridge_Transaction_Products.csv` | Bridge table resolving many-to-many relationships between transactions and individual products |
| `retailnew-checkpoint.ipynb` | Jupyter Notebook containing Python (Pandas) ETL transformations, schema normalization, and data validation |
| `RETAIL.pbix` | Multi-page interactive Power BI dashboard built on top of the Star Schema data model |
| `Retail_Transactions_Dataset-checkpoint.csv` | Source retail transactions dataset |

---

## Key Analytical Capabilities

- **Star-Schema Modeling:** Decomposed flat transaction records into fact, dimension, and bridge tables to eliminate data redundancy and optimize DAX query performance in Power BI.
- **Basket & Product Performance:** Evaluates top-selling products, average basket size, category revenue share, and cross-sell combinations via the transaction-product bridge.
- **Interactive BI Reporting:** Provides dynamic filtering across time periods, product lines, and transaction segments in `RETAIL.pbix`.

---

## How to Use

1. **Review the ETL Pipeline:** Open `retailnew-checkpoint.ipynb` in Jupyter Notebook or VS Code to inspect how the raw dataset was cleaned and split into `Fact_Transactions`, `Dim_Products`, and `Bridge
