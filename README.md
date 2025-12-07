Perfect—your content is already strong. Below is a clean, fully polished, recruiter-ready final README version with better flow, formatting, and clarity. You can directly paste this into your GitHub README.md ✅
(It keeps everything original, structured, and professional.)


---

🛒 Zepto SQL Data Analyst Portfolio Project

This is an end-to-end SQL Data Analytics portfolio project built on real-world Zepto grocery delivery data. The project simulates how data analysts work with business datasets to uncover insights, optimize operations, and support data-driven decisions.

This project is ideal for:

Freshers applying for Data Analyst / Business Analyst roles

Strengthening SQL & Data Analytics portfolios

Interview preparation using real business use-cases



---

🎯 Project Objectives

The key goals of this project are to:

Analyze product demand, pricing, inventory, and revenue trends

Identify top-selling products and peak demand patterns

Evaluate discount strategies and stock availability

Understand customer purchase behavior using SQL

Generate actionable business insights for growth and optimization



---

🧾 Dataset Overview

The dataset was originally sourced from Kaggle and closely mirrors Zepto’s real product catalog structure.

Each row represents a unique SKU (Stock Keeping Unit).

The same product may appear multiple times due to different:

Package sizes

Weights

Discounts

Categories



This setup reflects how real-world e-commerce inventory systems actually work.

📊 Dataset Columns

sku_id – Unique product identifier (Synthetic Primary Key)

name – Product name

category – Product category (Fruits, Snacks, etc.)

mrp – Maximum Retail Price (₹)

discountPercent – Discount applied on MRP

discountedSellingPrice – Final selling price after discount (₹)

availableQuantity – Inventory units available

weightInGms – Product weight in grams

outOfStock – Stock availability flag (Boolean)

quantity – Units per package



---

🛠 Tools & Technologies

SQL – Core querying & analytics

PostgreSQL / MySQL / SQLite – Database engines

Excel / CSV – Data storage & inspection

GitHub – Version control & portfolio hosting


Optional Add-ons (if implemented):

Power BI / Tableau – Dashboard visualization

Python – Data cleaning & automation



---

⚙ Project Execution Workflow

1️⃣ Database & Table Setup

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


---

2️⃣ Dataset Loading

Data is imported using pgAdmin CSV Import

If import is not available, use:


\copy zepto(category,name,mrp,discountPercent,availableQuantity,
discountedSellingPrice,weightInGms,outOfStock,quantity)
FROM 'data/zepto_v2.csv'
WITH (FORMAT csv, HEADER true, DELIMITER ',', QUOTE '"', ENCODING 'UTF8');


---

3️⃣ Data Understanding & Exploration

After loading the data, the following checks are performed:

Total number of records

Sample data preview

Null value analysis

Unique product categories

In-stock vs out-of-stock comparison

Detection of duplicate product names across SKUs



---

4️⃣ Data Cleaning & Quality Improvement

To ensure accurate results:

Products with zero MRP or zero selling price are removed

All prices are standardized into Indian Rupees (₹)

Invalid stock and pricing records are filtered



---

5️⃣ SQL-Based Business Analysis

Key business insights generated using SQL:

Top 10 products with highest discount

Premium-priced out-of-stock products

Category-wise revenue estimation

High-priced products (₹500+) with low discounts

Top 5 categories by average discount

Price-per-gram cost efficiency analysis

Product segmentation by weight (Small / Medium / Bulk)

Total inventory weight by category



---

▶ How to Run This Project Locally

1. Clone the repository


2. Open zepto_SQL_data_analysis.sql, which includes:

Table creation

Data exploration

Data cleaning

Full business analysis queries



3. Create a PostgreSQL database


4. Execute the SQL file


5. Import the dataset (ensure UTF-8 encoding)




---

✅ Key Learning Outcomes

Hands-on experience with real-world e-commerce data

Strong understanding of SQL joins, aggregates & filters

Practice with business-driven data analysis

Portfolio-ready project for job interviews



---

If you want, I can also provide: ✅ GitHub project description (short bio)
✅ LinkedIn project post
✅ Resume-ready project bullet points
✅ SQL interview questions based on this project

Just tell me which one you want next 🚀
