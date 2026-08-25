Employee Management System

Project Overview

Employee Management System is a simple MySQL database project used to store and manage employee information.

This project demonstrates basic SQL and DBMS concepts such as database creation, table creation, primary keys, unique constraints, NOT NULL constraints, INSERT, SELECT, UPDATE, DELETE, WHERE, GROUP BY, and aggregate functions.

Database

Database Name: employee_db

Table

The project contains one main table:

employee

Employee Table

The employee table stores basic information about employees.

Columns:

emp_id – Unique employee ID
emp_name – Employee name
email – Employee email address
salary – Employee salary
department – Employee department

Constraints Used

Primary Key:
The emp_id column uniquely identifies each employee.

NOT NULL:
The employee name cannot be empty.

UNIQUE:
Each employee must have a unique email address.

Sample Employees

Ayush – IT
Varun – HR
Sidhant – Finance
Rahul – Sales

SQL Operations

The project includes operations to:

Display all employees
Find employees based on salary
Count employees by department
Update employee salary
Delete employee records

Technologies Used

MySQL
SQL
MySQL Workbench
Git
GitHub

How to Run

Install MySQL or MySQL Workbench.
Open the SQL file.
Copy and execute the SQL code.
The employee_db database will be created.
Use SELECT queries to view the employee records.

Project Objective

The main objective of this project is to learn and practice basic SQL commands and database management concepts by creating a simple employee database.

Future Improvements

The project can be expanded by adding:

Department management
Employee attendance
Salary management
Leave management
Employee projects
Multiple tables
Foreign key relationships
Employee login system

Conclusion
This is a beginner-friendly MySQL Employee Management System suitable for learning SQL, practicing DBMS concepts, and showcasing a basic database project on GitHub.

## Database Normalization

The E-Commerce Database is normalized up to **Third Normal Form (3NF)**.

### 1. First Normal Form (1NF)

The database satisfies 1NF because all attributes contain **atomic values** and there are no repeating groups. Each table has a primary key that uniquely identifies every record.

For example, the `users` table stores individual values for `user_id`, `name`, `email`, and `city`. Similarly, product, order, and order item details are stored separately.

### 2. Second Normal Form (2NF)

The database satisfies 2NF because it is already in 1NF and there are **no partial dependencies**.

Each table uses a single-column primary key such as `user_id`, `product_id`, `order_id`, and `item_id`. Therefore, all non-key attributes depend completely on their respective primary key.

For example, in the `order_items` table, `quantity` and `unit_price` depend on the `item_id`.

### 3. Third Normal Form (3NF)

The database satisfies 3NF because it is already in 2NF and there are **no transitive dependencies**.

User details are stored only in the `users` table, product details are stored only in the `products` table, and order details are stored in the `orders` table. The `order_items` table uses `order_id` and `product_id` as foreign keys instead of duplicating user or product information.

This reduces data redundancy and maintains data consistency.

### Normalized Tables

- **Users:** `user_id (PK), name, email, city`
- **Products:** `product_id (PK), product_name, price, stock_quantity`
- **Orders:** `order_id (PK), user_id (FK), order_date, total_amount`
- **Order_Items:** `item_id (PK), order_id (FK), product_id (FK), quantity, unit_price`

### Relationships

- One **user** can have multiple **orders**.
- One **order** can contain multiple **order_items**.
- One **product** can appear in multiple **order_items**.
- `order_items` connects **orders** and **products**.

### Conclusion

The E-Commerce Database is normalized up to **3NF**, which helps reduce data redundancy, prevent insertion/update/deletion anomalies, and maintain data integrity.
