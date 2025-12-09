---
title: Calculate a Summary
author: Anna Vekhina
---
# Calculate a Summary

This document describes how to calculate various summaries across a report and its groups.

1. [Create a new report](../../add-new-reports.md) or open an existing one and [bind it to a data source](../../bind-to-data.md).

2. Insert the [Group Header](../../introduction-to-banded-reports.md) band, select the **Group Fields** section in the **Group Header Tasks** category and add a new group field to group the report's data by the required field. 

    ![](../../../../images/eurd-web-label-summary-group-data.png)

3. Insert the Group Footer band. Prepare the report layout and drop a required data field onto the group footer to display the summary result.

4. Select the label, expand the **Summary** section and invoke the **Running** drop-down list. Select the range for which to calculate a summary (the entire report, a specific report group or document page).
	
	![](../../../../images/eurd-web-label-summary-running-group.png)

5. Click the **Text** property's marker to invoke a menu. Select **Text Expression**.
	
	![](../../../../images/eurd-web-label-summary-expression-property.png)

6. This invokes the [Expression Editor](../../report-designer-tools/expression-editor.md) where you can select the required summary in the **Functions** | **Summary** section. Report summary functions start with the "sum" prefix to make it easy to differentiate them from aggregate functions.
	
	![](../../../../images/eurd-web-label-summary-expression.png)
	
	> [!TIP]
	> See the [Functions in Expressions](../../use-expressions/functions-in-expressions.md) topic for a complete list of supported summary functions.

7. You can use the **Text Format String** property to format the summary's value.
	
	![](../../../../images/eurd-web-label-summary-format-string.png)

Switch to [Print Preview](../../preview-print-and-export-reports.md) to see the result.

![](../../../../images/eurd-web-label-summary-result.png)