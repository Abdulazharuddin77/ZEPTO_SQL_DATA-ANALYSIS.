#  🛒 Zepto SQL Data Analyst Portfolio Project  

This project is an end-to-end SQL Data Analyst portfolio project built using real-world Zepto grocery delivery data. It is designed to simulate how data analysts work with business data to generate insights, improve operations, and support decision-making.

This project is ideal for:
- Freshers applying for Data Analyst / Business Analyst roles
- Strengthening SQL & Data Analysis portfolios
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

- SQL – Core analysis & business queries  
- MySQL / PostgreSQL / SQLite – Database engine  
- Excel / CSV – Dataset storage  
- GitHub – Version control & portfolio hosting  

(Optional Add-Ons if you used them)
- Power BI / Tableau – Dashboard creation  
- Python – Data cleaning or automation 
--------
## ⚙ Project Execution Flow  
This project follows a structured, end-to-end SQL analytics workflow as outlined below:
### 1 Database & Schema Setup  
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
### 2 Dataset Loading

- Loaded CSV using pgAdmin's import feature.
- If you're not able to use the import feature, write this code instead:
```
   \copy zepto(category,name,mrp,discountPercent,availableQuantity,
            discountedSellingPrice,weightInGms,outOfStock,quantity)
  FROM 'data/zepto_v2.csv' WITH (FORMAT csv, HEADER true, DELIMITER ',', QUOTE '"', ENCODING 'UTF8');
```
### 3 Data Understanding & Exploration
  Once the data is loaded, several exploratory checks are performed:
- Total number of records is calculated
- A preview of the dataset is examined to understand column structure
- Null value checks are applied across all fields
- Unique product categories are identified
- In-stock vs out-of-stock product distribution is analyzed
- Duplicate product names with different SKUs are detected.

### 4 Data Quality Improvement
  To ensure reliable insights, essential cleaning steps are applied:
- Records with zero MRP or zero selling price are eliminated
- Price values are converted from paise into rupees for standardization and better interpretation

### 5 SQL-Driven Business Analytics
  Multiple analytical queries are executed to generate real-world business insights:
- Top 10 products offering the highest discount percentage
- Premium-priced products that are currently unavailable
- Category-level revenue estimation
- High-priced items (above ₹500) with low discount benefits
- Top 5 categories ranked by average discount offered
- Cost-efficiency analysis using price-per-gram
- Product segmentation based on weight into Small, Medium, and Bulk
- Total category-wise inventory weight calculation


 🛠 How to Run This Project Locally
 
1 . Clone the repository
```
https://github.com/Abdulazharuddin77/ZEPTO_SQL_DATA-ANALYSIS..git
````
 2. Open the zepto_SQL_data_analysis.sql file, which contains:
- Table setup
- Data exploration queries
- Data cleaning operations
- Complete business analysis SQL queries
3. Create a PostgreSQL database and execute the SQL file
4. Import the dataset (ensure it is saved in UTF-8 format before loading)


  
