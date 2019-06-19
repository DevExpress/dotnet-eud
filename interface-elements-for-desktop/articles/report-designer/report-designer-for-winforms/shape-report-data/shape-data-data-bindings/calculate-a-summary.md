---
title: Calculate a Summary
author: Anna Gubareva
---
# Calculate a Summary

This tutorial describes the steps required to calculate one of the built-in summary functions in your report.

> [!NOTE]
> Use this approach if data bindings **are enabled** in the Report Designer (the Label's smart tag includes the **Data Binding** property).
>
> ![](../../../../../images/eurd-label-expression-binding-modes.png)
>
> See the [Calculate a Summary](../shape-data-expression-bindings/calculate-a-summary.md) topic in the [Shape Data (Expression Bindings)](../shape-data-expression-bindings.md) section to learn about an alternative approach.

1. [Create a new report](../../add-new-reports.md) or open an existing one and [bind it to a data source](../../bind-to-data.md).

2. Switch to the [Group and Sort](../../report-designer-tools/ui-panels/group-and-sort-panel.md) panel and group the report's data by the required field. Display the footer for the created group.

    ![](../../../../../images/eurd-win-label-summary-group-data.png)

3. Prepare the report layout and drop a required data field onto the group footer to display the summary result.

4. Click the label's smart tag and invoke its **Summary Running** drop-down list. Select the range for which to calculate a summary (the entire report, a specific report group or document page).
	
	![](../../../../../images/eurd-win-label-legacy-summary-running-group.png)

5. Set the **Summary Func** property to **Sum** and use the **Format String** property to format the summary's value.

	![](../../../../../images/eurd-win-label-legacy-summary-settings.png)
	

Switch to [Print Preview](../../preview-print-and-export-reports.md) to see the result.

![](../../../../../images/eurd-win-label-summary-result.png)