---
title: Create a Query or Select a Stored Procedure
author: Mary Sammal
---
# Create a Query or Select a Stored Procedure
> [!NOTE]
> This wizard step appears only if you're creating a new report from scratch. In this instance, familiarity with database connections is required, so we recommend that you contact your application administrator or vendor for assistance. If you're modifying an existing report, this step will not appear and you will start with the [Choose Fields to Display in a Report](../choose-fields-to-display-in-a-report.md) wizard page.

On this wizard page, you can choose which tables, views and/or stored procedures from your data source to display in the report.

![eurd-win-report-wizard-multi-query-select](../../../../../../../images/eurd-win-report-wizard-multi-query-select.png)

## Manage Custom Queries
When you are required to shape the query data at the level of a data source, you can create custom queries by expanding the **Queries** category and clicking the ![report-wizard-multi-query-page-icon-add](../../../../../../../images/eurd-win-img125532.png) button. This will invoke the [Query Builder](../../../query-builder.md) where you can create complex queries by joining multiple tables, filtering, sorting and grouping their data, as well as calculating various aggregate functions.

![eurd-win-query-builder-diagram-overview](../../../../../../../images/eurd-win-query-builder-diagram-overview.png)

The Query Builder can also be used to specify custom SQL, if this functionality is enabled by your software provider.

To customize an existing query using the Query Builder, click the ![report-wizard-multi-query-page-icon-edit](../../../../../../../images/uerd-win-img125534.png) button.

To delete a query, click the ![report-wizard-multi-query-page-icon-remove](../../../../../../../images/eurd-win-img125533.png) button.

On finishing the wizard, each of the selected data items will be included into a separate query.

![eurd-win-report-field-list](../../../../../../../images/eurd-win-report-field-list.png)

## Specify Master-Detail Relationships
To define [master-detail relationships](../../../../create-popular-reports/create-a-master-detail-report-use-detail-report-bands.md) between two or more queries, click **Manage Relations**.

![eurd-master-detail-relation-editor-categories-products-order-details](../../../../../../../images/eurd-master-detail-relation-editor-categories-products-order-details.png)

To create a new relationship, connect the required key fields using drag and drop.

To edit an existing relationship, double-click the corresponding arrow or right-click it, and select the **Edit Relation** command in the invoked context menu.

![eurd-win-master-detail-relation-editor-edit-relation-context-menu](../../../../../../../images/eurd-win-master-detail-relation-editor-edit-relation-context-menu.png)

This will invoke the **Edit Relation** editor that provides a different UI to manage the data relationships.

![eud-win-reports-edit-relation-editor](../../../../../../../images/eurd-win-edit-relation-dialog.png)

On finishing the wizard, the specified data relationships will appear in the [Field List](../../../ui-panels\field-list.md).

![eurd-win-report-field-list2](../../../../../../../images/eurd-win-report-field-list2.png)

If selected queries or stored procedures contain any [parameters](../../../../shape-report-data/use-report-parameters/use-query-parameters.md), you will be required to define their values on the next wizard page: [Configure Query Parameters](configure-query-parameters.md).

Otherwise, clicking **Next** will open the next Report Wizard page: [Choose Fields to Display in a Report](../choose-fields-to-display-in-a-report.md).