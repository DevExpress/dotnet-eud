---
uid: '400920'
title: Bind a Report to a Federated Data Source
owner: Anna Gubareva
seealso: 
- linkId: "400921"
- linkId: "400922"
- linkId: "400923"
---
# Bind a Report to a Federated Data Source

This topic describes how to create a federated data source that joins data from multiple data sources into a single query. 

## Create a Report and Data Sources

1. [Create a new blank report](xref:4270).

2. [Add a SQL data source](xref:2554) that provides information about categories. For instance, bind to the **Northwind** database's **Categories** table. You can use the **nwind.mdb** file from the XtraReports installation (the default path is _C:\Users\Public\Public Documents\DevExpress Demos 19.1\Components\Data\nwind.mdb_).

3. [Add an Excel data source](xref:114900) that provides information about products.

    ![](~/images/data-federation-initial-data-sources.png)

## Create Data Federation and Bind the Report to It

1. Click the report's smart tag, expand the **DataSource** property's drop-down menu and click **Add Report Data Source**.

    ![](~/images/data-federation-report-smart-tag.png)

2. In the invoked [Data Source Wizard](xref:120164), select **Data Federation** and click **Next**.

    ![](~/images/data-federation-wizard-choose-data-federation.png)

3. On the next page, click **Add Query**.

    ![](~/images/data-federation-wizard-add-query.png)

4. In the invoked [Query Builder](xref:17308), drag and drop the **Categories** table onto the design surface.

    ![](~/images/data-federation-query-builder-drop-table.png)

5. Drag and drop the Excel data source onto the design surface. In the invoked **Join Editor**, select the **Inner join** type and create a join relationship based on the **CategoryID** key field.

    ![](~/images/data-federation-query-builder-join-tables.png)

6. Enable check boxes for the data fields you want to include in the query result set.

    ![](~/images/data-federation-query-builder-select-fields.png)

7. Click **OK** to close the Query Builder. Click **Finish** to complete the Data Source Wizard.
 
The Wizard creates a new **FederationDataSource** that includes the single **Categories** query. This data source becomes available in the [Report Explorer](xref:4258)'s **Components** node. The [Field List](xref:4259) reflects the data source structure. 

![](~/images/data-federation-data-source-structure.png)

The federated query's default name equals to the main table's name (the **Categories** table in this tutorial). You can rename this query in the **Manage Queries** dialog. To invoke it, right-click the data source in the Field List or Report Explorer and select **Manage Queries** in the context menu.

![](~/images/data-federation-rename-query.png)

Once you rename the query, update the report's **DataMember** property.

![](~/images/data-federation-report-data-source-property.png)

## Design the Report Layout

1. Click the report's smart tag and select **Design in Report Wizard**.

    ![](~/images/data-federation-design-in-report-wizard.png)

2. In the invoked [Report Wizard](xref:4254), select **Table Report** and click **Next**.

    ![](~/images/data-federation-report-wizard-table-report.png)

3. Select data fields to display in the report and click **Finish**. You can also go to the [next page](xref:115541) to continue layout creation.

    ![](~/images/data-federation-report-wizard-select-fields.png)

The resulting layout looks similar to the following image:

![](~/images/data-federation-report-layout-result.png)

Switch to the Preview tab to see the report document.

![](~/images/data-federation-report-document-result.png)
