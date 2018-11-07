---
title: Count the Number of Records in a Report or Group
author: Anna Gubareva
---
# Count the Number of Records in a Report or Group

This document describes how to display the number or records in a report or group.


> [!Warning]
> Use the approach below if expression bindings **are not enabled** in the Report Designer (the [Property Grid](../../report-designer-tools/ui-panels/property-grid.md) does not provide the **Expressions** ![](../../../../../images/eurd-win-property-grid-expressions-icon.png) tab ).
>
> See [Count the Number of Records in a Report or Group](../shape-data-expression-bindings/count-the-number-of-records-in-a-report-or-group.md) if expression bindings **are enabled** in the Report Designer (the [Property Grid](../../report-designer-tools/ui-panels/property-grid.md) provides the **Expressions** ![](../../../../../images/eurd-win-property-grid-expressions-icon.png) tab).

1. Right-click the report's design surface and add a Report Header or Footer to display the record count for the entire report.
	
	![](../../../../../images/eurd-win-shaping-insert-report-header.png)
	
	> [!Note]
	> Use a Group Header/Footer for displaying record counts for groups, and a Page Header/Footer for displaying record counts for pages.

2. Switch to the [Field List](../../report-designer-tools/ui-panels/field-list.md) and drop the corresponding data table field onto the created band to create a data-bound label.
	
	![](../../../../../images/eurd-win-shaping-drop-field-onto-report-header.png)

3. Click the label's smart tag and invoke its **Summary Running** drop-down list. Select **Report** to count the records throughout the entire report, or select **Group** or **Page** to reset the record count for every group or page.
	
	![](../../../../../images/eurd-win-shaping-row-count-legacy-summary-running.png)

4. Set the **Summary Func** property to **Count** and use the **Format String** property to format the summary's value.
	
	![](../../../../../images/eurd-win-shaping-row-count-legacy-settings.png)

You can switch to [Print Preview](../../preview-print-and-export-reports.md) to see the resulting report.

![](../../../../../images/eurd-win-shaping-count-result.png)