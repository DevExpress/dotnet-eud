---
title: Conditionally Change a Control's Appearance
---
# Conditionally Change a Control's Appearance
This document describes the steps needed to conditionally change a control's appearance (e.g., make a Label's text red if its value exceeds a certain threshold). Thanks to the _formatting rules_ feature, no [scripts](../scripting.md) are required to achieve this, so you shouldn't write any code.

To conditionally change a control's appearance, do the following.
1. [Create a new report](../basic-operations/create-a-new-report.md) and [bind it to a data source](../providing-data/bind-a-report-to-data.md).
2. Switch to the [Properties Panel](../../interface-elements/properties-panel.md), expand the **Appearance** category and then expand the **Formatting Rules** section. Add a new _formatting rule_ by clicking the ![formatting-rules-editor-add](../../../../images/img118323.png) button.
	
	![eud-change-control-appearance-0](../../../../images/img119805.png)
3. Expand the newly added rule, specify its name and formatting options (e.g., **Foreground Color**). You can also specify the **Data Source** and **Data Member** properties. These properties define the list containing data fields that can participate in constructing the Boolean condition.
	
	![eud-change-control-appearance-1](../../../../images/img119806.png)
4. Then, click the ellipsis button for the **Condition** property. In the invoked [Expression Editor](../../interface-elements/expression-editor.md), define the required Boolean condition (which means that its result is returned as either true or false). In this tutorial, we will format fields if the **UnitPrice** value is greater than **30**.
	
	![eud-change-control-appearance-2](../../../../images/img119807.png)
	
	To save the condition and close the dialog, click **Save**.
5. A formatting rule can be applied to any number of [report elements](../../report-elements.md) within the same report. To apply a rule to a control, select the required report control and enable the checkbox for the required rule.
	
	![eud-change-control-appearance-3](../../../../images/img119808.png)
	
	If multiple rules are applied, it is possible to customize their precedence by using the ![formatting-rules-editor-up](../../../../images/img118325.png) and ![formatting-rules-editor-down](../../../../images/img118326.png) buttons. So the rules are applied in the same order that they appear in the list, and the last rule in the list has the highest priority.

Switch your report to the [Preview](../../document-preview.md) mode and view the result.

![eud-change-control-appearance-4](../../../../images/img119809.png)