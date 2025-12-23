---
title: Bind a Report to an XML File
author: Anna Gubareva
---
# Bind a Report to an XML File

This tutorial demonstrates how to bind a report to data stored in an external XML file.

1. [Create a new report param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } .

2. Click the report's smart tag. In the invoked actions list, expand the drop-down menu for the **Data Source** property and click **Add New DataSource**.
	
	![](..\/..\/..\/images/eurd-win-report-smart-tag-add-new-data-source.png)

3. On the first page of the invoked [Data Source Wizard param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } , select **Database** and click **Next**.
	
	![](..\/..\/..\/images/eurd-win-data-source-wizard-xml.png)

4. The next page allows you to specify whether you want to use an existing data connection or create a new data connection. Select the first option and click **Next**.
	
	![](..\/..\/..\/images/eurd-win-data-source-wizard-select-new-connection.png)

5. On the next page, specify the path to the database file. 
	
	![](..\/..\/..\/images/eurd-win-data-source-wizard-select-xml-file.png)
	
	To proceed to the next wizard page, click **Next**.

6. On the next page, you can choose which tables, views and/or stored procedures to add to the report. You can also construct custom queries using the [Query Builder param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } . Click **Finish** to exit the wizard.
	
	![](..\/..\/..\/images/eurd-win-data-source-wizard-select-xml-table.png)
	
	> [!NOTE]
	> Some of the data shaping capabilities available to SQL data sources (such as sorting, grouping and filtering data, as well as using aggregate functions) are not supported for XML files.

The newly created SQL data source will be displayed in the **Data Sources** node of the [Report Explorer param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } . Additionally, the hierarchy of the data source will be reflected by the [Field List param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } .

![](..\/..\/..\/images/eurd-win-data-source-wizard-xml-file-result.png)