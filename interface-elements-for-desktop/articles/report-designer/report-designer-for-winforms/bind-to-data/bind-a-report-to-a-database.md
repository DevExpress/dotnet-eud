---
title: Bind a Report to a Database
author: Anna Gubareva
---
# Bind a Report to a Database

This tutorial demonstrates how to bind a report to a hierarchical data source and specify a master-detail relationship between data source queries:

1. [Create a new report](../add-new-reports.md).
2. Click the report's smart tag. In the invoked actions list, expand the drop-down menu for the **Data Source** property and click **Add Report DataSource**.
	
	![](../../../../images/eurd-win-report-smart-tag-add-new-data-source.png)

3. On the first page of the invoked [Data Source Wizard](../report-designer-tools/data-source-wizard.md), select **Database** and click **Next** to proceed.
	
	![](../../../../images/eurd-win-data-source-wizard-select-database.png)

4. The next page allows you to specify whether you want to use an existing data connection or create a new data connection from scratch. Select the first option to create a new connection and click **Next**.
	
	![](../../../../images/eurd-win-data-source-wizard-select-new-connection.png)

5. On the next page, you can define a custom connection string, or select one of the supported data providers.
	
	Depending on the data provider selected, it may be necessary to specify additional connection options (such as the authentication type and database name) on this page.
		
	![](../../../../images/eurd-win-data-source-wizard-connection-settings.png)
	
	To proceed to the next wizard page, click **Next**.
6. On the next page, you can choose which tables, views and/or stored procedures to add to the report.

    To create a master-detail report, select two or more tables and click **Manage Relations**.

    ![](../../../../images/eurd-win-data-source-wizard-select-tables.png)

    In the invoked editor, connect the required key fields (columns) using drag and drop.

    ![](../../../../images/eurd-win-data-source-wizard-master-detail-relation-eidtor.png)

    Click **OK** to close the editor.

    > [!NOTE]
    > When you are required to shape data at the level of a data source, you can create [custom queries](../report-designer-tools/report-wizard/data-bound-report/connect-to-a-database/create-a-query-or-select-a-stored-procedure.md) by expanding the **Queries** category and clicking the plus button.
    > 
    > This will invoke the [Query Builder](../report-designer-tools/query-builder.md) where you can create complex queries by joining multiple tables, filtering, sorting and grouping their data, as well as calculating various aggregate functions.
    > 
    > Although it is also possible to join different tables within a single query, creating hierarchical data sources is preferred in most cases to provide better performance (in general, master-detail reports are generated faster than similar-looking reports created by grouping "flat" data sources).
        
Click **Finish** to complete the **Data Source Wizard**. If the selected queries or stored procedures contain any [parameters](../shape-report-data/use-report-parameters/use-query-parameters.md), you can go to the [next wizard page](../report-designer-tools/report-wizard/data-bound-report/connect-to-a-database/configure-query-parameters.md) and define their values.

The newly created SQL data source will be displayed in the **Components** node of the [Report Explorer](../report-designer-tools/ui-panels/report-explorer.md). Additionally, the hierarchy of the data source will be reflected by the [Field List](../report-designer-tools/ui-panels/field-list.md). In both panels, you can right-click the data source to access its settings.

![](../../../../images/eurd-win-data-source-wizard-database-result.png)