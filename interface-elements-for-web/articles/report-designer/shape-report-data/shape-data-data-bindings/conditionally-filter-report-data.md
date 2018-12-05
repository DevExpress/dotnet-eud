---
title: Conditionally Filter Report Data
author: Anna Vekhina
---
# Conditionally Filter Report Data

This document describes how to filter a report's data based on a specific condition.

> [!Warning]
> Use the approach below if expression bindings **are not enabled** in the Report Designer (the Designer does not provide the [Expressions](../../report-designer-tools/ui-panels/expressions-panel.md) panel).
>
> See [Conditionally Filter Report Data](../shape-data-expression-bindings/conditionally-filter-report-data.md) if expression bindings **are enabled** in the Report Designer (the Designer provides the [Expressions](../../report-designer-tools/ui-panels/expressions-panel.md) panel).

1. Switch to the [Field List](../../report-designer-tools/ui-panels/field-list.md), select the **Parameters** node and click **Add parameter**.
	
	![](../../../../images/eurd-web-shaping-legacy-filter-add-parameter.png)

2. Specify the parameter's description in Print Preview and set its type to **Number (Integer)**.
	
	![](../../../../images/eurd-web-shaping-legacy-filter-parameter-settings.png)

3. Select the Detail band, expand the **Appearance** node, select the **Formatting rules** and click the plus button to add a new formatting rule.

	![](../../../../images/eurd-web-shaping-legacy-report-add-formatting-rule.png)

4. Expand the **Formatting** node and set the **Visible** property to **No**. Click the **Condition** property's ellipsis button. In the invoked [Expression Editor](../../report-designer-tools/expression-editor.md), specify the required visibility condition.

	![](../../../../images/eurd-web-shaping-legacy-formatting-rule-filter-condition.png)

5. Enable the formatting rule's check box to apply the created formatting rule to the Detail band.

	![](../../../../images/eurd-web-shaping-legacy-apply-formatting-rule.png)

	In this editor, you can also customize the precedence of formatting rules using the up and down arrow buttons on the right of the dialog box. The rules are applied in the same order that they appear in the list, and the last rule in the list has the highest priority.

Switch to [Print Preview](../../preview-print-and-export-reports.md) to see the result. 

![](../../../../images/eurd-web-shaping-filter-result.png)