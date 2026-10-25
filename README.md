# Blinkit Sales Analysis — SQL Portfolio Project

A MySQL portfolio project exploring sample order revenue, customer spending, product performance, monthly sales, and delivery operations.

> **Data disclaimer:** This project uses educational sample data created for SQL practice. It is **not official or verified Blinkit data**, and the results must not be presented as Blinkit's actual business performance.

## Project overview

The project uses SQL to answer practical business-style questions about sales, products, customers, and delivery times. Each row represents one order, and revenue is calculated as `quantity * price`, where `price` is the per-unit price.

## Dataset

- **Data type:** Simulated sample / practice data
- **Rows:** 30 orders
- **Date range:** January–June 2025
- **Database:** `blinkitdb`
- **Table:** `orders`

### Table schema

| Column | Description |
|---|---|
| `order_id` | Unique order identifier (primary key) |
| `customer_id` | Customer identifier |
| `customer_name` | Customer name in the sample data |
| `city` | City recorded for the order |
| `order_date` | Order date |
| `category` | Product category |
| `product_name` | Product name |
| `quantity` | Quantity purchased |
| `price` | Price per unit |
| `payment_method` | Recorded payment method |
| `delivery_time` | Delivery time in minutes |
| `rating` | Customer rating |

## Business questions answered

### Sales and revenue
- What are total revenue, order count, unique-customer count, and average order value?
- Which customers and cities contribute the most revenue?
- Which product categories generate the most revenue?

### Product performance and trends
- Which products sell the most units or generate the most revenue?
- How does revenue change by month, and which month has the highest revenue?

### Customer analysis
- Which customers place repeat orders?
- What is each customer's total spending?
- Which customers spend above the average customer-level spend?
- How can customers be segmented by total spending?

### Delivery analysis
- What is the average delivery time by city?
- Which cities have an average delivery time above 20 minutes?

## Selected results from the sample data

These values are calculated from the 30 rows included in the SQL script. They describe only this simulated dataset.

| Metric | Sample result |
|---|---:|
| Total revenue | ₹10,290.00 |
| Total orders | 30 |
| Average order value | ₹343.00 |
| Highest-revenue month | May 2025 — ₹2,165.00 |
| Lowest-revenue month | January 2025 — ₹1,240.00 |

Monthly revenue in the sample:

| Month | Revenue |
|---|---:|
| January 2025 | ₹1,240.00 |
| February 2025 | ₹1,285.00 |
| March 2025 | ₹1,760.00 |
| April 2025 | ₹1,700.00 |
| May 2025 | ₹2,165.00 |
| June 2025 | ₹2,140.00 |

## SQL concepts demonstrated

- Aggregations: `SUM()`, `AVG()`, `COUNT()`
- Unique counts: `COUNT(DISTINCT ...)`
- Grouping and filtering: `GROUP BY`, `HAVING`, `WHERE`
- Sorting and ranking: `ORDER BY`, `LIMIT`
- Customer segmentation with `CASE`
- Date analysis with `YEAR()`, `MONTH()`, and `MONTHNAME()`
- Subqueries for comparing customer spending with average customer-level spending

## How to run

### Prerequisites

- MySQL Server
- MySQL Workbench or another MySQL-compatible SQL client

### Steps

1. Download or clone this repository.
2. Open `blinkit_sales_analysis.sql` in MySQL Workbench.
3. Execute the script from top to bottom.
4. Review each result set returned by the 18 analysis queries.

The script creates the `blinkitdb` database and `orders` table if they do not already exist, then inserts the 30 sample orders and runs the analysis queries. It uses `INSERT IGNORE`, which skips rows whose `order_id` already exists. If you have modified the table or want a fresh copy of the sample data, inspect your existing records before resetting or recreating the table; do not delete data you need.

## Project structure

```text
Day 35/
├── README.md
└── blinkit_sales_analysis.sql
```

Adjust this structure in the README if the files are stored in a different folder in your repository.

## Author

**Dhruv Aggarwal**  
GitHub: [dhruvaggarwal96](https://github.com/dhruvaggarwal96)

---

*Part of my Python and data-analysis learning journey.*
