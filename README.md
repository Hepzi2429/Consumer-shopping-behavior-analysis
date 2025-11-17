# 🛍️ Customer Shopping Behavior Analysis

A data analytics project analyzing customer purchasing behaviors, spending patterns, and preferences across multiple product categories using Python, MySQL, and Power BI.

---

## 📌 Project Overview

This project explores customer shopping trends using a dataset of **3,900 records** across various categories. The key objectives include studying:

- Customer demographics  
- Spending patterns  
- Item preferences  
- Rating behavior  
- Discount usage  
- Overall buying tendencies  

---

## ⚙️ Workflow

1. **Data Cleaning** — Performed in Python  
2. **Missing Value Handling** — 53 missing ratings handled category-wise  
3. **Data Loading** — Cleaned dataset loaded into MySQL  
4. **SQL Analysis** — Business-oriented queries for behavioral insights  
5. **Visualization** — Interactive Power BI dashboard  

---

## 📂 Dataset Summary

| Details | Information |
|----------|--------------|
| Total Rows | 3,900 |
| Total Columns | 18 |
| Missing Values | 53 missing values in `review_rating` |
| Processing Tools | Python, MySQL, Power BI |

---
## 🐍 Data Cleaning (Python)

Data cleaning was completed using **Python (Pandas)** to ensure data quality before importing it into MySQL.

### Steps Performed

1. **Checked data structure and summary**

2. **Converted `review_rating` column to numeric**

3. **Handled missing values**
- Found 53 missing values in `review_rating`.
- Filled missing ratings using **category-wise median**.


4. **Standardized and cleaned column names**
- Converted to `snake_case`
- Cleaned inconsistent categorical values (like extra spaces, casing issues)

5. **Loaded cleaned data into MySQL**


## 🛢️ SQL Analysis Using MySQL

After loading the cleaned data, the following SQL queries were executed to derive business insights.

### 1. Top 5 Highest Rated Products

### 2. Revenue by Gender

### 3. Subscriber vs Non-Subscriber Spending

### 4. Most Discount-Used Products

### 5. Product Popularity by Category

---


---

## 📊 Power BI Dashboard

**Dashboards Include:**

- Revenue by gender and age group  
- Category-wise sales performance  
- Subscription vs non-subscription spending  
- Top-rated products  
- Average spending by shipping type  
- Discount usage analysis  
- Customer segmentation  
- Post-cleaning rating distribution  

---

## 💡 Key Insights

- Subscribers spend more compared to non-subscribers.  
- Highly rated products can be prioritized to drive sales.  
- Certain products are heavily discount-dependent — optimize pricing strategy.  
- Majority of customers belong to age groups **19–35** and **36–60**.  
- Express shipping users show higher average spending.  

---

## ⚙️ Tools & Libraries

| Tool | Purpose |
|------|----------|
| Python | Data cleaning and transformation |
| Pandas | Data manipulation |
| SQLAlchemy | Database connection and data export |
| MySQL | Query execution and analysis |

---

## 📊 Summary

- Cleaned dataset of 3,900 records and 18 columns.  
- Missing values in review ratings filled using median per category.  
- SQL queries used to find top-rated items, revenue segmentation, and discount trends.  
- Prepared dataset is ready for dashboard creation in Power BI.

---


## ✨ Author

**Hepzibah**  
Data Analyst | Python | SQL | Power BI  
📧hepzi2443@gmail.com



