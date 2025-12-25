---
title: Display Row Numbers in a Report, Group or Page
author: Anna Gubareva
---
# Display Row Numbers in a Report, Group or Page

This document describes how to show the current row number for each data source value displayed in a report.

A label can display row numbers after [binding your report to data](../../bind-to-data.md) and specifying a bound data field in the Label's **Expression** property.

1. Click the label's smart tag. In the invoked **Label Tasks** window, click the **Summary** property's ellipsis button.
	
	![](../../../images/eurd-win-shaping-row-numbers-summary-running.png)

2. In the Summary Editor window:

	* Set the **Summary running** property. Select **Report** to increment the row numbers throughout the entire report, or select **Group** or **Page** to reset the row numbers for every group or page.
	* Set the **Summary function** property to **Record Number**.
	
	![](../../../images/eurd-win-shaping-row-numbers-expression-property.png)

3. Back in the **Label Tasks** window, you can use the **FormatString** property to format the resulting value:
	
	![](../../../images/eurd-win-shaping-row-numbers-format-string.png)

You can switch to [Print Preview](../../preview-print-and-export-reports.md) to see the record numbers displayed for the specified range.

![](../../../images/eurd-win-shaping-row-numbers-result.png)