# Day 7 – Excel Macros & VBA Basics

## Topics Covered
- Introduction to Macros
- Recording a Macro
- VBA Editor (Alt + F11)
- Creating and Running Macros
- Assigning Shortcut Keys
- Saving Workbook as .xlsm
- Save Spreadsheet as PDF using VBA
- Macro Security Basics

## VBA Code Learned

```vba
Sub SaveAsPDF()

    ActiveSheet.ExportAsFixedFormat _
        Type:=xlTypePDF, _
        Filename:=ThisWorkbook.Path & "\" & ActiveSheet.Name & ".pdf", _
        Quality:=xlQualityStandard, _
        IncludeDocProperties:=True, _
        IgnorePrintAreas:=False, _
        OpenAfterPublish:=True

End Sub
```

## Files
- Day7_Macros.xlsm
- Screenshots of Macro Recording
- PDF Output

## Key Shortcuts
- Alt + F11 → VBA Editor
- Alt + F8 → Run Macro
- Ctrl + Shift + ; → Current Time
- Ctrl + Shift + @ → Apply Time Format

## Learning Outcome
Created and executed Excel macros, worked with the VBA editor, and automated saving a worksheet as a PDF.
