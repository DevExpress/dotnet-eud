---
title: Calculate a Weighted Average
author: Anna Gubareva
---
# Calculate a Weighted Average

![](../../../../../images/eurd-win-weighted-average-result.png)

## <a name="summaryfunctions"></a>Use Report Summary Functions (Recommended)

You can calculate a weighted average at report level by specifying a control's expression using several built-in report summary functions.

> [!NOTE]
> You can use this approach if expression bindings **are enabled** in the Report Designer (the [Property Grid](../../report-designer-tools/ui-panels/property-grid.md) provides the **Expressions** ![](../../../../../images/eurd-win-property-grid-expressions-icon.png) tab).
> 
> See the next document sections to learn about alternative approaches.

1. [Open an existing report](../../open-reports.md) or [create a new one from scratch](../../add-new-reports.md).
2. [Bind a report](../../bind-to-data.md) to a required data source. 
3. [Group the report's data](../../shape-report-data/group-and-sort-data/group-data.md) using the [Group and Sort Panel](../../report-designer-tools/ui-panels/group-and-sort-panel.md) and construct a layout like the following:
	
	![](../../../../../images/eurd-win-weighted-average-group-data.png)

4. Add the [Group Footer](../../introduction-to-banded-reports.md) band to the report and drop a [Label](../../use-report-elements/use-basic-report-controls/label.md) control on this band to display the summary result.	Click the label's smart tag, then click the Summary field's ellipsis button.
	
	![](../../../../../images/eurd-win-weighted-average-summary-running.png)

5. In the invoked **Summary Editor** window:
    * Set the **Summary Running** property to **Group**.
    * Set the **Summary Function** property to **Weighed average**.
    * Set the **Argument Expression** property to the field to count the weighted average on, and the **Weight** property to the field that provides weights.
	
	![](../../../../../images/eurd-win-weighted-average-summary-expression.png)

6. You can also use the control's **Format String** property to format the summary value. For instance, set this property to **Weighted Average Price: {0:c2}**.
