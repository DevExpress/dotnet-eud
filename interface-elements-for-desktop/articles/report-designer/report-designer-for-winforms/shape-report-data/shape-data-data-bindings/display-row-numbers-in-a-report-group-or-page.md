---
title: Display Row Numbers in a Report, Group or Page
author: Anna Gubareva
---
# Display Row Numbers in a Report, Group or Page

This document describes how to show the current row number for each data source value displayed in a report.

> [!Warning]
> Use the approach below if expression bindings **are not enabled** in the Report Designer (the [Property Grid](../../report-designer-tools/ui-panels/property-grid.md) does not provide the **Expressions** ![](../../../../../images/eurd-win-property-grid-expressions-icon.png) tab ).
>
> See [Display Row Numbers in a Report, Group or Page](../shape-data-expression-bindings/display-row-numbers-in-a-report-group-or-page.md) if expression bindings **are enabled** in the Report Designer (the [Property Grid](../../report-designer-tools/ui-panels/property-grid.md) provides the **Expressions** ![](../../../../../images/eurd-win-property-grid-expressions-icon.png) tab).

A label can display row numbers after [binding your report to data](../../bind-to-data.md) and specifying a bound data field.

1. Click the label's smart tag and invoke its **Summary Running** drop-down list. Select **Report** to increment the row numbers throughout the entire report, or select **Group** or **Page** to reset the row numbers for every group or page.
	
	![](../../../../../images/eurd-win-shaping-row-numbers-legacy-summary-running.png)

2. Set the **Summary Func** property to **Record Number** and use the **Format String** property to format the summary's value.
	
	![](../../../../../images/eurd-win-shaping-row-numbers-legacy-settings.png)

You can switch to [Print Preview](../../preview-print-and-export-reports.md) to see the record numbers displayed for the specified range.

![](../../../../../images/eurd-win-shaping-row-numbers-result.png)