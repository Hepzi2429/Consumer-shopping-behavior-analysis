🛍️ Customer Shopping Behavior Analysis

Data Cleaning • MySQL • Python • Power BI

📌 Project Overview

This project analyzes customer shopping behavior using a dataset containing 3,900 records across various product categories. The goal is to study customer demographics, spending patterns, item preferences, rating behavior, discount usage, and overall buying behaviour.

The workflow includes:

Data Cleaning using Python

Handling Missing Values (53 missing ratings)

Loading cleaned data into MySQL

Performing SQL Analysis

Power BI Dashboard Visualization

📂 Dataset Summary
Details	Information
Total Rows	3,900
Total Columns	18
Missing Values	53 missing values in review_rating
Processing Tools	Python, MySQL, Power BI
🧹 Data Cleaning (Python)
✔ Checked data structure
df.info()
df.describe()

✔ Converted review_rating to numeric
df['review_rating'] = pd.to_numeric(df['review_rating'], errors='coerce')

✔ Handled 53 missing values (category-wise median)
df['review_rating'] = (
    df.groupby('category')['review_rating']
      .transform(lambda x: x.fillna(x.median()))
)

✔ Cleaned column names

Converted to snake_case and standardized categorical values.

✔ Loaded cleaned data into MySQL
df.to_sql("customers", engine, if_exists="replace", index=False)

🛢️ SQL Analysis (MySQL)
🔹 1. Top 5 Highest Rated Products
SELECT item_purchased,
       ROUND(AVG(review_rating), 2) AS Average_Product_Rating
FROM customers
GROUP BY item_purchased
ORDER BY AVG(review_rating) DESC
LIMIT 5;

🔹 2. Revenue by Gender
SELECT gender, SUM(purchase_amount) AS total_revenue
FROM customers
GROUP BY gender;

🔹 3. Subscriber vs Non-Subscriber Spending
SELECT subscription_status,
       ROUND(AVG(purchase_amount),2) AS avg_spend,
       SUM(purchase_amount) AS total_revenue
FROM customers
GROUP BY subscription_status;

🔹 4. Most Discount-Used Products
SELECT item_purchased,
       ROUND(AVG(discount_applied) * 100, 2) AS discount_usage_percentage
FROM customers
GROUP BY item_purchased
ORDER BY discount_usage_percentage DESC
LIMIT 5;

🔹 5. Product Popularity by Category
SELECT category, item_purchased, COUNT(*) AS sales_count
FROM customers
GROUP BY category, item_purchased
ORDER BY category, sales_count DESC;

📊 Power BI Dashboard

The dashboard showcases:

Revenue by gender and age group

Category-wise sales

Subscription vs Non-subscription performance

Top-rated products

Average spending by shipping type

Discount usage patterns

Customer segmentation

Post-cleaning rating distribution

💡 Key Insights

Subscribers spend more compared to non-subscribers.

High-rated products can be promoted for better sales.

Some items rely heavily on discounts — pricing can be optimized.

Majority of customers fall in 19–35 and 36–60 age groups.

Express shipping users tend to spend more.

🛠️ Tech Stack
Tool	Use
Python	Data Cleaning & Preprocessing
Pandas / SQLAlchemy	ETL into MySQL
MySQL	Data Analysis & Querying
Power BI	Dashboard Visualization
Jupyter Notebook	Exploratory Data Analysis
