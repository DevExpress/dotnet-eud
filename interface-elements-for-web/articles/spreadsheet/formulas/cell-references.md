---
title: Cell References
author: Anna Kondratova
legacyId: 18242
---
# Cell References

If you want to change data in a worksheet without changing formulas that use this data for evaluation, you can use **cell references**. A cell reference defines cell location in a worksheet. It is a combination of column letters (**A, B, C,** etc.) and row numbers (**1, 2, 3,** etc.). For example, **A1** refers to a cell at the intersection of column A and row 1.

To add values in cells A1 and A2, and divide the result by the value in cell A3, type the following formula (use parentheses to determine the order of operations):

**=(A1+A2)/A3**

You can also use a reference to a cell located in another worksheet. For example, to multiply a value in cell B1 by the value in cell B1 in _Sheet 2_, enter the following formula.

**=B1*Sheet2!B1**

To prevent data from changing when the formula is copied, use the **absolute reference**. Absolute references have a dollar sign ($) before column and/or row references.

The following example demonstrates how to use a constant value in cell B1 in calculations:

__=A1*$B$1__