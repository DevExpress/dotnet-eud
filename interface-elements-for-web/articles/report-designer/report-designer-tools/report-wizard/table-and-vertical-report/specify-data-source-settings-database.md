---
uid: '400958'
title: Specify Data Source Settings (Database)
owner: Anna Gubareva
---
# Specify Data Source Settings (Database)

This page appears if you selected **Database** on the [previous page](select-data-source.md). 


![](../../../../../images/eurd-web-report-wizard-database-settings.png)


## Choose a Data Connection

Select a data connection from the list.

![](../../../../../images/eurd-web-report-wizard-choose-data-connection.png)

## Choose Queries

Check tables, views and/or stored procedures to include them in a data source as separated queries.

![](../../../../../images/eurd-web-report-wizard-choose-queries.png)

You can also check specific data fields.

![](../../../../../images/eurd-web-report-wizard-choose-data-fields.png)

To join multiple data tables and shape the resulting data, click the **Queries** category's plus button to invoke the [Query Builder](../../query-builder.md) and create a custom query.

![](../../../../../images/eurd-web-report-wizard-query-builder.png)

If you enabled custom SQL queries, the plus button invokes a context menu. You can choose whether to run the Query Builder or Custom SQL Editor.

![](../../../../../images/eurd-web-report-wizard-custom-query-menu.png)

You can click the ![](../../../../../images/eurd-web-report-wizard-edit-query-button.png) button to customize the query or the ![](../../../../../images/eurd-web-report-wizard-remove-query-button.png) button to remove the query.

Once you finished the wizard, the data source becomes available in the [Report Explorer](../../ui-panels/report-explorer.md)'s **Data Sources** node. The [Field List](../../ui-panels/field-list.md) reflects the data source structure.

![](../../../../../images/eurd-web-report-wizard-queries-result.png)

## Configure Master-Detail Relationships

This step is available when you selected two or more queries. 

To create a master-detail relationship, click the master query's plus button, select the detail query in the invoked list, and connect the key fields.

![](../../../../../images/eurd-web-report-wizard-master-detail-relationship.png)

After the wizard is completed, the Field List reflects the master-detail hierarchy.

![](../../../../../images/eurd-web-report-wizard-master-detail-result.png)

## Configure Query Parameters

This step is available if you selected a parameterized stored procedure or created a custom query.

Select a query and click the plus button to add a new parameter.

![](../../../../../images/eurd-web-report-wizard-query-parameters.png)

Click the ![](../../../../../images/eurd-web-report-wizard-edit-query-button.png) button to customize the parameter or the ![](../../../../../images/eurd-web-report-wizard-remove-query-button.png) button to remove it.

You can use the following approaches to specify a parameter value:

* **Assign a static value**

    Select a query parameter's type from the **Type** drop-down list and specify a value based on the selected type.

    ![](../../../../../images/eurd-web-report-wizard-parameter-static-value.png)

* **Provide a dynamic parameter value** 

    Set the **Type** option to **Expression** and specify the **Result Type**. Click the **Value** option's ellipsis button and construct an expression in the invoked.

    ![](../../../../../images/eurd-web-report-wizard-parameter-dynamic-value.png)

    If you design the current report in the wizard, you can map a query parameter to an existing report parameter. To do this, use the **?parameterName** syntax.

    ![](../../../../../images/eurd-web-report-wizard-parameter-mapping.png)
