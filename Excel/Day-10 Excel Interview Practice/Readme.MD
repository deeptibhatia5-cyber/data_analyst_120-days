# Day 2 – Excel Interview Questions

## Topic
- Relative Cell Reference
- Absolute Cell Reference
- SUM()
- COUNT()
- COUNTA()
- AVERAGE()

---

## Q1. What is the difference between Relative and Absolute Cell References?

**Answer:**
A Relative Cell Reference changes automatically when a formula is copied to another cell.
An Absolute Cell Reference remains fixed by using the `$` symbol (e.g., `$A$1`).

---

## Q2. When do we use an Absolute Cell Reference?

**Answer:**
We use an Absolute Cell Reference when a value should remain constant in every formula, such as a tax rate, bonus percentage, GST, or discount percentage.

---

## Q3. What does the SUM() function do?

**Answer:**
The SUM() function adds all the numbers in a selected range.

**Example:**
```excel
=SUM(D2:D21)
```

---

## Q4. What is the difference between COUNT() and COUNTA()?

**Answer:**
- COUNT() counts only numeric values.
- COUNTA() counts all non-empty cells, including numbers, text, and dates.

---

## Q5. What does the AVERAGE() function do?

**Answer:**
The AVERAGE() function calculates the arithmetic mean of a range of numbers.

**Example:**
```excel
=AVERAGE(D2:D21)
```

---

## Practical Exercise Completed
- Created Employee dataset
- Used Absolute Reference for Bonus calculation
- Calculated Total Salary
- Calculated Average Salary
- Found Highest Salary
- Found Lowest Salary
- Counted Number of Employees

## Skills Learned
- Relative Cell Reference
- Absolute Cell Reference
- SUM()
- AVERAGE()
- MAX()
- MIN()
- COUNT()
- RANDBETWEEN()
