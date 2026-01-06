# Retail Orders Data Analysis | Python & SQL Server

## Project Overview

This project delivers an **end-to-end retail sales analysis pipeline**, combining **Python for data ingestion and preprocessing** with **SQL Server for advanced analytical querying**.
The objective is to extract **actionable business insights** from transactional retail data, focusing on **revenue performance, product trends, and regional sales dynamics**.

The workflow mirrors a **real-world analytics environment**, where raw data is sourced externally, cleaned programmatically, stored in a relational database, and analyzed using SQL.

---

## Business Objectives

The analysis aims to answer key business questions, including:

* Which products generate the **highest revenue**?
* What are the **top-selling products by region**?
* How does **sales performance evolve over time**?
* Which product categories show the **strongest year-over-year growth**?

These insights can support **pricing strategy, inventory planning, and regional marketing decisions**.

---

## Dataset Description

* **Source:** Kaggle – Retail Orders Dataset
* **Granularity:** Order-level transactional data
* **Key Attributes:**

  * Order date
  * Product ID and category
  * Region and sub-category
  * Sales price
  * Quantity ordered

Missing and inconsistent values are explicitly handled during preprocessing.

---

## Tech Stack

| Layer                     | Tools                              |
| ------------------------- | ---------------------------------- |
| Data Ingestion & Cleaning | Python (Pandas)                    |
| Database                  | Microsoft SQL Server (SQL Express) |
| Connectivity              | SQLAlchemy + ODBC Driver           |
| Querying & Analysis       | T-SQL                              |
| Version Control           | Git & GitHub                       |

---

## Project Workflow

### Data Import

* Dataset downloaded programmatically using the Kaggle API.
* Compressed files extracted and loaded into a Pandas DataFrame.

### Data Cleaning & Preparation (Python)

Key preprocessing steps:

* Handled missing values (`Not Available`, `unknown`)
* Converted `order_date` to proper datetime format
* Dropped redundant pricing columns to avoid data leakage
* Ensured schema consistency for database ingestion

### Database Integration

* Established a connection to **SQL Server** using SQLAlchemy.
* Loaded cleaned data into a relational table (`df_orders`) using an automated pipeline.
* Designed for **scalability and reproducibility**, mirroring enterprise ETL practices.

### Analytical SQL Queries

Performed advanced SQL analysis to derive business insights, including:

* Top 10 revenue-generating products
* Top 5 products by sales in each region
* Year-over-year sales comparison by sub-category
* Identification of highest growth product segments

CTEs, aggregations, and window functions were used to ensure **clarity, efficiency, and analytical accuracy**.

---

## Key Insights

* A small subset of products contributes disproportionately to total revenue, highlighting **Pareto-type sales behavior**.
* Regional performance varies significantly, indicating opportunities for **localized marketing and inventory optimization**.
* Certain sub-categories show strong year-over-year growth, signaling **high-potential segments** for future investment.

---

## Repository Structure

```
├── Data_Import_Cleaning.ipynb   # Python data ingestion & preprocessing
├── SQLQueries.sql               # Analytical SQL queries
├── orders.csv                   # Raw dataset (if included)
└── README.md                    # Project documentation
```


