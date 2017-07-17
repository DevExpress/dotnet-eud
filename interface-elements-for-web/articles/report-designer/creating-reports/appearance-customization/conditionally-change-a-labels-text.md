---
title: Conditionally Change a Label's Text
author: Anya Vekhina
legacyId: 114735
---
# Conditionally Change a Label's Text
In this tutorial, you will learn how to change a label's text if a certain condition is met, without using [scripts](../scripting.md).

To conditionally change a label's text, do the following.
1. [Create a new report](../basic-operations/create-a-new-report.md) and [bind it to a data source](../providing-data/bind-a-report-to-data.md).
2. Now, add a new [calculated field](../providing-data/calculated-fields.md). To do this, switch to the [Field List](../../interface-elements/field-list.md) panel, click a data table and click **Add calculated field** button.
	
	![eud-calc-fields-0](../../../../images/img119502.png)
3. Click the **Edit** button (the 'pencil' icon ![web-report-designer-edit-query](../../../../images/img118475.png)) for the calculated field and set the **Field Type** property to **String**.
	
	Then, click the ellipsis button for its **Expression** property and in the invoked [Expression Editor](../../interface-elements/expression-editor.md), define the required logical condition for the calculated field (e.g., **Iif([UnitsOnOrder] == 0, 'None', [UnitsOnOrder])**, which means that if the **UnitsOnOrder** data field's value is equal to **0**, the control's text will be replaced with **None**).
	
	![eud-change-label-text](../../../../images/img119846.png)
4. Finally, drop the required data fields (and the created calculated field as well) from the Field List onto the report's [Detail](../../report-elements/report-bands.md) band.
	
	![eud-change-label-text-1](../../../../images/img119847.png)

The report is now ready. Switch your report to the [Preview](../../document-preview.md) mode and view the result.

![eud-change-label-text-2](../../../../images/img119848.png)