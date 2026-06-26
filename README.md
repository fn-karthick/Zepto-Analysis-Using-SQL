# 🛒 Zepto Inventory & Sales Analysis using PostgreSQL

## 📌 Project Overview

This project presents a comprehensive SQL-based exploratory data analysis of Zepto's product inventory dataset using **PostgreSQL (pgAdmin 4)**. The objective is to demonstrate practical SQL skills by performing data exploration, cleaning, and business analysis to extract meaningful insights from an e-commerce inventory database.

The analysis focuses on identifying pricing trends, discount strategies, inventory distribution, product availability, revenue estimation, and category-level performance using advanced SQL queries.

## 🎯 Objectives

* Explore and understand the structure of the dataset
* Detect missing and inconsistent data
* Clean invalid records before analysis
* Analyze pricing and discount patterns
* Evaluate inventory availability
* Estimate category-wise revenue
* Identify best-value products
* Perform product segmentation based on weight
* Demonstrate real-world SQL querying techniques

## 🛠️ Tech Stack

| Technology  | Purpose                     |
| ----------- | --------------------------- |
| PostgreSQL  | Database Management System  |
| pgAdmin 4   | SQL Development Environment |
| SQL         | Data Cleaning & Analysis    |
| CSV Dataset | Product Inventory Data      |

## 📂 Dataset Information

The dataset contains inventory information for products available on Zepto, including pricing, discounts, stock availability, product weights, and category details.

### Dataset Features

* Product Category
* Product Name
* Maximum Retail Price (MRP)
* Discount Percentage
* Discounted Selling Price
* Available Quantity
* Product Weight
* Stock Availability
* Product Quantity

## 🗄️ Database Schema

```sql
CREATE TABLE zepto (
    sku_id SERIAL PRIMARY KEY,
    category VARCHAR(120),
    name VARCHAR(150) NOT NULL,
    mrp NUMERIC(8,2),
    discountPercent NUMERIC(5,2),
    availableQuantity INTEGER,
    discountedSellingPrice NUMERIC(8,2),
    weightInGms INTEGER,
    outOfStock BOOLEAN,
    quantity INTEGER
);
```

# 🔍 Project Workflow

```
        ┌────────────────────┐
        │   CSV Dataset      │
        └─────────┬──────────┘
                  │
                  ▼
        ┌────────────────────┐
        │ PostgreSQL Import  │
        └─────────┬──────────┘
                  │
                  ▼
        ┌────────────────────┐
        │ Data Validation    │
        └─────────┬──────────┘
                  │
                  ▼
        ┌────────────────────┐
        │ Data Cleaning      │
        └─────────┬──────────┘
                  │
                  ▼
        ┌────────────────────┐
        │ SQL Analytics      │
        └─────────┬──────────┘
                  │
                  ▼
        ┌────────────────────┐
        │ Business Insights  │
        └────────────────────┘
```

# 📊 Data Exploration

The initial phase focuses on understanding the dataset.

### Performed Explorations

* Counted total records
* Previewed sample records
* Checked for NULL values
* Identified unique product categories
* Compared products in stock vs out of stock
* Detected duplicate product names

# 🧹 Data Cleaning

Data quality was improved before performing analysis.

Cleaning steps included:

* Identifying products with zero pricing
* Removing invalid records
* Converting prices from paise to Indian Rupees
* Validating updated price values

# 📈 Business Analysis

The following SQL analyses were performed:

### 1️⃣ Top 10 Best-Value Products

Identified products offering the highest discounts.

### 2️⃣ High-Value Products Currently Out of Stock

Retrieved premium products (MRP > ₹300) that are unavailable.

### 3️⃣ Estimated Revenue by Category

Calculated potential revenue using:

```
Discounted Selling Price × Available Quantity
```

### 4️⃣ Premium Products with Low Discounts

Found products priced above ₹500 with discounts below 10%.

### 5️⃣ Categories with Highest Average Discounts

Ranked product categories based on average discount percentage.

### 6️⃣ Best Value Products by Price per Gram

Calculated the price per gram for products weighing more than 100 grams.

### 7️⃣ Product Weight Classification

Grouped products into:

* Low
* Medium
* Bulk

using SQL CASE statements.

### 8️⃣ Total Inventory Weight by Category

Calculated total inventory weight available in each product category.

# 📁 Project Structure

```
Zepto-SQL-Analysis/
│
├── Dataset/
│   └── zepto_v2.csv
│
├── SQL/
│   └── zepto_analysis.sql
│
├── README.md
│
└── Screenshots/
    ├── Database.png
    ├── Queries.png
    └── Results.png
```

# 🚀 How to Run

### Clone the repository

```bash
git clone https://github.com/yourusername/Zepto-SQL-Analysis.git
```

### Open PostgreSQL

Launch pgAdmin 4 and create a new database.

### Create the table

Execute the SQL script to generate the table structure.

### Import Dataset

Import the `zepto.csv` file into the `zepto` table.

### Execute Queries

Run the SQL queries sequentially to perform:

* Data Exploration
* Data Cleaning
* Business Analysis

# 📌 Key SQL Concepts Used

* SELECT
* WHERE
* DISTINCT
* ORDER BY
* GROUP BY
* HAVING
* CASE
* Aggregate Functions
* UPDATE
* DELETE
* LIMIT
* Data Cleaning
* Exploratory Data Analysis (EDA)

# 📈 Skills Demonstrated

* SQL Query Writing
* Database Design
* PostgreSQL
* Data Cleaning
* Exploratory Data Analysis
* Business Analytics
* Inventory Analysis
* Revenue Estimation
* Data Aggregation
* Conditional Logic using CASE

# 📷 Project Preview

* Database Schema
* Table Data
* SQL Query Execution
* Query Results
* pgAdmin Dashboard

# ⭐ Future Improvements

* Develop an interactive Power BI dashboard
* Create Tableau visualizations
* Build a Python data analysis pipeline
* Automate SQL reporting
* Perform customer and sales trend analysis
  
# 👨‍💻 Author

**Karthick Raja P**

**Aspiring Data Scientist | SQL | Python | Power BI | Machine Learning**

If you found this project useful, consider giving it a ⭐ on GitHub!
