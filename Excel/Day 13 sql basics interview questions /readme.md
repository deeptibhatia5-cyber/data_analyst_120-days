# Day 13 – SQL Fundamentals

## 📌 Topics Covered

- SELECT
- SELECT *
- FROM
- DISTINCT
- WHERE
- Comparison Operators
- AND
- OR
- NOT
- ORDER BY
- ASC
- DESC
- TOP
- SQL Interview Questions

---

# 1. SELECT

`SELECT` is used to retrieve or display data from one or more columns of a table.

### Example

```sql
SELECT name
FROM employees;
```

This retrieves the `name` column from the employees table.

### Multiple Columns

```sql
SELECT name, department, salary
FROM employees;
```

---

# 2. SELECT *

`SELECT *` is used to retrieve all columns from a table.

### Example

```sql
SELECT *
FROM employees;
```

This returns all columns and all rows from the employees table.

---

# 3. FROM

`FROM` specifies the table from which SQL should retrieve the data.

### Example

```sql
SELECT name, salary
FROM employees;
```

Here:

- `SELECT` → specifies what data we want
- `FROM` → specifies where the data comes from
- `employees` → table containing the data

---

# 4. DISTINCT

`DISTINCT` is used to return unique values and eliminate duplicate results.

### Example

```sql
SELECT DISTINCT department
FROM employees;
```

If the department column contains:

```text
IT
HR
IT
Sales
HR
```

The result will be:

```text
IT
HR
Sales
```

---

# 5. WHERE

`WHERE` is a filtering clause used to retrieve rows based on a specified condition.

### Example

```sql
SELECT *
FROM employees
WHERE salary > 50000;
```

This retrieves only employees whose salary is greater than 50,000.

### Important

`WHERE` filters **rows**.

---

# 6. Comparison Operators

| Operator | Meaning |
|---|---|
| `=` | Equal to |
| `<>` | Not equal to |
| `>` | Greater than |
| `<` | Less than |
| `>=` | Greater than or equal to |
| `<=` | Less than or equal to |

### Example

```sql
SELECT *
FROM employees
WHERE salary > 50000;
```

---

# 7. AND Operator

`AND` is used when all specified conditions must be true.

### Example

```sql
SELECT *
FROM employees
WHERE department = 'IT'
AND salary > 50000;
```

Both conditions must be satisfied:

1. Department must be IT.
2. Salary must be greater than 50,000.

---

# 8. OR Operator

`OR` is used when at least one of the conditions must be true.

### Example

```sql
SELECT *
FROM employees
WHERE department = 'IT'
OR department = 'HR';
```

This retrieves employees from either IT or HR.

---

# 9. NOT Operator

`NOT` reverses a condition.

### Example

```sql
SELECT *
FROM employees
WHERE NOT department = 'HR';
```

This retrieves employees who are not from HR.

The following is also commonly used:

```sql
SELECT *
FROM employees
WHERE department <> 'HR';
```

---

# 10. ORDER BY

`ORDER BY` is used to sort the result of a query.

## Ascending Order

```sql
SELECT name, salary
FROM employees
ORDER BY salary ASC;
```

This arranges salaries from lowest to highest.

## Descending Order

```sql
SELECT name, salary
FROM employees
ORDER BY salary DESC;
```

This arranges salaries from highest to lowest.

### Remember

```text
ASC  → Ascending
DESC → Descending
```

---

# 11. TOP

`TOP` is used in SQL Server to limit the number of rows returned.

### Example

To find the 5 highest salaries:

```sql
SELECT TOP 5 salary
FROM employees
ORDER BY salary DESC;
```

To find the top 5 highest-paid employees:

```sql
SELECT TOP 5 name, salary
FROM employees
ORDER BY salary DESC;
```

### Important

`TOP 5` alone does not mean the 5 highest salaries.

We need:

```sql
ORDER BY salary DESC
```

to arrange the highest salaries first.

---

# 12. SQL Practical Queries

## Display all employees

```sql
SELECT *
FROM employees;
```

## Display specific columns

```sql
SELECT name, department, salary
FROM employees;
```

## Display unique departments

```sql
SELECT DISTINCT department
FROM employees;
```

## Find IT employees

```sql
SELECT *
FROM employees
WHERE department = 'IT';
```

## Find employees earning more than 50,000

```sql
SELECT *
FROM employees
WHERE salary > 50000;
```

## Find IT employees earning more than 50,000

```sql
SELECT *
FROM employees
WHERE department = 'IT'
AND salary > 50000;
```

## Find employees who are not from HR

```sql
SELECT *
FROM employees
WHERE department <> 'HR';
```

## Find employees from IT or HR

```sql
SELECT *
FROM employees
WHERE department = 'IT'
OR department = 'HR';
```

## Sort employees by salary from highest to lowest

```sql
SELECT *
FROM employees
ORDER BY salary DESC;
```

## Find the top 5 highest salaries

```sql
SELECT TOP 5 salary
FROM employees
ORDER BY salary DESC;
```

---

# 13. Important SQL Concepts

### SELECT vs WHERE

```text
SELECT → chooses columns
WHERE  → filters rows
```

### WHERE vs ORDER BY

```text
WHERE      → filters records based on a condition
ORDER BY   → sorts the result
```

### AND vs OR

```text
AND → both conditions must be TRUE
OR  → at least one condition must be TRUE
```

---

# 14. Interview Questions

## Q1. What is SELECT?

`SELECT` is used to retrieve or display data from one or more columns of a table.

---

## Q2. What does SELECT * mean?

`SELECT *` retrieves all columns from a table.

---

## Q3. What is the purpose of FROM?

`FROM` specifies the table from which SQL should retrieve the data.

---

## Q4. What is DISTINCT?

`DISTINCT` returns unique values and eliminates duplicate results.

---

## Q5. What is WHERE?

`WHERE` is a filtering clause used to retrieve only rows that satisfy a specified condition.

---

## Q6. What is the difference between AND and OR?

`AND` requires all conditions to be true, whereas `OR` requires at least one condition to be true.

---

## Q7. What does <> mean?

`<>` means **not equal to**.

Example:

```sql
WHERE department <> 'HR'
```

---

## Q8. What is the difference between ASC and DESC?

`ASC` represents ascending order, while `DESC` represents descending order.

---

## Q9. How do you find the top 5 highest salaries?

```sql
SELECT TOP 5 salary
FROM employees
ORDER BY salary DESC;
```

---

## Q10. What is the difference between WHERE and ORDER BY?

`WHERE` filters rows based on a condition, whereas `ORDER BY` arranges the result in ascending or descending order.

---

# 15. Day 13 Interview Performance

| Question | Score |
|---|---:|
| SELECT | 9/10 |
| SELECT * | 10/10 |
| FROM | 10/10 |
| DISTINCT | 10/10 |
| WHERE | 10/10 |
| AND / OR | 10/10 |
| `<>` | 10/10 |
| ASC / DESC | 10/10 |
| TOP 5 | 10/10 |
| WHERE vs ORDER BY | 10/10 |
| **Total** | **99/100** |
| **Percentage** | **99%** |

---

# 🧠 Day 13 Key Takeaways

```text
SELECT   → Choose columns
FROM     → Choose table
WHERE    → Filter rows
DISTINCT → Remove duplicate results
AND      → All conditions must be true
OR       → At least one condition must be true
NOT      → Reverse a condition
ORDER BY → Sort results
ASC      → Lowest to highest
DESC     → Highest to lowest
TOP      → Limit returned rows
```

---

