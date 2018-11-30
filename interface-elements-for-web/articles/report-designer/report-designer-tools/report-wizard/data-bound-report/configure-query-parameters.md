---
title: Configure Query Parameters
author: Anna Vekhina
---
# Configure Query Parameters

On this wizard page, you can manage parameters that are used in queries and/or stored procedures selected on the [previous wizard page](create-a-query-or-select-a-stored-procedure.md), as well as specify parameter values.

## Specify Parameter Values

A parameter value can be specified in one of the following ways.
* Parameters can be assigned static values (according to the specified parameter type), which is illustrated in the following image.
	
	![](../../../../../images/eurd-web-data-source-wizard-multi-query-configure-parameters-static-values-date-time.png)

* Alternatively, you can calculate a parameter value based on an expression. To do this, expand the **Type** property's drop-down list and select **Expression**. Click the **Value** property's ellipsis button and construct an expression in the invoked **Expression Editor**. 

    ![](../../../../../images/eurd-web-data-source-wizard-configure-query-parameters-expression-editor.png)

    You can map a [report parameter](../../../shape-report-data/use-report-parameters.md) that already exists in a report to a query parameter.
	
	![](../../../../../images/eurd-web-report-wizard-page-multi-query-parameters.png)

## Manage Parameters

To create a new query parameter, select a query and click **Add parameter**.

![](../../../../../images/eurd-web-report-wizard-add-query-parameter.png)

Select a parameter on this wizard page and click the **Edit** ![](../../../../../images/eurd-web-report-wizard-edit-query.png) button to specify its properties or click the **Remove** ![](../../../../../images/eurd-web-report-wizard-remove-query.png) button to delete it.

![](../../../../../images/eurd-web-report-wizard-edit-query-parameter.png)

When the resulting query contains two or more queries you should define master-detail relationships between them on the next wizard page: [Configure Master-Detail Relationships](configure-master-detail-relationships.md).

Otherwise, clicking **Next** will open the next Report Wizard page: [Choose Fields to Display in a Report](choose-fields-to-display-in-a-report.md).
