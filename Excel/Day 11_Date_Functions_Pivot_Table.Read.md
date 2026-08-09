# Day 6 – Excel Date Functions & Pivot Tables

## 📌 Topics Covered

- TODAY()
- DAY()
- MONTH()
- YEAR()
- TEXT()
- Pivot Tables
- Aggregate functions in Pivot Tables
- KPI analysis
- Department-wise analysis
- Month-wise analysis
- Business insights

---

# 1. TODAY()

The `TODAY()` function returns the current date.

### Syntax

```excel
=TODAY()
```

### Example

If today's date is 09-08-2026:

```excel
=TODAY()
```

Result:

```text
09-08-2026
```

### Use Case

It can be used when we need the current date for reporting, age calculations, date comparisons, or daily dashboards.

---

# 2. DAY()

The `DAY()` function extracts the day number from a date.

### Syntax

```excel
=DAY(date)
```

### Example

If A2 contains:

```text
09-08-2026
```

Formula:

```excel
=DAY(A2)
```

Result:

```text
9
```

---

# 3. MONTH()

The `MONTH()` function extracts the month number from a date.

### Syntax

```excel
=MONTH(date)
```

### Example

If A2 contains:

```text
09-08-2026
```

Formula:

```excel
=MONTH(A2)
```

Result:

```text
8
```

8 represents August.

---

# 4. YEAR()

The `YEAR()` function extracts the year from a date.

### Syntax

```excel
=YEAR(date)
```

### Example

If A2 contains:

```text
09-08-2026
```

Formula:

```excel
=YEAR(A2)
```

Result:

```text
2026
```

---

# 5. TEXT()

The `TEXT()` function converts a date or number into text according to a specified format.

### Syntax

```excel
=TEXT(value,"format")
```

### Display Full Month Name

```excel
=TEXT(A2,"MMMM")
```

If A2 contains:

```text
09-08-2026
```

Result:

```text
August
```

### Display Short Month Name

```excel
=TEXT(A2,"MMM")
```

Result:

```text
Aug
```

### Important Note

`TEXT()` should normally be used with an actual Excel date when extracting a month name.

For example:

```excel
=TEXT(A2,"MMMM")
```

If A2 contains the actual date `09-08-2026`, the result is `August`.

---

# 6. Pivot Table

A Pivot Table is an Excel tool used to summarize and analyze large datasets quickly.

It allows us to perform calculations such as:

- SUM
- COUNT
- AVERAGE
- MIN
- MAX

It also allows us to analyze data by categories such as:

- Department
- Month
- Employee
- Product
- Region

---

# 7. Department-wise Pivot Table Analysis

I created a Pivot Table to analyze employee salary according to department.

| Department | Total Salary | Employees | Average Salary |
|---|---:|---:|---:|
| ADMIN | 164000 | 3 | 54667 |
| HR | 145000 | 5 | 29000 |
| IT | 186200 | 6 | 31033 |
| SALES | 104000 | 6 | 17333 |
| **Grand Total** | **599200** | **20** | **29960** |

---

# 8. Pivot Table Aggregate Functions

## SUM

SUM calculates the total of the selected values.

In a Pivot Table, placing Salary in the Values area and selecting SUM gives the total salary.

Example:

```text
Total Salary = 599200
```

---

## COUNT

COUNT counts the number of records or values.

Example:

```text
Number of Employees = 20
```

---

## AVERAGE

AVERAGE calculates the average of the selected values.

Example:

```text
Average Salary = 29960
```

---

# 9. KPI Analysis

I created KPI values from the employee dataset.

| KPI | Result |
|---|---:|
| Total Salary | 599200 |
| Average Salary | 29960 |
| Highest Salary | 150000 |
| Lowest Salary | 1200 |
| Number of Employees | 20 |

### Formulas Used

### Total Salary

```excel
=SUM(D2:D21)
```

### Average Salary

```excel
=AVERAGE(D2:D21)
```

### Highest Salary

```excel
=MAX(D2:D21)
```

### Lowest Salary

```excel
=MIN(D2:D21)
```

### Number of Employees

```excel
=COUNT(A2:A21)
```

---

# 10. Month-wise Employee Analysis

I created a Pivot Table to analyze the number of employees joining in each month.

