#  🛒 Zepto SQL Data Analyst Portfolio Project  

This project is an end-to-end *SQL Data Analyst portfolio project built using real-world Zepto grocery delivery data*. It is designed to simulate how data analysts work with business data to generate insights, improve operations, and support decision-making.

This project is ideal for:
- Freshers applying for *Data Analyst / Business Analyst roles*
- Strengthening *SQL & Data Analysis portfolios*
- Interview preparation with real business use-cases  

  ---

## 📌 Project Objective  

The main objective of this project is to:
- Analyze customer orders, product demand, delivery performance, and revenue trends
- Identify top-selling products and peak order timings
- Understand customer behavior using SQL queries
- Generate actionable business insights for growth and optimization

---

## 🧾 Dataset Details  

- Originally scraped from Zepto's official product listings, the dataset was obtained from Kaggle. It is similar to what you would find in an actual e-commerce inventory system.

- A distinct SKU (Stock Keeping Unit) for a product is represented by each row. Because the same product may appear more than once in various packaging sizes, weights, discounts, or categories to increase visibility—exactly how actual catalog data appears—duplicate product names exist.

### 
 Columns:

- sku_id: Unique identifier for each product entry (Synthetic Primary Key)

- name: Product name 

- category: Product category like Fruits, Snacks, etc.

- mrp: Maximum Retail Price (Converted from paise ₹)

- discountPercent: Discount applied on MRP

- discountedSellingPrice: Final price after discount & (also converted to ₹)

- availableQuantity: Units available in inventory

- weightInGms: The weight of the product in grams

- outOfStock: A Boolean indication that indicates the availability of stock

- quantity: Number of units per package (mixed with grams for loose produce)
 
---

## 🛠 Tools & Technologies Used  

- *SQL* – Core analysis & business queries  
- *MySQL / PostgreSQL / SQLite* – Database engine  
- *Excel / CSV* – Dataset storage  
- *GitHub* – Version control & portfolio hosting  

(Optional Add-Ons if you used them)
- Power BI / Tableau – Dashboard creation  
- Python – Data cleaning or automation  

---
## ⚙ Project Execution Flow  

This project follows a structured, end-to-end SQL analytics workflow as outlined below:

---
1 . Database & Schema Setup  

The first step is to define a structured SQL table to store the Zepto product dataset efficiently. Appropriate data types are assigned to ensure accuracy and performance.

```sql
