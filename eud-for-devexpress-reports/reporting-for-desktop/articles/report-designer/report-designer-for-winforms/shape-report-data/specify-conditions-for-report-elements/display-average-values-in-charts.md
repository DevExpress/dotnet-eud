---
title: Display Average Values in Charts
author: Margarita Zakhodyaeva
---
# Display Average Values in Charts

The following tutorial explains how to bind a chart’s constant line to an expression that calculates the average of all displayed values.

## Bind a Constant Line to an Expression

Select the **Chart** control. The “f” button appears next to the selection. Click this button to invoke the Expression Editor:

![Invoke the Expression Editor](~/eud-for-devexpress-reports/reporting-for-desktop/images/xrcontrol-invoke-the-expression-editor.png)

In the invoked editor, specify the following expression for the **Axis Value** property and click OK.

`[CategoriesProducts].Avg([UnitPrice])`

![Bind a constant line to an expression](~/eud-for-devexpress-reports/reporting-for-desktop/images/specify-expression-in-the-expression-editor.png)

## See the Result

Run the application. Constant lines show average product prices in each category.

![Result](~/eud-for-devexpress-reports/reporting-for-desktop/images/average-price-example.png)