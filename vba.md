# VBA for Excel

## Tools
* MS Excel (recommended 2016)
* Sublime Text 3 (with [VBScript](https://packagecontrol.io/packages/VBScript) package installed)

## Coding guidelines
* **Function**: A module defined for being called into any sheet in an excel workbook.
  - Open VB editor.
  - Insert >> Module
  - Code sample:
```vba
Function Area(x As Double, y As Double) As Double
Area = x * y
End Function
```

* **Sub** procedure: defined for a sheet in an excel workbook.
  - View project structure on the left panel of the editor.
  - select any sheet - "Sheet1".
  - insert this code below:
```vba
Private Sub CommandButton1_Click()
' find the area using a Area module
Dim z as Double
z = Area(2, 5) + 5
MsgBox(z)
End Sub
```

## Websites
* https://www.excel-easy.com/
* https://analystcave.com/
* My repo - https://github.com/abhi3700/vba_excel
* Cheatsheet - https://github.com/abhi3700/vba_excel/blob/master/vbasic_cheatsheet.pdf
