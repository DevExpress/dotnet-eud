---
title: Calculate an Advanced Summary
author: Anna Vekhina
---
# Calculate an Advanced Summary

This document describes how to calculate an advanced summary for report groups using a built-in summary function and arithmetical or logical functions.

> [!Warning]
> Use the approach below if expression bindings **are enabled** in the Report Designer (the Designer provides the [Expressions](../../report-designer-tools/ui-panels/expressions-panel.md) panel).
>
> See [Calculate a Custom Summary](../shape-data-data-bindings/calculate-a-custom-summary.md) if expression bindings **are not enabled** in the Report Designer (the Designer does not provide the [Expressions](../../report-designer-tools/ui-panels/expressions-panel.md) panel).

1. [Create a new report](../../add-new-reports.md) or open an existing one and [bind it to a data source](../../bind-to-data.md).

2. Insert the [Group Header](../../introduction-to-banded-reports.md) band, select the **Group Fields** section in the **Actions** category and add a new group field to group the report's data by the required field. 

    ![](../../../../images/eurd-web-label-advanced-summary-group-data.png)

3. Drop a [Label](../../use-report-elements/use-basic-report-controls/label.md) onto the group footer to display the summary result. Expand the **Summary** section in the **Actions** category and set the **Running** property to **Group**.

    ![](../../../../images/eurd-web-label-advanced-summary-running.png)

4. Click the ellipsis button for the label's **Expression** property.

    ![](../../../../images/eurd-web-label-advanced-summary-expression-property.png)

5. This invokes the **Expression Editor** where you can specify a custom expression with the required summary functions and other logical or arithmetical functions. For example:

    ![](../../../../images/eurd-web-label-advanced-summary-expression-editor.png)

	> [!TIP]
	> See the [Expression Constants, Operators, and Functions](../../use-expressions/expression-syntax.md) topic for a complete list of supported summary functions.

6. You can use the **Text Format String** property to format the summary's value.
	
	![](../../../../images/eurd-web-label-advanced-summary-format-string.png)

Switch to [Print Preview](../../preview-print-and-export-reports.md) to see the result.

![](../../../../images/eurd-web-label-advanced-summary-result.png)