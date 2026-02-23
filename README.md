# Task 7: Basic Sales Summary using SQLite and Python

## 📌 Objective
The objective of this task is to use SQL queries inside Python to extract basic sales information such as total quantity sold and total revenue from a small SQLite database, and display the results using print statements and a simple bar chart.

---

## 🛠 Tools & Technologies Used
- Python
- SQLite (sqlite3)
- Pandas
- Matplotlib
- VS Code

---

## 📂 Project Structure

Task7_SQLite_Sales/
│
├── sales_data.db # SQLite database file
├── task7_sales_summary.py # Python script
├── sales_chart.png # Revenue bar chart output
└── README.md # Project documentation


---

## 🗄 Database Details
- **Database Name:** sales_data.db  
- **Table Name:** sales  

### Table Columns:
- product (TEXT)
- quantity (INTEGER)
- price (REAL)

---

## 📊 SQL Query Used
```sql
SELECT product,
       SUM(quantity) AS total_qty,
       SUM(quantity * price) AS revenue
FROM sales
GROUP BY product;
