---
title: Add Calculated Fields to a Report
---
# Add Calculated Fields to a Report
This document demonstrates how to add a _calculated field_ to a report. The main purpose of calculated fields is to perform pre-calculations (of virtually any level of complexity) over [data fields](../../../../../interface-elements-for-desktop/articles/report-designer/report-designer-for-winforms/report-editing-basics/displaying-values-from-a-database-(binding-report-elements-to-data).md). To learn how to easily perform simple calculations within a single data field, refer to [Add Totals to a Report](../../../../../interface-elements-for-desktop/articles/report-designer/report-designer-for-winforms/report-editing-basics/add-totals-to-a-report.md).

In the Report Designer, a calculated field is similar to an ordinary data field (e.g. you can bind controls to it, and [group](../../../../../interface-elements-for-desktop/articles/report-designer/report-designer-for-winforms/report-editing-basics/change-or-apply-data-grouping-to-a-report.md), [sort](../../../../../interface-elements-for-desktop/articles/report-designer/report-designer-for-winforms/report-editing-basics/change-or-apply-data-sorting-to-a-report.md) and [filter](../../../../../interface-elements-for-desktop/articles/report-designer/report-designer-for-winforms/report-editing-basics/change-or-apply-data-filtering-to-a-report.md) your report against it).

To add a calculated field to your report, follow the instructions below.
1. To create a calculated field, in the [Field List](../../../../../interface-elements-for-desktop/articles/report-designer/report-designer-for-winforms/report-designer-reference/report-designer-ui/field-list.md), right-click any data member, and on the invoked menu, choose **Add Calculated Field**.
	
	![RD_HowTo_CalculatedField_0](../../../../images/Img8465.png)
2. In the Field List, select the created field to show its properties in the [Property Grid](../../../../../interface-elements-for-desktop/articles/report-designer/report-designer-for-winforms/report-designer-reference/report-designer-ui/property-grid.md). Among these options, make sure to change the **Field Type** property to an appropriate value.
	
	![RD_HowTo_CalculatedField_1](../../../../images/Img8466.png)
3. Now, let's create an expression for the calculated field.
	
	Click the ellipsis button in the **Expression** section, to invoke the **Expression Editor**. You can also invoke this dialog by right-clicking your calculated field within the Field List and selecting **Edit Expression...**
	
	![RD_HowTo_CalculatedField_2](../../../../images/Img8467.png)
	
	Click **Fields** to see the field list. Double-click field names to add them to the expression string. Use the toolbar to add operators between field names.
	
	> Note that it's also possible to employ [parameters](../../../../../interface-elements-for-desktop/articles/report-designer/report-designer-for-winforms/report-editing-basics/add-parameters-to-a-report.md) in a calculated field's expression.
	
	 
	
	To close the dialog and save the expression, click **OK**.
4. Finally, drag the calculated field from the Field List onto the required [band](../../../../../interface-elements-for-desktop/articles/report-designer/report-designer-for-winforms/report-designer-reference/report-bands.md), just like an ordinary data field.
	
	![RD_HowTo_CalculatedField_3](../../../../images/Img8468.png)

The report with a calculated field is now ready. Switch to the [Preview Tab](../../../../../interface-elements-for-desktop/articles/report-designer/report-designer-for-winforms/report-designer-reference/report-designer-ui/preview-tab.md), and view the result.

![RD_HowTo_CalculatedField_4](../../../../images/Img8469.png)