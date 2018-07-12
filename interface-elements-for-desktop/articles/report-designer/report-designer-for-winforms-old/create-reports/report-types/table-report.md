---
title: Table Report
author: Eugeniy Burmistrov
legacyId: 5048
---
# Table Report
This tutorial describes the steps to create a _table report_, which means that the report's data is arranged into a table-like layout. This feature should not be confused with the [master-detail report](master-detail-report.md) or [cross-tab report](cross-tab-report.md).

To create a table report, follow the steps below.
1. [Create a new report](../basic-operations/create-a-new-report.md).
2. [Bind the report to a data source](../binding-a-report-to-data.md).
3. To add a [Page Header](../../report-designer-reference/report-bands/page-header-and-footer.md) to the report, right-click anywhere on the report's surface, and in the invoked [Context Menu](../../report-designer-reference/report-designer-ui/context-menu.md), choose **Insert Band** | **Page Header**.
	
	![RD_Elements_ContextMenu_PageHeader](../../../../../images/img11092.png)
4. Now, add two [Table](../../report-designer-reference/report-controls/table.md) controls to the report's Page Header and [Detail band](../../report-designer-reference/report-bands/detail-band.md).
	
	To do this, in the [Toolbox](../../report-designer-reference/report-designer-ui/control-toolbox.md), click the **Table** icon. Then, in the Page Header's content area, click and hold down the left mouse button while dragging the mouse cursor across the Detail band.
	
	![RD_CreateReports_TableReport_0](../../../../../images/img8344.png)
	
	As a result, two tables are created. One will be used as a header, and the other one - for the report's detail information.
5. Type the headers into the upper table's cells, and bind the corresponding cells in the detail section to the appropriate data fields. This can be done by simply dropping these fields from the [Field List](../../report-designer-reference/report-designer-ui/field-list.md) onto the cells.
	
	![RD_CreateReports_TableReport_1](../../../../../images/img8345.png)
6. Finally, you can customize various properties of the tables, to improve their appearance. For example, using the [Property Grid](../../report-designer-reference/report-designer-ui/property-grid.md) you can define their **Borders**, as well as **Background Color**. To customize the cells' text options, use the [Formatting Toolbar](../../report-designer-reference/report-designer-ui/formatting-toolbar.md).
	
	A noteworthy feature is the capability to specify [odd-even styles](../styles-and-conditional-formatting/use-odd-and-even-styles.md) for the detail table.

The table report is now ready. Switch to the [Preview Tab](../../report-designer-reference/report-designer-ui/preview-tab.md), and view the result.

![RD_CreateReports_TableReport_2](../../../../../images/img8346.png)