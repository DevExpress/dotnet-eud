---
title: Bind a Report to an Excel Workbook
author: Anna Gubareva
---
# Bind a Report to an Excel Workbook


This tutorial describes how to bind a report to data obtained from a Microsoft Excel workbook:

1. [Create a new report](../add-new-reports.md).
2. Click the report's smart tag. In the invoked actions list, expand the drop-down menu for the **Data Source** property and click **Add Report DataSource**.
	
	![](../../../../images/eurd-win-report-smart-tag-add-new-data-source.png)

3. On the first page of the invoked [Data Source Wizard](../report-designer-tools/data-source-wizard.md), select **Excel File** and click **Next**.
	
	![](../../../../images/eurd-win-data-source-wizard-select-excel-data-source.png)

4. On the next wizard page, select a required Excel workbook. To do this, click the ellipsis button and locate the source file or enter the full path to this file. The XLS, XLSX and XLSM formats are supported.
	
	![eurd-win-selectexcelworkbook](../../../../images/eurd-win-selectexcelworkbook.png)
	
	Click **Next** to proceed to the next wizard page.
4. The next wizard page allows you to specify import settings.
	
	Enable the first check box to use values of the first row as field names. If you disable this option, values of the first row will be imported as data and field names will be generated automatically. You can also specify whether to include empty rows to the result data source and whether to skip hidden rows and columns.
	
	![eurd-win-exceldatasource_specifyingimportoptions](../../../../images/eurd-win-exceldatasource_specifyingimportoptions.png)
	
	Specify required settings and click **Next**.
5. On the next wizard page specify from which part of the workbook to extract data. All worksheets, tables and named regions existing in the workbook are listed here.
	
	![eurd-win-exceldatasource_choosingtablesheetrange](../../../../images/eurd-win-exceldatasource_choosingtablesheetrange.png)
6. The next wizard page allows you to select required columns and specify their settings.
	
	To include a column to the resulting data source, enable the corresponding **Selected** check box. Use **Name** to specify the custom column name and **Type** to choose the column type.
	
	![eurd-win-exceldatasource_selectingcolumns](../../../../images/eurd-win-exceldatasource_selectingcolumns.png)
	
	On this page, you can also preview the resulting data by clicking the **Preview...** button.
	
	![eurd-win-exceldatasource_datapreview](../../../../images/eurd-win-exceldatasource_datapreview.png)
	
	Click **Finish** to complete the wizard.

The created data source becomes displayed in the [Report Explorer](../report-designer-tools/ui-panels/report-explorer.md)'s **Components** node. The [Field List](../report-designer-tools/ui-panels/field-list.md) reflects the data source's hierarchy.

![](../../../../images/eurd-win-data-source-wizard-select-excel-result.png)