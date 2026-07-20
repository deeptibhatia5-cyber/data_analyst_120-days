# Day 8 – SQL Installation & Basic SQL Commands

## Topics Covered
- Installed Microsoft SQL Server 2025 Express Edition
- Installed SQL Server Management Studio (SSMS)
- Connected to SQL Server
- Created a new database
- Created a table
- Inserted records using the INSERT statement
- Learned basic SQL syntax

## SQL Commands Practiced
- CREATE DATABASE
- USE
- CREATE TABLE
- INSERT INTO
- SELECT

## Sample Code

### Create Database
```sql
CREATE DATABASE PracticeDB;
```

### Use Database
```sql
USE PracticeDB;
```

### Create Table
```sql
CREATE TABLE Employees (
    EmployeeID INT PRIMARY KEY,
    EmployeeName VARCHAR(50),
    Department VARCHAR(30),
    Salary DECIMAL(10,2)
);
```

### Insert Data
```sql
INSERT INTO Employees
VALUES
(101,'Rahul','IT',45000),
(102,'Priya','HR',38000),
(103,'Amit','Finance',52000);
```

### View Data
```sql
SELECT * FROM Employees;
```

## Key Learnings
- Understanding databases and tables
- Difference between DDL and DML commands
- Creating tables with appropriate data types
- Inserting multiple records into a table
