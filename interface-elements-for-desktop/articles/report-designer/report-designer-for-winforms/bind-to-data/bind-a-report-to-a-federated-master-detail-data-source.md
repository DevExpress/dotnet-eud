---
uid: '400921'
title: Bind a Report to a Federated Master-Detail Data Source
owner: Anna Gubareva
seealso: 
- linkId: "400920"
- linkId: "400922"
- linkId: "400923"
---
# Bind a Report to a Federated Master-Detail Data Source

This topic describes how to create a federated data source that retrieves data from multiple data sources into separate queries. The topic also shows how to specify a master-detail relationship between these queries. 

## Create a Report and Data Sources

1. [Create a new blank report](xref:4270).

2. [Add a SQL data source](xref:2554) that provides information about categories. For instance, bind the report to the **Northwind** database's **Categories** table. You can use the **nwind.mdb** file from the XtraReports installation (the default path is _C:\Users\Public\Public Documents\DevExpress Demos 19.1\Components\Data\nwind.mdb_).

3. [Add an Excel data source](xref:114900) that provides information about products.

    ![](~/images/data-federation-initial-data-sources.png)

## Create Data Federation and Bind the Report to It

1. Click the report's smart tag, expand the **DataSource** property's drop-down menu, and click **Add Report Data Source**.

    ![](~/images/data-federation-report-smart-tag.png)

2. In the invoked [Data Source Wizard](xref:120164), select **Data Federation** and click **Next**.

    ![](~/images/data-federation-wizard-choose-data-federation.png)

3. On the next page, enable check boxes for the SQL data source's **Categories** table and the Excel data source. The selected items are included to data federation as separate queries.

    Click **Manage Relations** to specify a master-detail relationship between these queries.

    ![](~/images/data-federation-choose-data-for-separate-queries.png)

4. In the invoked editor, drag and drop the **CategoryID** key field from the master query (**Categories**) to the detail query (**Products**).

    ![](~/images/data-federation-master-detail-relationship.png)

5. Click **OK** to close the editor. Click **Finish** to complete the Data Source Wizard.

The Wizard creates a new **FederationDataSource** that includes two queries with a master-detail relationship. This data source becomes available in the [Report Explorer](xref:4258)'s **Components** node. The [Field List](xref:4259) reflects the data source structure. 

![](~/images/data-federation-master-detail-data-source-structure.png)

The Wizard specifies query names as follows:

* If the initial data source contains data at the root level (as the Excel data source), the federated query's name equals to the data source name.
* If the initial data source contains one or more queries (as the SQL data source), the federated query's name consists of the data source name and query name separated by the underscore.

You can rename queries in the **Manage Queries** dialog. To invoke it, right-click the data source in the Field List or Report Explorer and select **Manage Queries** in the context menu.

![](~/images/data-federation-master-detail-rename-queries.png)

The master-detail relationship's name changes accordingly.

![](~/images/data-federation-master-detail-new-query-names.png)

Once you rename the query, update the report's **DataMember** property.

![](~/images/data-federation-master-detail-report-data-source-property.png)

## Design the Report Layout

1. Click the report's smart tag and select **Design in Report Wizard**.

    ![](~/images/data-federation-master-detail-design-in-report-wizard.png)

2. In the invoked [Report Wizard](xref:4254), select **Table Report** and click **Next**.

    ![](~/images/data-federation-report-wizard-table-report.png)

3. Select data members for the report and its [detail reports](xref:4785). Select data fields to display in the report and click **Finish**. You can also go to the [next page](xref:115541) to continue layout creation.

    ![](~/images/data-federation-master-detail-report-wizard-select-fields.png)

The resulting layout looks similar to the following image:

![](~/images/data-federation-master-detail-report-layout-result.png)

Switch to the Preview tab to see the report document.

![](~/images/data-federation-master-detail-report-document-result.png)