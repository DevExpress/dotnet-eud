---
title: Calculate a Summary
author: Anna Vekhina
---
# Calculate a Summary

This tutorial describes the steps required to calculate one of the built-in summary functions in your report.

> [!Warning]
> Use the approach below if expression bindings **are not enabled** in the Report Designer (the Designer does not provide the [Expressions](../../report-designer-tools/ui-panels/expressions-panel.md) panel).
>
> See [Calculate a Summary](../shape-data-expression-bindings/calculate-a-summary.md) if expression bindings **are enabled** in the Report Designer (the Designer provides the [Expressions](../../report-designer-tools/ui-panels/expressions-panel.md) panel).

1. [Create a new report](../../add-new-reports.md) or open an existing one and [bind it to a data source](../../bind-to-data.md).

2. Insert the [Group Header](../../introduction-to-banded-reports.md) band, select the **Group Fields** section in the **Actions** category and add a new group field to group the report's data by the required field. 

    ![](../../../../images/eurd-web-label-legacy-summary-group-data.png)

3. Insert the Group Footer band. Prepare the report layout and drop a required data field onto the group footer to display the summary result.

4. Select the label, expand the **Summary** section in the **Actions** category and invoke the **Running** drop-down list. Select the range for which to calculate a summary (the entire report, a specific report group or document page).
	
	![](../../../../images/eurd-web-label-legacy-summary-running-group.png)

5. Set the **Function** property to **Sum** and use the **Format String** property to format the summary's value.

	![](../../../../images/eurd-web-label-legacy-summary-settings.png)
	

Switch to [Print Preview](../../preview-print-and-export-reports.md) to see the result.

![](../../../../images/eurd-web-label-summary-result.png)