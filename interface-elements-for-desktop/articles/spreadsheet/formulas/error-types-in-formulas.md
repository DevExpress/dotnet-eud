---
title: Error Types in Formulas
author: Natalya Senichkina
legacyId: 15773
---
# Error Types in Formulas
If a formula in a cell cannot be calculated correctly, it means that the cell contains an **error**. The error appears because the formula's syntax is incorrect, or the formula uses unexpected arguments or data types.

Errors that occur in formulas are detailed in the following table:

| Error | Description | Example |
|---|---|---|
| **#####** | The column is not wide enough to display the cell content. |  |
| **#DIV/0!** | Division by zero. | **=A1/B1** (where the value in cell B1 is equal to zero, or cell B1 is blank). |
| **#NAME?** | The formula refers to a name that doesn't exist or is spelled incorrectly. | **=SUM(Values)** (the cell range named "Values" does not exist). |
| **#N/A** | The referenced value is not available to the formula. | **=SUM(A1:A5*B1:B3)** (the array formula has arguments consisting of different numbers of elements). |
| **#NULL!** | An incorrect range operator is used in the formula, or the specified intersection includes two ranges that do not intersect. | **=SUM(A1 A3)** (a colon is missing in the cell range reference). |
| **#NUM!** | There are invalid numeric values in the formula. | **=SQRT(-4)** (the square root of a negative number cannot be calculated). |
| **#REF!** | The cell reference is not valid. | **=SUM(A1, B1)** (column B has been deleted). |
| **#VALUE!** | The formula uses values of the wrong data type. | **=SUM(5, "Text")** (the SUM function requires numeric arguments). |