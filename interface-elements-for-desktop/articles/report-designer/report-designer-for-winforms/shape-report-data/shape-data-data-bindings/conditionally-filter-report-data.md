---
title: Conditionally Filter Report Data
author: Anna Gubareva
---
# Conditionally Filter Report Data

This document describes how to filter a report's data based on a specific condition.

> [!NOTE]
> Use this approach if data bindings **are enabled** in the Report Designer (the Label's smart tag includes the **Data Binding** property).
>
> ![](../../../../../images/eurd-label-expression-binding-modes.png)
>
> See the [Conditionally Filter Report Data](../shape-data-expression-bindings/conditionally-filter-report-data.md) topic in the [Shape Data (Expression Bindings)](../shape-data-expression-bindings.md) section to learn about an alternative approach.

1. Switch to the [Field List](../../report-designer-tools/ui-panels/field-list.md), right-click the **Parameters** section and add a new report parameter.
	
	![](../../../../../images/eurd-win-shaping-filter-add-parameter.png)

2. Specify the parameter's description in Print Preview and set its type to **Number (Integer)**.
	
	![](../../../../../images/eurd-win-shaping-filter-parameter-settings.png)

3. Click the Detail band's smart tag, and in its actions list, click the **Formatting Rules** property's ellipsis button. In the invoked **Formatting Rules Editor**, click the **Edit Rule Sheet** button.

	![](../../../../../images/eurd-win-shaping-formatting-rules-property.png)

4. In the invoked **Formatting Rule Sheet Editor**, click the plus button to create a new formatting rule. Set the **Visible** property to **No** and click the **Condition** property's ellipsis button.

	![](../../../../../images/eurd-win-shaping-formatting-rule-settings.png)

5. In the invoked **Condition Editor**, specify the required visibility condition.
	
	![](../../../../../images/eurd-win-shaping-formatting-rule-filter-condition.png)
	
	Click **OK** to save the changes and close the dialog. Then, click **Close** to quit the **Formatting Rule Sheet Editor**.

6. In the **Formatting Rules Editor**, you can see the created rule (called **formattingRule1**), which should be moved to the list of active rules on the right using the arrow buttons in the center of the dialog box.

	![](../../../../../images/eurd-win-shaping-apply-formatting-rule.png)

	In this editor, you can also customize the precedence of formatting rules using the up and down arrow buttons on the right of the dialog box. The rules are applied in the same order that they appear in the list, and the last rule in the list has the highest priority.

Switch to [Print Preview](../../preview-print-and-export-reports.md) to see the result. 

![](../../../../../images/eurd-win-shaping-filter-result.png)