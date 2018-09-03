---
title: Count the Number of Groups in a Report
author: Anna Gubareva
---
# Count the Number of Groups in a Report

This document describes how to count the number of groups in a report.

> [!Warning]
> Use the approach below if expression bindings **are enabled** in the Report Designer (the [Property Grid](../../report-designer-tools/ui-panels/property-grid.md) provides the **Expressions** ![](../../../../../images/eurd-win-property-grid-expressions-icon.png) tab ).
>
> See [Count the Number of Groups in a Report](../shape-data-data-bindings/count-the-number-of-groups-in-a-report.md) if expression bindings **are not enabled** in the Report Designer (the [Property Grid](../../report-designer-tools/ui-panels/property-grid.md) does not provide the **Expressions** ![](../../../../../images/eurd-win-property-grid-expressions-icon.png) tab).

1. Switch to the [Group and Sort](../../report-designer-tools/ui-panels/group-and-sort-panel.md) panel and create a new group. Enable the **Show Header** option to display the Group Header in the report.
	
	![](../../../../../images/eurd-win-shaping-count-group-data.png)

2. Switch to the [Field List](../../report-designer-tools/ui-panels/field-list.md) and drop the group field onto the created Group Header.
	
	![](../../../../../images/eurd-win-shaping-count-drop-filed-onto-group-header.png)

3. Right-click the report's surface and add a Report Footer to the report.
	
	![](../../../../../images/eurd-win-shaping-insert-report-footer.png)

4. Drop a label onto the Report Footer and invoke its smart tag. Set its **Summary Running** property to **Report**.
	
	![](../../../../../images/eurd-win-shaping-group-count-summary-running.png)

5. Click the ellipsis button for the label's **Expression** property.
	
	![](../../../../../images/eurd-win-shaping-group-count-expression-property.png)

6. In the invoked **Summary Expression Editor**, select the **sumDCount** summary function in the **Functions** | **Summary** section.
	
	![](../../../../../images/eurd-win-shaping-group-count-expression.png)

7. Use the **Format String** property to format the summary's value.
	
	![](../../../../../images/eurd-win-shaping-group-count-format-string.png)

You can see the group count in the report footer when switching to [Print Preview](../../preview-print-and-export-reports.md).

![](../../../../../images/eurd-win-shaping-group-count-result.png)