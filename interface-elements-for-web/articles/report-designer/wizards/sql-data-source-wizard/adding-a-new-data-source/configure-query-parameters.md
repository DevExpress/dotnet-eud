---
title: Configure Query Parameters
---
# Configure Query Parameters
This page is displayed if any custom queries and/or parameterized stored procedures were selected on the [previous wizard page](../../../../../../interface-elements-for-web/articles/report-designer/wizards/sql-data-source-wizard/adding-a-new-data-source/create-a-query-or-select-a-stored-procedure.md).

On this page, you can manage parameters that are used in queries and/or stored procedures and specify parameter values.

To add a new parameter, select a query and click the ![web-designer-report-wizard-button-query-add](../../../../../images/Img125709.png) button.

![web-designer-report-wizard-03-configure-parameters](../../../../../images/Img125712.png)

To delete a parameter, click the ![web-designer-report-wizard-button-query-delete](../../../../../images/Img125711.png) button.

To customize an existing parameter, click the ![web-designer-report-wizard-button-query-edit](../../../../../images/Img125710.png) button.

Next, you can specify the parameter name, type and value.

![web-designer-report-wizard-04-configure-parameters-expression](../../../../../images/Img125713.png)

When the parameter type is set to **Expression**, the value editor displays the ellipsis button, and clicking on it invokes the [Expression Editor](../../../../../../interface-elements-for-web/articles/report-designer/interface-elements/expression-editor.md).

![web-designer-expression-editor](../../../../../images/Img125714.png)

To link a query parameter to an existing report parameter, type the report parameter name using the following syntax: **[parameters.parameter1]**.

Click **Next** to proceed to the next wizard page: [Configure Master-Detail Relationships](../../../../../../interface-elements-for-web/articles/report-designer/wizards/sql-data-source-wizard/adding-a-new-data-source/configure-master-detail-relationships.md).

> When invoking the SQL Data Source Wizard to edit an existing data source, [another version](../../../../../../interface-elements-for-web/articles/report-designer/wizards/sql-data-source-wizard/editing-an-existing-data-source/create-a-query-or-select-a-stored-procedure.md) of this page is displayed.
> 
> This version is also shown if your software vendor switched the SQL Data Source Wizard to the single-query mode.