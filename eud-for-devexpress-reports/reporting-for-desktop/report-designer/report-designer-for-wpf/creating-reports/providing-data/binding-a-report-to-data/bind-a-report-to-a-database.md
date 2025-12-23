---
title: Bind a Report to a Database
author: Anna Gubareva
legacyId: 116270
---
# Bind a Report to a Database
This document describes the steps required to connect a report to a database.

To bind a report to a database, do the following.
1. [Create a new report param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } .
2. Right-click the report and select **Edit...** in the context menu. In the invoked dialog, expand the **Data Source** drop-down and click the **Add New** button.
	
	![EUD_WpfReportDesigner_AddDataSource](../../../../../images/img123562.png)

3. On the first page of the invoked **Data Source Wizard**, specify the data connection to be used. If it is absent in the list containing existing connections, select **No, I'd like to specify the connection parameters myself** and click **Next**.
	
	![EUD_WpfReportDesigner_DataSourceWizard_Database_2](../../../../../images/img123986.png)

4. On the next page, specify the data source type. Select **Microsoft SQL Server** and click **Next** to proceed.
	
	![WPDDesigner_ReportWizard_SelectDataSourceType](../../../../../images/img122896.png)

5. This page allows you to specify connection string parameters specific to the selected data source provider. Depending on the data provider selected, it may be necessary to specify additional connection options (such as authentication type and database name) on this page.
	
	![WPDDesigner_ReportWizard_SpecifyConnectionString](../../../../../images/img122000.png)
	
	Click **Next** to proceed.
6. If server authentication is required for the selected database type, the next page will prompt you to specify whether or not you want to save the user credentials along with the connection string.
	
	Select the required option and click **Next**.
	
	![EUD_WpfReportDesigner_DataSourceWizard_Database_3](../../../../../images/img123987.png)
7. On the next page, you can construct an SQL query to obtain data from the database, or select a stored procedure.
	
	To construct an SQL query, click **Run Query Builder...**
	
	![EUD_WpfReportDesigner_DataSourceWizard_Database_4](../../../../../images/img123988.png)
8. In the invoked [Query Builder param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  window, select an item from the list of available tables on the left and drop it onto the list of data tables to be used.
	
	![WPDDesigner_QueryBuilder_AddingTable](../../../../../images/img122798.png)
9. Enable the check box near the added table to include all of its fields in the data view.
	
	![WPDDesigner_QueryBuilder_AddTable](../../../../../images/img122117.png)
	
	Click **OK** to exit the **Query Builder**. Click **Finish** to exit the **Data Source Wizard**.
	
	The newly created SQL data source will be displayed in the **Components** node of the [Report Explorer param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } . Additionally, the hierarchy of the data source will be reflected by the [Field List param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } .
	
	![EUD_WpfReportDesigner_SqlDataSource](../../../../../images/img123563.png)