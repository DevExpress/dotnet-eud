---
title: Conditionally Suppress Controls
author: Anna Vekhina
---
# Conditionally Suppress Controls

This document describes how to display or hide a report control in a published document based on a specified logical condition.

1. [Create a new report](../../add-new-reports.md) or open an existing one and prepare the report layout.

2. Select the required control, switch to the [Expressions](../../report-designer-tools/ui-panels/expressions-panel.md) panel and click the **Visible** property's ellipsis button. 

    ![](../../../../images/eurd-web-shaping-check-box-visible-property.png)

3. In the invoked [Expression Editor](../../report-designer-tools/expression-editor.md), specify the required [expression](../../use-expressions.md).
	
	![](../../../../images/eurd-web-shaping-suppress-expression.png)
	
	Use the **Iif** function to define the required condition. For example:
	
	**Iif([Discontinued] == False, False, [Discontinued])**
	
	This expression means that if the data field's value is **False**, the control's **Visible** property's value is also **False**.

When switching to [Print Preview](../../preview-print-and-export-reports.md), you can view the report control's visibility changes according to the assigned condition.

![](../../../../images/eurd-web-shaping-suppress-result.png)

> [!Note]
> See [Hide Table Cells](../../use-report-elements/use-tables/hide-table-cells.md) to learn how to conditionally suppress table cells and define the mode for processing them.