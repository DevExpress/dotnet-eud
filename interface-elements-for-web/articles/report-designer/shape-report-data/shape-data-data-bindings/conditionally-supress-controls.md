---
title: Conditionally Suppress Controls
author: Anna Vekhina
---
# Conditionally Suppress Controls

This document describes how to display or hide a report control in a published document based on a specified logical condition.

> [!Warning]
> Use the approach below if expression bindings **are not enabled** in the Report Designer (the Designer does not provide the [Expressions](../../report-designer-tools/ui-panels/expressions-panel.md) panel).
>
> See [Conditionally Suppress Controls](../shape-data-expression-bindings/conditionally-supress-controls.md)  if expression bindings **are enabled** in the Report Designer (the Designer provides the [Expressions](../../report-designer-tools/ui-panels/expressions-panel.md) panel).

1. [Create a new report](../../add-new-reports.md) or open an existing one and prepare the report layout.

2. Select the required control and expand the **Appearance** category in the [Properties](../../report-designer-tools/ui-panels/properties-panel.md) panel. Select the **Formatting rules** node and click the plus button to add a new formatting rule. 

    ![](../../../../images/eurd-web-shaping-check-box-add-formatting-rule.png)

3. Expand the **Formatting** node and set the **Visible** property to **No**. Click the **Condition** property's ellipsis button. In the invoked **Expression Editor**, specify the required visibility condition.

    ![](../../../../images/eurd-web-shaping-formatting-rule-suppress-expression.png)

4. Enable the formatting rule's check box to apply the created formatting rule to the required control.

	![](../../../../images/eurd-web-shaping-suppress-controls-apply-formatting-rule.png)

	In this editor, you can also customize the precedence of formatting rules using the up and down arrow buttons on the right of the dialog box. The rules are applied in the same order that they appear in the list, and the last rule in the list has the highest priority.

When switching to [Print Preview](../../preview-print-and-export-reports.md), you can view the report control's visibility changes according to the assigned condition.

![](../../../../images/eurd-web-shaping-suppress-result.png)
