Day 7 – Excel Macros & VBA

## 📌 Topics Covered

- Excel Macros
- VBA
- Recording a Macro
- Running a Macro
- VBA Editor
- Sub and End Sub
- Range
- Cells
- AutoFit
- Excel automation
- Macro-enabled workbooks

---

# 1. What is a Macro?

A Macro is an automation tool in Excel that records or executes a series of repetitive tasks automatically.

Macros help save time and reduce manual effort.

### Example

Instead of manually:

- Formatting headers
- Applying borders
- Adjusting column width
- Adjusting row height

We can create a Macro to perform these tasks automatically.

---

# 2. What is VBA?

VBA stands for:

**Visual Basic for Applications**

VBA is the programming language used to create and control Excel Macros.

### Key Difference

**Macro = What gets automated**

**VBA = Language used to program/control the automation**

---

# 3. Recording a Macro

A Macro can be recorded using:

**Developer → Record Macro**

Example Macro name:

```text
FormatEmployeeData
```

After performing the required Excel actions:

**Developer → Stop Recording**

The recorded actions can then be run again automatically.

---

# 4. VBA Editor

The VBA Editor can be opened using:

```text
Alt + F11
```

It allows us to view, edit, and write VBA code.

---

# 5. Sub and End Sub

`Sub` and `End Sub` define the beginning and end of a VBA procedure.

Example:

```vba
Sub FormatData()

    Range("A1:J21").Columns.AutoFit

End Sub
```

- `Sub FormatData()` → starts the procedure
- Code between them → performs the required actions
- `End Sub` → ends the procedure

---

# 6. Range

`Range` refers to cells using Excel cell addresses.

Example:

```vba
Range("A1")
```

This refers to cell A1.

Example:

```vba
Range("A1:D10")
```

This refers to the range from A1 to D10.

---

# 7. Cells

The syntax of Cells is:

```vba
Cells(row, column)
```

Examples:

```vba
Cells(1,1)
```

→ A1

```vba
Cells(5,4)
```

→ D5

```vba
Cells(10,3)
```

→ C10

### Important

Remember:

**Cells(row, column)**

---

# 8. Range vs Cells

Both can refer to the same cell.

```vba
Range("A1")
```

and

```vba
Cells(1,1)
```

both refer to:

**A1**

However, `Cells()` is useful when working with variables and loops.

Example:

```vba
Cells(i,4)
```

This can refer to different rows in Column D depending on the value of `i`.

---

# 9. AutoFit

### Autofit Columns

```vba
Range("A1:D10").Columns.AutoFit
```

This automatically adjusts the width of columns A to D according to their contents.

### Autofit Rows

```vba
Range("A1:D10").Rows.AutoFit
```

This automatically adjusts the row height according to the contents.

---

# 10. Formatting Salary Column

To format the Salary column as a number:

```vba
Range("D:D").NumberFormat = "#,##0"
```

Example:

```text
150000
```

will be displayed as:

```text
150,000
```

---

# 11. Day 12 Practical Macro

Created a Macro to automate employee report formatting.

```vba
Sub CleanEmployeeReport()

    Range("A1:J1").Font.Bold = True
    Range("A:J").Columns.AutoFit
    Range("1:21").Rows.AutoFit
    Range("D:D").NumberFormat = "#,##0"
    Range("A1").Select

End Sub
```

### What this Macro does

1. Makes the header bold.
2. Autofits columns.
3. Autofits rows.
4. Formats the Salary column as numbers.
5. Selects cell A1 at the end.

---

# 12. Interview Questions

## Q1. What is a Macro?

A Macro is an automation tool in Excel that records or executes repetitive tasks automatically.

---

## Q2. What does VBA stand for?

VBA stands for **Visual Basic for Applications**.

It is a programming language used to create and control Excel Macros.

---

## Q3. What is the difference between a Macro and VBA?

A Macro is an automated sequence of tasks, while VBA is the programming language used to create and control those Macros.

---

## Q4. What is the purpose of Sub and End Sub?

`Sub` and `End Sub` define the beginning and end of a VBA procedure.

---

## Q5. What does this refer to?

```vba
Cells(5,4)
```

Answer:

```text
D5
```

Because the syntax is:

```text
Cells(row, column)
```

---

## Q6. What does this code do?

```vba
Range("A1:D10").Columns.AutoFit
```

Answer:

It automatically adjusts the width of columns A to D based on their contents.

---

## Q7. What is the difference between Range("A1") and Cells(1,1)?

Both refer to the same cell, A1.

`Range("A1")` uses the Excel cell address, while `Cells(1,1)` uses row and column numbers.

---

