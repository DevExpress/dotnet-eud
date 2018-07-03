---
title: Multi-Column Report
author: Eugeniy Burmistrov
legacyId: 5051
---
# Multi-Column Report
This tutorial describes the steps to create a _multi-column report_, meaning that each page of the report document is laid out in a specified number of columns.

To demonstrate the multi-column feature, we'll use a report with grouping, similar the one created in the following tutorial: [Change or Apply Data Grouping to a Report](../../report-editing-basics/change-or-apply-data-grouping-to-a-report.md).
1. Select the [Detail band](../../report-designer-reference/report-bands/detail-band.md), and in the [Property Grid](../../report-designer-reference/report-designer-ui/property-grid.md), expand the **Multi-Column Options** section.
	
	First, set the required **Mode**. It determines whether the number of columns is manually specified, or it depends on the fixed column width.
	
	![RD_CreateReports_MultiColumn_1](../../../../../images/img8349.png)
2. Then, if you've chosen to **Use Column Count**, set the **Column Count** to **2**, and **Column Spacing** to **10**.
	
	The **Direction** determines the order in which records of the same group are processed.
	
	![RD_CreateReports_MultiColumn_2](../../../../../images/img8350.png)
3. Now, on the Detail band's surface a grey area appears, delimiting the available column's width. Adjust the controls width, so that they fit within the effective borders.
	
	![RD_CreateReports_MultiColumn_0](../../../../../images/img8348.png)

The multi-column report is now ready. Switch to the [Preview Tab](../../report-designer-reference/report-designer-ui/preview-tab.md), and view the result.

![RD_CreateReports_MultiColumn_3](../../../../../images/img8351.png)