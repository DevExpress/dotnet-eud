---
title: Table Report
---
This tutorial describes the steps to create a _table report_, which means that the report's data is arranged into a table-like layout. This feature should not be confused with the [master-detail report](../../../../interface-elements-for-web/articles/report-designer/report-types/master-detail-report-(detail-report-bands).md) or [cross-tab report](../../../../interface-elements-for-web/articles/report-designer/report-types/cross-tab-report.md).

To create a table report, follow the steps below.
1. [Create a new report](../../../../interface-elements-for-web/articles/report-designer/creating-reports/basic-operations/create-a-new-report.md) and [bind it to a data source](../../../../interface-elements-for-web/articles/report-designer/creating-reports/providing-data/bind-a-report-to-data.md).
2. To add a [Page Header](../../../../interface-elements-for-web/articles/report-designer/report-elements/report-bands.md) to the report, switch to the [Properties Panel](../../../../interface-elements-for-web/articles/report-designer/interface-elements/properties-panel.md), expand the **Actions** category and click **Insert Page Header Band**.
	
	![RD_Elements_ContextMenu_PageHeader](../../../images/Img119001.png)
3. Now, add two [Table](../../../../interface-elements-for-web/articles/report-designer/report-elements/report-controls.md) controls to the report's Page Header and [Detail band](../../../../interface-elements-for-web/articles/report-designer/report-elements/report-bands.md).
	
	To do this, drag the Table report control from the [Toolbox](../../../../interface-elements-for-web/articles/report-designer/interface-elements/toolbox.md) and drop it onto the Page Header band. Then, add a table to the Detail band in the same way.
	
	![RD_CreateReports_TableReport_0](../../../images/Img119002.png)
	
	One table will be used as a header, and the other one - for the report's detail information.
4. Type the headers into the upper table's cells, and bind the corresponding cells in the detail section to the appropriate data fields. To do this, select a table cell and set its **Data Binding** property to the required data field.
	
	![RD_CreateReports_TableReport_1](../../../images/Img119003.png)
5. Finally, you can customize various properties of the tables to improve their appearance. For example, in the **Appearance** category of the Properties Panel, you can define the **Borders** property, as well as the **Background Color** property. To customize cell text options, specify the **Font** property.
	
	A noteworthy feature is the capability to specify [odd-even styles](../../../../interface-elements-for-web/articles/report-designer/creating-reports/appearance-customization/use-odd-and-even-styles.md) for the detail table.

The table report is now ready. Switch your report to the [Preview](../../../../interface-elements-for-web/articles/report-designer/document-preview.md) mode and view the result.

![RD_CreateReports_TableReport_2](../../../images/Img119004.png)