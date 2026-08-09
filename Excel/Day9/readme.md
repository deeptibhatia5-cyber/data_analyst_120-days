# Day 9 – SQL Subqueries

## Topics Covered

* Introduction to SQL Subqueries
* Single-row subqueries
* Multiple-row subqueries
* Correlated subqueries
* Nested subqueries
* Subqueries in `SELECT`, `FROM`, and `WHERE` clauses
* Using `IN`, `EXISTS`, `ANY`, and `ALL` with subqueries

## Practice Queries

### 1. Find employees earning more than the average salary

```sql
SELECT employee_name, salary
FROM Employees
WHERE salary >
(
    SELECT AVG(salary)
    FROM Employees
);
```

### 2. Find employees working in the Sales department

```sql
SELECT employee_name
FROM Employees
WHERE department_id =
(
    SELECT department_id
    FROM Departments
    WHERE department_name = 'Sales'
);
```

### 3. Find employees whose salary matches any manager's salary

```sql
SELECT employee_name
FROM Employees
WHERE salary IN
(
    SELECT salary
    FROM Managers
);
```

### 4. Find departments that have employees

```sql
SELECT department_name
FROM Departments d
WHERE EXISTS
(
    SELECT 1
    FROM Employees e
    WHERE e.department_id = d.department_id
);
```

## Key Learning

* A subquery is a query written inside another SQL query.
* The inner query executes first, and its result is used by the outer query.
* Subqueries help solve complex filtering and comparison problems without creating temporary tables.
