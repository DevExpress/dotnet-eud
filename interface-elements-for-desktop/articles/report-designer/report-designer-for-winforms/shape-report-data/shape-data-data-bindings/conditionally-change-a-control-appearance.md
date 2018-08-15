---
title: Conditionally Change a Control's Appearance
author: Anna Gubareva
---
# Conditionally Change a Control's Appearance

This document describes how to change a report control's appearance based on a specific condition.

> [!Warning]
> Use the approach below if expression bindings **are not enabled** in the Report Designer (the [Property Grid](../../report-designer-tools/ui-panels/property-grid.md) does not provide the **Expressions** ![](../../../../../images/eurd-win-property-grid-expressions-icon.png) tab ).
>
> See [Conditionally Change a Control's Appearance](../shape-data-expression-bindings/conditionally-change-a-control-appearance.md) if expression bindings **are enabled** in the Report Designer (the [Property Grid](../../report-designer-tools/ui-panels/property-grid.md) provides the **Expressions** ![](../../../../../images/eurd-win-property-grid-expressions-icon.png) tab).

1. Click the report's smart tag, and in the invoked actions list, click the **Formatting Rule Sheet** property's ellipsis button.

    ![](../../../../../images/eurd-win-shaping-report-formatting-rule-sheet-property.png)

2. In the invoked **Formatting Rule Sheet Editor**, click the plus button to create a new formatting rule and click the **Condition** property's ellipsis button.

	![](../../../../../images/eurd-win-shaping-formatting-rule-editor-condition-property.png)

3. In the invoked **Condition Editor**, specify the required Boolean condition (which means that its result is either _true_ or _false_).
	
	![](../../../../../images/eurd-win-shaping-formattin-rule-appearance-condition.png)	

	Click **OK** to save the changes and close the dialog.

4. Back in the **Formatting Rule Sheet Editor**, define the formatting to be applied (e.g. specify the desired font color).

    ![](../../../../../images/eurd-win-shaping-formattin-rule-appearance-settings.png)

    Click **Close** to save the changes and quit the dialog.

5. Select a required band or control to which the formatting rule should be applied and access its **Formatting Rules** collection.

    ![](../../../../../images/eurd-win-shaping-band-formatting-rules-property.png)

6. In the invoked **Formatting Rules Editor**, move the rule to the list of active rules on the right using the arrow buttons in the center of the editor.

    ![](../../../../../images/eurd-win-shaping-apply-formatting-rule.png)

    In this editor, you can also customize the precedence of formatting rules using the up and down arrow buttons on the right of the dialog box. The rules are applied in the same order that they appear in the list, and the last rule in the list has the highest priority.

Switch to [Print Preview](../../preview-print-and-export-reports.md) to view the resulting report.

![](../../../../../images/eurd-win-shaping-formatting-rules-result.png)