---
title: Create a Query or Select a Stored Procedure
author: Anna Vekhina
---

# Create a Query or Select a Stored Procedure

On this wizard page, you can choose which tables, views and/or stored procedures from your data source to display in the report.

## Select Data to Create a Query Automatically

Select tables or views and their particular columns to automatically include them into the a query.

![](../../../../../images/eurd-web-report-wizard-create-a-query-automatically.png)

When a query contains two or more tables you should define master-detail relationships between them on the next wizard page: [Configure Master-Detail Relationships](configure-master-detail-relationships.md).

Otherwise, clicking **Next** will open the next Report Wizard page: [Choose Fields to Display in a Report](choose-fields-to-display-in-a-report.md).

## Manage Custom Queries

When you are required to shape the query data at the level of a data source, you can create custom queries by expanding the **Queries** category and clicking the plus button. 

![](../../../../../images/eurd-web-report-wizard-add-a-query.png)

This will invoke the [Query Builder](../../query-builder.md) where you can create complex queries by joining multiple tables, filtering, sorting and grouping their data, as well as calculating various aggregate functions.

![](../../../../../images/eurd-web-report-wizard-query-builder.png)

To customize an existing query using the Query Builder, click the ![](../../../../../images/eurd-web-report-wizard-edit-query.png) button.

To delete a query, click the ![](../../../../../images/eurd-web-report-wizard-remove-query.png) button.

On finishing the wizard, each of the selected data items will be included into a separate query.

![](../../../../../images/eurd-web-report-wizard-field-list-result.png)

Click **Next** to proceed to the next wizard page: [Configure Query Parameters](configure-query-parameters.md).



