---
title: Count the Number of Groups in a Report
author: Anna Gubareva
---
# Count the Number of Groups in a Report

This document describes how to count the number of groups in a report.

> [!NOTE]
> Use this approach if data bindings **are enabled** in the Report Designer (the Label's smart tag includes the **Data Binding** property).
>
> ![](../../../../../images/eurd-label-expression-binding-modes.png)
>
> See the [Count the Number of Groups in a Report](../shape-data-expression-bindings/count-the-number-of-groups-in-a-report.md) topic in the [Shape Data (Expression Bindings)](../shape-data-expression-bindings.md) section to learn about an alternative approach.

1. Switch to the [Group and Sort](../../report-designer-tools/ui-panels/group-and-sort-panel.md) panel and create a new group. Enable the **Show Header** option to display the Group Header in the report.
	
	![](../../../../../images/eurd-win-shaping-count-group-data.png)

2. Switch to the [Field List](../../report-designer-tools/ui-panels/field-list.md) and drop the group field onto the created Group Header.
	
	![](../../../../../images/eurd-win-shaping-count-drop-filed-onto-group-header.png)

3. Right-click the report's surface and add a Report Footer to the report.
	
	![](../../../../../images/eurd-win-shaping-insert-report-footer.png)

4. Drop the group field onto the Report Footer and invoke its smart tag. Set its **Summary Running** property to **Report**.
	
	![](../../../../../images/eurd-win-shaping-group-count-legacy-summary-running.png)


5. Set the **Summary Func** property to **Count (Distinct)** and use the **Format String** property to format the summary's value.
	
	![](../../../../../images/eurd-win-shaping-group-count-legacy-settings.png)


You can see the group count in the report footer when switching to [Print Preview](../../preview-print-and-export-reports.md).

![](../../../../../images/eurd-win-shaping-group-count-result.png)