| Month Number | Number of Employees |
|---:|---:|
| 1 | 2 |
| 3 | 1 |
| 4 | 2 |
| 5 | 1 |
| 6 | 2 |
| 7 | 4 |
| 8 | 2 |
| 9 | 3 |
| 10 | 1 |
| 11 | 1 |
| 12 | 1 |
| **Grand Total** | **20** |

### Business Insight

The highest number of employees joined in:

```text
July – 4 employees
```

---

# 11. Business Analysis

Pivot Tables help convert raw data into meaningful business information.

For example, from the employee dataset we can identify:

- Which department has the highest total salary?
- Which department has the most employees?
- Which department has the highest average salary?
- Which month has the highest employee joining count?
- What is the overall average salary?
- What is the highest and lowest salary?

### Key Findings

**Highest total salary department:**

IT – 186200

**Highest number of employees:**

IT and SALES – 6 employees each

**Highest average department salary:**

ADMIN – 54667

**Highest individual salary:**

150000

**Lowest individual salary:**

1200

**Total employees:**

20

---

# 12. Interview Questions

## Q1. What is TODAY()?

**Answer:**

TODAY() returns the current date.

---

## Q2. What does DAY() do?

**Answer:**

DAY() extracts the day number from a date.

Example:

```excel
=DAY(A2)
```

---

## Q3. What does MONTH() do?

**Answer:**

MONTH() extracts the month number from a date.

Example:

```excel
=MONTH(A2)
```

---

## Q4. What does YEAR() do?

**Answer:**

YEAR() extracts the year from a date.

Example:

```excel
=YEAR(A2)
```

---

## Q5. What is the use of TEXT()?

**Answer:**

TEXT() converts a value into text according to a specified format.

Example:

```excel
=TEXT(A2,"MMMM")
```

This can return the full month name.

---

## Q6. What is a Pivot Table?

**Answer:**

A Pivot Table is an Excel tool used to summarize and analyze large datasets quickly.

It can perform calculations such as SUM, COUNT, and AVERAGE.

---

## Q7. What is the difference between a normal table and a Pivot Table?

**Answer:**

A normal table displays raw or structured data, whereas a Pivot Table summarizes and analyzes the data based on selected fields.

---

## Q8. What are Values in a Pivot Table?

**Answer:**

The Values area contains the data on which calculations such as SUM, COUNT, and AVERAGE are performed.

---

## Q9. Can we calculate average salary using a Pivot Table?

**Answer:**

Yes. Add the Salary field to the Values area and change the calculation from SUM to AVERAGE.

---

## Q10. Why are Pivot Tables useful for Data Analysts?

**Answer:**

Pivot Tables help Data Analysts quickly summarize large datasets, identify trends, compare categories, calculate KPIs, and generate business insights.

---

# 13. Key Learning

### Date Functions

```text
TODAY()  → Current date
DAY()    → Day number
MONTH()  → Month number
YEAR()   → Year
TEXT()   → Formatted text
```

### Pivot Table

```text
Raw Data
   ↓
Pivot Table
   ↓
Summarization
   ↓
Analysis
   ↓
Business Insight
```

---

# 14. Skills Practiced

- Excel date functions
- Date extraction
- Date formatting
- Pivot Table creation
- SUM in Pivot Table
- COUNT in Pivot Table
- AVERAGE in Pivot Table
- KPI creation
- Business analysis
- Data summarization
- Extracting insights from data

---



| Topic | Status |
|---|---|
| TODAY() | ✅ Completed |
| DAY() | ✅ Completed |
| MONTH() | ✅ Completed |
| YEAR() | ✅ Completed |
| TEXT() | ✅ Completed |
| Pivot Tables | ✅ Completed |
| KPI Analysis | ✅ Completed |
| Business Insights | ✅ Completed |
| Interview Questions | ✅ Completed |



---



**Days Completed: 11 / 120

```text
Day 1 → Excel Basics ✅
Day 2 → Cell References & Basic Functions ✅
Day 3 → IF & Nested IF ✅
Day 4 → SUMIF, COUNTIF, AVERAGEIF ✅
Day 5 → SUMIFS, COUNTIFS, AVERAGEIFS ✅
Day 6 → Date Functions & Pivot Tables ✅
```

### Next Topic

## Day 12 – SQL Fundamentals

Topics:

- SELECT
- FROM
- WHERE
- DISTINCT
- ORDER BY
- TOP
- AND / OR / NOT
- Comparison Operators
- SQL Practice Dataset
- SQL Interview Questions
