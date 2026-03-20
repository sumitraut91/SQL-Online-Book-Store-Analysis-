# 📚 Online Book Store — SQL Analysis Project

A beginner-to-intermediate SQL project built using **PostgreSQL** to analyze an online book store database. The project covers database design, data import, and solving real-world business queries ranging from basic to advanced.

---

## 🗂️ Database Schema

The project uses **3 tables** connected via common key columns:

### Books
| Column | Type |
|---|---|
| Book_ID | SERIAL PRIMARY KEY |
| Title | VARCHAR(100) |
| Author | VARCHAR(100) |
| Genre | VARCHAR(50) |
| Published_Year | INT |
| Price | NUMERIC(10,2) |
| Stock | INT |

### Customers
| Column | Type |
|---|---|
| Customer_ID | SERIAL PRIMARY KEY |
| Name | VARCHAR(100) |
| Email | VARCHAR(100) |
| Phone | VARCHAR(15) |
| City | VARCHAR(50) |
| Country | VARCHAR(150) |

### Orders
| Column | Type |
|---|---|
| Order_ID | SERIAL PRIMARY KEY |
| Customer_ID | INT (FK → Customers) |
| Book_ID | INT (FK → Books) |
| Order_Date | DATE |
| Quantity | INT |
| Total_Amount | NUMERIC(10,2) |

---

## 📁 Project Files

```
📦 Online-Book-Store-SQL
 ┣ 📄 Online_Book_Store_Analysis.sql   # All SQL queries (DDL + DML + Analysis)
 ┣ 📊 Books.csv                        # Books dataset
 ┣ 📊 Customers.csv                    # Customers dataset
 ┣ 📊 Orders.csv                       # Orders dataset
 ┗ 📄 README.md
```

---

## 🔍 Queries Covered

### ✅ Basic Queries
1. Retrieve all books in the **"Fiction"** genre
2. Find books published **after the year 1950**
3. List all customers from **Canada**
4. Show orders placed in **November 2023**
5. Retrieve the **total stock** of books available
6. Find the details of the **most expensive book**
7. Show all customers who ordered **more than 1 quantity** of a book
8. Retrieve all orders where the **total amount exceeds $20**
9. List all **distinct genres** available in the Books table
10. Find the book with the **lowest stock**
11. Calculate the **total revenue** generated from all orders

### ⚡ Advanced Queries
1. Total number of books sold **per genre**
2. Average price of books in the **"Fantasy"** genre
3. Customers who have placed **at least 2 orders**
4. The **most frequently ordered** book
5. Top 3 most expensive books in the **'Fantasy'** genre
6. Total quantity of books sold **by each author**
7. Cities where customers who spent **over $30** are located
8. The customer who **spent the most** on orders

---

## 🛠️ Tools & Technologies

- **Database:** PostgreSQL
- **Language:** SQL
- **Concepts Used:** DDL, DML, Aggregate Functions, JOINs, GROUP BY, HAVING, Subqueries, ORDER BY, LIMIT

---

## 🚀 How to Run

1. Open **pgAdmin** or any PostgreSQL client (e.g., psql, DBeaver)
2. Create a new database:
   ```sql
   CREATE DATABASE online_book_store;
   ```
3. Run the `Online_Book_Store_Analysis.sql` file to create tables
4. Update the file paths in the `COPY` commands to match your local CSV file locations:
   ```sql
   COPY Books FROM 'your/local/path/Books.csv' CSV HEADER;
   ```
5. Execute the queries one by one or all at once to explore the results

---

## 💡 Key Learnings

- Designing a relational database with primary and foreign key constraints
- Using `JOIN` to connect multiple tables for meaningful insights
- Applying aggregate functions (`SUM`, `AVG`, `COUNT`) with `GROUP BY` and `HAVING`
- Filtering data with `WHERE`, `BETWEEN`, and `DISTINCT`
- Writing subqueries to calculate derived metrics like remaining stock

---

## 📬 Connect

Feel free to fork this project, raise issues, or suggest improvements. Happy querying! 🎯
