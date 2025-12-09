---
title: Calculated Fields
author: Anna Gubareva
legacyId: 116278
---
# Calculated Fields
This document demonstrates how to add a _calculated field_ to a report. The main purpose of calculated fields is to perform pre-calculations of virtually any level of complexity over data fields based on a specific expression.

In the Report Designer, a calculated field is similar to an ordinary data field (e.g., you can [bind controls to it](binding-report-controls-to-data.md), and [group](../shaping-data/grouping-data.md), [sort](../shaping-data/sorting-data.md) and [filter](../shaping-data/filtering-data.md) your report against it).

To add a calculated field to your report, follow the instructions below.
1. To create a calculated field, in the [Field List](../../interface-elements/field-list.md), right-click any item inside the data source, and in the invoked menu, select **Add Calculated Field**.
	
	![WPFDesigner_FieldListAddingCalcField](../../../../../images/img123013.png)
2. In the Field List, select the created field and switch to the [Properties Panel](../../interface-elements/properties-panel.md). Make sure to change the **Field Type** property to an appropriate value.
	
	![EUD_WpfReportDesigner_CalcField_1](../../../../../images/img123716.png)
3. Then, create an expression for the calculated field.
	
	Click the ellipsis button for the **Expression** property to invoke the **Expression Editor**. You can also invoke this dialog by right-clicking the calculated field within the Field List and selecting **Edit Expression...**
	
	![EUD_WpfReportDesigner_CalcField_2](../../../../../images/img123717.png)
	
	Click **Fields** to see the field list. To add a data field or [report parameter](report-parameters.md) to this expression, double-click the required name. A data field is inserted into the expression's text using its name in **[**square brackets**]**, and parameters are inserted using the "**Parameters.**" prefix before their names. Use the toolbar to add operators between field names.
	
	To close the dialog and save the expression, click **OK**.
4. Finally, drag the calculated field from the Field List onto the required [band](../../report-elements/report-bands.md) like an ordinary data field.
	
	![EUD_WpfReportDesigner_CalcField_3](../../../../../images/img123718.png)

The report with a calculated field is now ready. Switch to the [Print Preview](../../document-preview.md) tab and view the result.

![EUD_WpfReportDesigner_CalcField_Result](../../../../../images/img123719.png)