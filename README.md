# 🏦 Banking Database Management System (MySQL)
## 📌 Project Overview
The **Banking Database Management System** is a SQL-based project developed using MySQL to manage banking operations such as customer information, bank branches, account details, and financial transactions.
The project demonstrates core SQL concepts, including database creation, table relationships, joins, subqueries, aggregate functions, views, stored procedures, and triggers. It also implements basic transaction handling and data integrity constraints.

## 🎯 Objectives
- Manage customer, branch, account, and transaction information efficiently.
- Maintain relationships between tables using primary and foreign keys.
- Perform banking data analysis using SQL queries.
- Automate operations using stored procedures and triggers.
- Maintain data integrity through constraints and transaction handling.

## 🛠️ Technologies Used
- **Database:** MySQL
- **Development Tool:** MySQL Workbench
- **Language:** SQL

## 🗂️ Database Structure
The project contains the following tables:

| Table Name | Description |
|---|---|
| `Branches` | Stores branch names, locations, and IFSC codes. |
| `Customers` | Stores customer details, including names, phone numbers, email addresses, and addresses. |
| `Account_Types` | Stores account types such as Savings and Current. |
| `Accounts` | Stores account numbers, balances, opening dates, and account statuses. |
| `Transactions` | Stores deposit, withdrawal, and transfer transaction records. |
| `Transaction_Log` | Records newly inserted transactions through a trigger. |

## ⚙️ Features
### 1. Database and Table Management
- Create and manage the banking database.
- Define primary keys and foreign key relationships.
- Apply constraints to maintain valid account balances, transaction amounts, and account statuses.

### 2. SQL Queries and Data Analysis
- Retrieve customer and account information.
- Display active and inactive accounts.
- Find accounts with the highest balances.
- Calculate total deposits and withdrawals.
- Generate branch-wise account balances and customer counts.
- Generate monthly transaction summaries.
- Identify customers with multiple accounts.
- Retrieve the latest transactions for each account.

### 3. Views
- Create the `Active_Account_Details` view to display active accounts along with customer, account type, and branch information.

### 4. Stored Procedures
- **`Transfer_Money`** — Transfers money between accounts after validating transfer details and available balance.
- **`Get_Customer_Accounts`** — Retrieves all accounts associated with a customer.
- **`Get_Account_Transactions`** — Retrieves transaction history for a specified account.

### 5. Triggers
- **`trg_log_new_transaction`** — Automatically logs newly inserted transactions in the `Transaction_Log` table.
- **`trg_prevent_negative_balance`** — Prevents account balances from being updated to negative values.

## 🚀 How to Run the Project
1. Install MySQL Server and MySQL Workbench.
2. Clone or download this repository.
3. Open MySQL Workbench and connect to your MySQL server.
4. Open the project SQL script.
5. Execute the database creation and table creation statements first.
6. Insert the sample data into the tables.
7. Execute the SQL queries and create the view.
8. Create the stored procedures and triggers using the SQL editor.
9. Run the `CALL` statements to test the stored procedures.
10. Test the triggers by inserting a new transaction and attempting an update with a negative account balance.

**Note:** Create stored procedures and triggers before executing the statements that call or test them. Run the SQL script in the correct order to avoid dependency errors.

## 💡 SQL Concepts Demonstrated
- DDL (Data Definition Language)
- DML (Data Manipulation Language)
- Joins and subqueries
- Aggregate functions
- Grouping and sorting
- Views
- Stored procedures
- Triggers
- Transactions and rollback handling
- Primary keys and foreign keys
- Data integrity constraints

## 🔒 Data Integrity and Transaction Handling
The project uses primary keys, foreign keys, `CHECK` constraints, and stored procedure validation to maintain data consistency. The money transfer procedure uses transaction handling to commit successful transfers or roll back changes when an SQL exception occurs.
The trigger-based logging mechanism maintains a record of newly inserted transactions.

## 📚 Learning Outcomes
Through this project, I gained practical experience in:
- Designing relational databases.
- Writing and executing complex SQL queries.
- Implementing stored procedures and triggers.
- Understanding transaction management.
- Enforcing data integrity using constraints.
- Analyzing banking data through aggregate queries and views.

## 🔮 Future Enhancements
- Add user authentication and role-based access control.
- Implement fund transfers with detailed transaction records.
- Add transaction history reports and account statements.
- Develop a web-based interface for banking operations.
- Integrate reporting dashboards for financial analysis.
