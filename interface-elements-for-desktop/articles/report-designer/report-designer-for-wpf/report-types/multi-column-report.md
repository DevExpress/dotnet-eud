---
title: Multi-Column Report
---
# Multi-Column Report
This tutorial describes the steps to create a _multi-column report_, meaning that each page of the report document is laid out in a specified number of columns.

To demonstrate the multi-column feature, use a report with grouping, similar to the one created in the following tutorial: [Grouping Data](../../../../../interface-elements-for-desktop/articles/report-designer/report-designer-for-wpf/creating-reports/shaping-data/grouping-data.md).
1. Select the [Detail band](../../../../../interface-elements-for-desktop/articles/report-designer/report-designer-for-wpf/report-elements/report-bands.md), and in the [Properties Panel](../../../../../interface-elements-for-desktop/articles/report-designer/report-designer-for-wpf/interface-elements/properties-panel.md), expand the **Multi-Column Options** section.
	
	Set the required **Mode**, which determines whether the number of columns is manually specified or if it depends on the fixed column width.
	
	![EUD_WpfReportDersigner_MultiColumn_1](../../../../images/Img123506.png)
2. Then, if you've chosen to **Use Column Count**, set the **Column Count** to **2**, and **Column Spacing** to **10**.
	
	The **Layout** property determines the order in which records of the same group are processed.
	
	![EUD_WpfReportDersigner_MultiColumn_2](../../../../images/Img123507.png)
3. Now, on the Detail band's surface, a gray area appears, delimiting the available column's width. Adjust the control width, so that they fit within the effective borders.
	
	![EUD_WpfReportDersigner_MultiColumn_3](../../../../images/Img123508.png)

The multi-column report is now ready. Switch to the [Print Preview](../../../../../interface-elements-for-desktop/articles/report-designer/report-designer-for-wpf/document-preview.md) tab and view the result.

![EUD_WpfReportDersigner_MultiColumn_Result](../../../../images/Img123509.png)