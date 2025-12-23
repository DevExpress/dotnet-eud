---
title: Bind a Report to a Federated Master-Detail Data Source
owner: Anna Gubareva
---
# Bind a Report to a Federated Master-Detail Data Source

This topic describes how to create a federated data source that retrieves data from multiple data sources. The topic also shows how to specify a master-detail relationship between these queries.

## Create a Report and Data Sources

1. [Create a new blank report param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } .

2. [Add a SQL data source param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  that provides one data table.

3. [Add an Excel data source param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  that provides the other data table.

    ![](..\/..\/..\/images/eurd-federated-datasource-excel-datasource.png)

## Create Data Federation and Bind the Report to It

1. Click the report's smart tag, expand the **Data Source** property's drop-down menu, and click **Add New DataSource**.

    ![](..\/..\/..\/images/eurd-add-federated-datasource.png)

2. In the invoked [Data Source Wizard param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } , select **Data Federation** and click **Next**.

    ![](..\/..\/..\/images/eurd-data-federation-wizard.png)

3. On the next page, enable check boxes for the SQL data source's table and the Excel data source. The selected items are included in data federation as separate queries.

    Click **Manage Relations** to specify a master-detail relationship between these queries.

    ![](..\/..\/..\/images/eurd-data-federation-choose-data-for-separate-queries.png)

4. In the invoked editor, drag and drop the key field from the master query to the detail query.

    ![](..\/..\/..\/images/eurd-data-federation-master-detail-relationship.png)

5. Click **OK** to close the editor. Click **Finish** to complete the Data Source Wizard.

The Data Source Wizard creates a new **FederationDataSource** that includes two queries with a master-detail relationship. This data source becomes available in the [Report Explorer param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } 's **Data Sources** node. The [Field List param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  reflects the data source's structure.

![](..\/..\/..\/images/eurd-data-federation-master-detail-data-source-structure.png)

The Data Source Wizard specifies query names as follows:

* If the initial data source contains data at the root level (as the Excel data source), the federated query's name equals to the data source name.
* If the initial data source contains one or more queries (as the SQL data source), the federated query's name consists of the data source name and query name separated by an underscore.

You can rename queries in the **Manage Queries** dialog. To invoke it, right-click the data source in the Field List or Report Explorer and select **Manage Queries** in the context menu.

![](..\/..\/..\/images/eurd-data-federation-master-detail-rename-queries.png)

The master-detail relationship's name changes accordingly.

![](..\/..\/..\/images/eurd-data-federation-master-detail-new-query-names.png)

Once you rename the query, update the report's **Data Member** property.

![](..\/..\/..\/images/eurd-data-federation-master-detail-report-data-source-property.png)

## Design the Report Layout

1. Click the report's smart tag and select **Design in Report Wizard**.

    ![](..\/..\/..\/images/eurd-data-federation-master-detail-design-in-report-wizard.png)

2. In the invoked [Report Wizard param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } , select **Table Report** and click **Next**.

    ![](..\/..\/..\/images/eurd-data-federation-report-wizard-table-report.png)

3. Select data members for the report and its [detail reports param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } . Select data fields to display in the report and click **Finish**. You can also go to the [next page param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  to continue layout creation.

    ![](..\/..\/..\/images/eurd-data-federation-master-detail-report-wizard-select-fields.png)

The resulting layout looks similar to the following image:

![](..\/..\/..\/images/eurd-data-federation-master-detail-report-layout-result.png)

Switch to the Preview mode to see the report document.

![](..\/..\/..\/images/eurd-data-federation-master-detail-report-document-result.png)
