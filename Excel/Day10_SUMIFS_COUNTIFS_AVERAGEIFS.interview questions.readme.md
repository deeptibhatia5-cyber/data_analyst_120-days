# Day 5 – Excel Interview Questions

## Topic
- SUMIFS()
- COUNTIFS()
- AVERAGEIFS()
- Multiple-condition analysis
- Comparison operators

---

## Q1. What is the difference between SUMIF() and SUMIFS()?

**Answer:**

SUMIF() calculates a sum based on a single condition.

SUMIFS() calculates a sum based on multiple conditions.

**Example:**

```excel
=SUMIF(C2:C21,"IT",D2:D21)
```

This calculates the total salary of IT employees.

```excel
=SUMIFS(D2:D21,C2:C21,"IT",D2:D21,">10000")
```

This calculates the total salary of IT employees earning more than 10,000.

---

## Q2. What is the syntax of COUNTIFS()?

**Answer:**

```excel
=COUNTIFS(criteria_range1,criteria1,criteria_range2,criteria2,...)
```

COUNTIFS() can be used with multiple criteria.

---

## Q3. What does COUNTIFS() do?

**Answer:**

COUNTIFS() counts the number of cells or records that satisfy multiple conditions.

**Example:**

```excel
=COUNTIFS(C2:C21,"IT",D2:D21,">10000")
```

This counts IT employees whose salary is greater than 10,000.

---

## Q4. What is the difference between AVERAGEIF() and AVERAGEIFS()?

**Answer:**

AVERAGEIF() calculates the average based on a single condition.

AVERAGEIFS() calculates the average based on multiple conditions.

**Example:**

```excel
=AVERAGEIF(C2:C21,"IT",D2:D21)
```

This calculates the average salary of IT employees.

```excel
=AVERAGEIFS(D2:D21,C2:C21,"IT",D2:D21,">10000")
```

This calculates the average salary of IT employees earning more than 10,000.

---

## Q5. Can SUMIFS() have more than two conditions?

**Answer:**

Yes. SUMIFS() can be used with multiple conditions.

For example:

```excel
=SUMIFS(D2:D21,C2:C21,"IT",D2:D21,">10000",E2:E21,"Joined")
```

This checks three conditions:

1. Department is IT
2. Salary is greater than 10,000
3. Joining Status is Joined

---

## Q6. What does "<>HR" mean?

**Answer:**

`<>HR` means **not equal to HR**.

For example:

```excel
=COUNTIF(C2:C21,"<>HR")
```

This counts employees whose department is not HR.

---

# Practical Exercises Completed

- Calculated total salary using SUMIFS()
- Counted employees using COUNTIFS()
- Calculated average salary using AVERAGEIFS()
- Applied multiple conditions
- Used comparison operators such as `>`, `<`, and `<>`
- Created business-oriented salary analysis

---

# Key Learning

| Function | Purpose |
|---|---|
| SUMIF() | Sum based on one condition |
| SUMIFS() | Sum based on multiple conditions |
| COUNTIF() | Count based on one condition |
| COUNTIFS() | Count based on multiple conditions |
| AVERAGEIF() | Average based on one condition |
| AVERAGEIFS() | Average based on multiple conditions |

### Important Rule

**IF = One condition**

**IFS = Multiple conditions**

---

# Day 5 Result

**Interview Score: 50/50**

**Status: Completed Successfully**
