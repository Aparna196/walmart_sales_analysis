# Walmart Sales Data Analysis using MySQL

## Project Overview
This project performs sales data analysis on Walmart transactional data using MySQL.  
The project includes database creation, data cleaning, feature engineering, and business analysis queries.

The main objective of this project is to analyze:
- Sales performance
- Customer behavior
- Product performance
- Revenue trends
- Tax and rating analysis

---

## Technologies Used
- MySQL
- SQL
- MySQL Workbench
- GitHub

---

## Database Creation
The project creates a database named:

```sql
CREATE DATABASE IF NOT EXISTS walmartSales;
```

and a table named:

```sql
sales
```

---

## Features Implemented

### 1. Database and Table Creation
- Database creation
- Sales table creation
- Primary key implementation
- Data type handling

### 2. Data Cleaning
- Checking data records
- Handling structured sales data

### 3. Feature Engineering
Additional columns created:
- `time_of_day`
- `day_name`
- `month_name`

These columns help perform better business analysis.

---

## Business Problems Solved

### Generic Analysis
- Unique cities analysis
- Branch distribution analysis

### Product Analysis
- Most selling product line
- Revenue by month
- Highest COGS month
- Product line with highest revenue
- Product line with highest VAT
- Product performance classification

### Customer Analysis
- Customer type analysis
- Payment method analysis
- Gender distribution analysis
- Customer rating analysis

### Sales Analysis
- Sales by time of day
- Revenue by customer type
- Tax analysis by city
- VAT contribution by customer type

---

## SQL Concepts Used
- CREATE DATABASE
- CREATE TABLE
- ALTER TABLE
- UPDATE
- CASE Statements
- GROUP BY
- ORDER BY
- Aggregate Functions
- Subqueries
- Data Filtering
- Feature Engineering

---

## Project Structure

```text
Walmart-Sales-Analysis/
│
├── walmart_sales_analysis.sql
├── README.md
└── dataset.csv
```

---

## How to Run the Project

1. Open MySQL Workbench
2. Create and select the database:
   ```sql
   CREATE DATABASE walmartSales;
   USE walmartSales;
   ```

3. Run the SQL script
4. Insert dataset into the `sales` table
5. Execute analysis queries

---

## Sample Queries

### Revenue by Product Line

```sql
SELECT
    product_line,
    SUM(total) as total_revenue
FROM sales
GROUP BY product_line
ORDER BY total_revenue DESC;
```

### Most Common Customer Type

```sql
SELECT
    customer_type,
    COUNT(*) as count
FROM sales
GROUP BY customer_type
ORDER BY count DESC;
```

---

## Learning Outcomes
Through this project, the following concepts were practiced:
- SQL Query Writing
- Database Design
- Data Analysis
- Business Intelligence Queries
- Data Aggregation
- Feature Engineering

---

## Future Improvements
- Dashboard integration using Power BI/Tableau
- Data visualization
- Stored procedures
- Views and indexing
- Advanced SQL analytics

---
