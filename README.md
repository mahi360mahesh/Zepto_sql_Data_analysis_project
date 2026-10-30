# Zepto SQL Data Analysis Project

## 📌 Project Overview

This project focuses on analyzing Zepto product inventory and pricing data using SQL. The objective is to explore product information, clean raw data, and extract meaningful business insights related to product pricing, discounts, inventory availability, and category-wise revenue.

The project uses SQL queries to answer real-world business questions and demonstrate practical SQL skills for data analysis.

## 📂 Project Files

| File Name | Description |
|---|---|
| `zepto_v2.csv` | Raw dataset containing product information |
| `Zepto_SQL_data_analysis.sql` | SQL scripts for table creation, data exploration, cleaning, and analysis |

## 📊 Dataset Description

- **Total Records:** 3,732
- **Total Columns:** 9
- **Data Format:** CSV

### Dataset Columns

| Column | Description |
|---|---|
| Category | Product category |
| name | Product name |
| mrp | Maximum Retail Price |
| discountPercent | Discount percentage |
| availableQuantity | Available inventory quantity |
| discountedSellingPrice | Selling price after discount |
| weightInGms | Product weight in grams |
| outOfStock | Product stock availability |
| quantity | Product quantity |

## 🛠️ Tools & Technologies

- **PostgreSQL** – Database management and SQL analysis
- **SQL** – Data exploration, cleaning, aggregation, and business analysis
- **CSV** – Dataset storage and import

## 🔍 Project Workflow

### 1. Database & Table Creation
- Created the Zepto table using appropriate SQL data types.
- Defined a primary key using `SERIAL`.
- Applied `NOT NULL` constraints where required.

### 2. Data Exploration
- Retrieved total record count.
- Displayed sample product records.
- Identified NULL values.
- Explored distinct product categories.
- Compared in-stock and out-of-stock products.
- Identified product names appearing multiple times.

### 3. Data Cleaning
- Identified products with zero MRP or selling price.
- Removed records with zero MRP.
- Converted MRP and discounted selling prices from paise to rupees.

### 4. SQL Business Analysis

The project answers the following 8 business questions:

1. **Top 10 Best-Value Products:** Identified products offering the highest discount percentages.
2. **High-MRP Out-of-Stock Products:** Found products with MRP above ₹300 that are currently out of stock.
3. **Category-Wise Estimated Revenue:** Calculated estimated revenue using discounted selling price and available quantity.
4. **High-Priced Products with Low Discounts:** Identified products with MRP above ₹500 and discounts below 10%.
5. **Top 5 Discount Categories:** Found categories offering the highest average discount percentage.
6. **Price Per Gram Analysis:** Calculated price per gram for products weighing at least 100 grams to identify better-value products.
7. **Product Weight Categorization:** Classified products into Low, Medium, and Bulk categories using CASE statements.
8. **Category-Wise Inventory Weight:** Calculated total inventory weight for each product category.

## 💡 SQL Concepts Used

- CREATE TABLE
- PRIMARY KEY
- SERIAL and data types
- SELECT and DISTINCT
- WHERE and filtering conditions
- IS NULL
- ORDER BY and LIMIT
- GROUP BY and HAVING
- COUNT(), SUM(), AVG()
- ROUND()
- CASE WHEN
- UPDATE and DELETE
- Aggregate functions and data cleaning

## 🎯 Key Learning Outcomes

- Gained practical experience in SQL-based data exploration and cleaning.
- Learned to analyze product pricing, discounts, and inventory availability.
- Applied aggregate functions to calculate category-level business metrics.
- Used conditional logic to categorize products based on weight.
- Developed SQL queries to solve real-world business problems.
- Improved analytical thinking and business insight generation.

## 🚀 How to Run the Project

1. Download or clone this repository.
2. Open PostgreSQL using pgAdmin or another SQL client.
3. Create a database for the project.
4. Create the `zepto` table using the provided SQL script.
5. Import `zepto_v2.csv` into the table, mapping the CSV `Category` column to the SQL `category` column. Exclude the auto-generated `sku_id`.
6. Execute the SQL queries from `Zepto_SQL_data_analysis.sql`.
7. Explore the results of each business analysis query.

**Note:** The SQL cleaning operations modify the imported data. Keep a copy of the original CSV before running the cleaning queries.

## 📌 Conclusion

This project demonstrates how SQL can be used to transform raw product data into meaningful business insights. By performing data exploration, cleaning, and business analysis, the project provides a better understanding of product pricing, discount strategies, and inventory management.
