# SQL Time Intelligence Interview Practice

A focused SQL practice project designed for **Data Analyst interviews**, covering SQL Date & Time functions and real-world **Time Intelligence** problems.

The project uses a realistic **10-year e-commerce dataset (2016–2025)** with thousands of customers and orders to practice business-oriented SQL queries.

---

## 🎯 Objective

The goal of this repository is to build strong practical skills in SQL date/time analysis and prepare for commonly asked Data Analyst interview questions.

Topics covered include:

- Date & Time functions
- Date arithmetic
- MTD / QTD / YTD
- MoM / QoQ / YoY
- WoW / WTD
- Rolling time windows
- Previous/next period analysis
- Customer purchase behavior
- Consecutive periods
- Gaps & Islands
- Cohort analysis
- Retention analysis

---

## 🗄️ Database

**Database:** MySQL 8+

### Dataset

| Table | Approx. Rows | Description |
|---|---:|---|
| `customers` | 3,000 | Customer information and signup dates |
| `products` | 200 | Product and category information |
| `orders` | ~55,000 | Order transactions across 10 years |
| `order_items` | ~100,000+ | Products purchased in each order |

### Date Range

```text
2016-01-01 → 2025-12-31
```

The dataset contains multiple transactions throughout the day, including weekday/weekend variation, seasonal patterns, payments, deliveries, cancellations, and returns.

---

## 📊 Database Schema

```text
customers
    │
    │ customer_id
    ▼
orders
    │
    │ order_id
    ▼
order_items
    │
    │ product_id
    ▼
products
```

### Customers

```text
customer_id
first_name
last_name
email
city
state
signup_date
birth_date
gender
customer_segment
```

### Products

```text
product_id
product_name
category
price
launch_date
```

### Orders

```text
order_id
customer_id
order_date
order_datetime
payment_datetime
delivery_datetime
return_datetime
order_status
payment_status
shipping_method
total_amount
```

### Order Items

```text
order_item_id
order_id
product_id
quantity
unit_price
discount_percent
line_total
```

---

# 🔥 SQL Time Intelligence Topics

## 1. Date & Time Fundamentals

- Extract year, month, day, weekday and quarter
- Orders by weekday
- Orders by hour
- Date arithmetic
- Delivery duration
- First and last day of month
- Working with `DATE` and `DATETIME`

## 2. MTD / QTD / YTD

- Month-to-Date
- Quarter-to-Date
- Year-to-Date
- Last Year-to-Date
- MTD vs previous MTD
- YTD vs LYTD

## 3. Period-over-Period Analysis

- Month-over-Month (MoM)
- Quarter-over-Quarter (QoQ)
- Year-over-Year (YoY)
- Week-over-Week (WoW)
- Same period last year

## 4. Weekly Analysis

- Weekly sales
- Week-to-Date (WTD)
- Previous week comparison
- WoW growth

## 5. Rolling Windows

- Rolling 7-day sales
- Rolling 30-day sales
- Rolling averages
- Daily sales vs rolling average

## 6. Customer Time Analysis

- First purchase
- Second purchase
- Previous purchase
- Next purchase
- Days between purchases
- Customer inactivity
- Purchase frequency

## 7. Advanced SQL

- Consecutive months
- Consecutive purchase days
- Gaps & Islands
- Longest inactivity period
- Last N days of each month
- Business-day analysis

## 8. Cohort & Retention

- Customer cohort month
- Monthly retention
- Cohort-based customer analysis
- Retention by purchase month

---

# 📝 Interview Practice Questions

The repository focuses on 30 high-value interview questions.

### Fundamentals

1. Extract year, month, day, weekday, week number and quarter from each order.
2. Find the number of orders placed on each day of the week.
3. Find the number of orders placed during each hour of the day.
4. Calculate delivery time in days and hours.
5. Find the first and last day of each month.

### Time Intelligence

6. Calculate MTD sales.
7. Calculate QTD sales.
8. Calculate YTD sales.
9. Compare MTD sales with the previous month.
10. Compare YTD sales with LYTD.

### Period Comparison

11. Calculate monthly sales and previous month's sales.
12. Calculate MoM growth.
13. Calculate QoQ growth.
14. Calculate YoY growth.
15. Compare each month with the same month last year.

### Weekly Analysis

16. Calculate weekly sales.
17. Calculate WoW growth.
18. Calculate WTD sales.
19. Compare current WTD with previous WTD.

### Rolling Analysis

20. Calculate rolling 7-day sales.
21. Calculate rolling 30-day average sales.
22. Find days where sales exceed the previous 7-day average.

### Customer Analysis

23. Find first and second purchases.
24. Calculate days between consecutive purchases.
25. Find customers inactive for 90+ days.
26. Find customers purchasing in 3 consecutive months.

### Advanced

27. Find orders during the last 3 days of every month.
28. Find orders during the first 3 business days of every month.
29. Find the longest gap between customer purchases.
30. Build a monthly customer cohort retention analysis.

---

# 🧠 SQL Concepts Practiced

```text
SELECT
WHERE
GROUP BY
ORDER BY
HAVING
CASE
DATE functions
DATETIME functions
DATE arithmetic
CTEs
Subqueries
Window Functions
LAG()
LEAD()
ROW_NUMBER()
RANK()
SUM() OVER()
AVG() OVER()
PARTITION BY
ORDER BY
ROWS BETWEEN
Conditional aggregation
Gaps & Islands
Cohort analysis
```

---

# 🛠️ Tools

- MySQL 8+
- SQL
- Python
- Git & GitHub

Python is used only to generate the large synthetic dataset.

---

# 📁 Project Structure

```text
sql-time-intelligence-interview-practice/
│
├── data/
│   └── sql_date_time_interview_dataset.sql
│
├── python/
│   └── generate_sql_data.py
│
├── questions/
│   └── time_intelligence_questions.sql
│
├── solutions/
│   └── time_intelligence_solutions.sql
│
└── README.md
```

---

# 🚀 Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/raghu9189/sql-time-intelligence-interview-practice.git
```

### 2. Open MySQL

```sql
CREATE DATABASE sql_interview_practice;
```

### 3. Import the dataset

Run:

```text
data/sql_date_time_interview_dataset.sql
```

### 4. Start practicing

Open:

```text
questions/time_intelligence_questions.sql
```

Try solving each problem before checking the solutions.

---

# 📈 Difficulty Levels

| Level | Focus |
|---|---|
| 🟢 Beginner | Date extraction & basic date functions |
| 🟡 Intermediate | MTD, QTD, YTD, MoM, QoQ, YoY |
| 🟠 Advanced | Rolling windows & customer analysis |
| 🔴 Expert | Gaps & Islands, business days, cohorts |

---

# 🎯 Interview Focus

This project emphasizes **business-oriented SQL**, not just syntax.

The main goal is to understand how SQL is used to answer questions such as:

```text
How much did sales grow MoM?

How are we performing compared with last year?

What are our current YTD sales?

Which customers are becoming inactive?

What was the highest-selling 7-day period?

Which customers purchased in consecutive months?

How long does it take customers to purchase again?

How many customers were retained after their first purchase?
```

---

## 👨‍💻 Author

**Raghu**

Data Analyst | Data Engineer

Focused on SQL, Python, Data Analytics, Data Engineering, ETL and Business Intelligence.

---

⭐ If this project helps with your SQL interview preparation, consider starring the repository.
