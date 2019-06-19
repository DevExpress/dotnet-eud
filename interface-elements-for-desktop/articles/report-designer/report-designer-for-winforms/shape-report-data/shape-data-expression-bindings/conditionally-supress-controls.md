---
title: Conditionally Suppress Controls
author: Anna Gubareva
---
# Conditionally Suppress Controls

This document describes how to display or hide a report control in a published document based on a specified logical condition.

> [!NOTE]
> Use this approach if expressions **are enabled** in the Report Designer (the Label's smart tag includes the **Expression** property).
>
> ![](../../../../../images/eurd-label-expression-binding-modes.png)

> See the [Conditionally Suppress Controls](../shape-data-data-bindings/conditionally-supress-controls.md) topic in the [Shape Data (Data Bindings)](../shape-data-data-bindings.md) section to learn about an alternative approach.

1. [Create a new report](../../add-new-reports.md) or open an existing one and prepare the report layout.

    ![](../../../../../images/eurd-win-shaping-suppress-initial-layout.png)

2. Select the required control and switch to the [Property Grid](../../report-designer-tools/ui-panels/property-grid.md). Open the **Behavior** tab, click the **Visible** property's marker and select **Visible Expression** in the context menu.

    ![](../../../../../images/eurd-win-shaping-suppress-visible-property.png)

3. In the invoked **Expression Editor**, specify the required [expression](../../use-expressions.md).
	
	![](../../../../../images/eurd-win-shaping-suppress-expression.png)
	
	Use the **Iif** function to define the required condition. For example:
	
	**Iif([Discontinued] == False, False, [Discontinued])**
	
	This expression means that if the data field's value is **False**, the control's **Visible** property is disabled.

When switching to [Print Preview](../../preview-print-and-export-reports.md), you can view the report control's visibility changes according to the assigned condition.

![](../../../../../images/eurd-win-shaping-suppress-result.png)

> [!Note]
> See [Hide Table Cells](../../use-report-elements/use-tables/hide-table-cells.md) to learn how to conditionally suppress table cells and define the mode for processing them.