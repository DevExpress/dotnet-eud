---
title: Bind a Report to an Entity Framework Data Source
author: Anna Gubareva
legacyId: 116271
---
# Bind a Report to an Entity Framework Data Source
This document describes the steps required to connect a report to data provided by an Entity Framework data context.

To bind a report to an Entity Framework data source, do the following.
1. [Create a new report](../../basic-operations/create-a-new-report.md).
2. Right-click the report and select **Edit...** in the context menu. In the invoked dialog, expand the **Data Source** drop-down and click the **Add New** button.
	
	![EUD_WpfReportDesigner_AddDataSource](../../../../../../images/img123562.png)
3. The first page of the invoked **Data Source Wizard** allows you to specify the data source type. Select **Entity Framework** and click **Next** to proceed.
	
	![EUD_WpfReportDesigner_DataSourceWizard_EF](../../../../../../images/img123564.png)
4. On the next page, select the required data context from the list of available data contexts and click **Next**.
	
	![EUD_WpfReportDesigner_EF_1](../../../../../../images/img123989.png)
5. Select a connection string to be used to establish a data connection.
	
	![EUD_WpfReportDesigner_EF_2](../../../../../../images/img123990.png)
	
	Click **Next** to proceed to the next page.
6. The following wizard page is available only if the current entity data model contains stored procedures. To bind to a stored procedure, click **Add**. Then, in the invoked window, select a required stored procedure and click **OK**.
	
	![EUD_WpfReportDesigner_EF_3](../../../../../../images/img123991.png)
7. Configure the parameters to be passed to the selected stored procedure. Be sure to specify the correct parameter **Type**. Click **Finish** to exit the wizard.
	
	![EUD_WpfReportDesigner_EF_4](../../../../../../images/img123992.png)

The newly created Entity Framework data source will be displayed in the **Components** node of the [Report Explorer](../../../interface-elements/report-explorer.md). Additionally, the hierarchy of the data source will be reflected by the [Field List](../../../interface-elements/field-list.md).

![EUD_WpfReportDesigner_EFDataSource](../../../../../../images/img123567.png)