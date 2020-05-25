---
title: Specify Data Source Settings (Object)
owner: Sergey Andreev
---
# Specify Data Source Settings (Object)

This page appears if you selected **Object** on the wizard's start page.

![](../../../../images/eurd-datasource-wizard-object-datasource.png)

## Choose an Object

Select a data object or constructor from the list. If you select a data object, its default constructor is used.

![](../../../../images/eurd-datasource-wizard-object-datasource-select-object.png)

## Choose a Data Member

Select the method that should provide data or select **Entire Object** to bind the report to the object's fields.

![](../../../../images/eurd-report-wizard-object-datasource-select-member.png)

## Configure Parameters

Specify constructor and/or data member parameters, if required.

![](../../../../images/eurd-report-wizard-object-datasource-configure-parameters.png)

You can use expressions to provide data source parameter values. Click the ![](../../../../images/eurd-report-wizard-object-datasource-f-button.png) button to switch the parameter's editor to the expression mode. Specify an expression in the parameter's editor, or click the parameter's ellipsis button to launch the [Expression Editor](../expression-editor.md). You can use [report parameters](../../shape-report-data/use-report-parameters.md) in expressions to specify an input value for a data source parameter.

![](../../../../images/eurd-report-wizard-object-datasource-configure-parameters-expression.png)

To return to the value mode, click the ![](../../../../images/eurd-report-wizard-object-datasource-f-button.png)  button again.

![](../../../../images/eurd-report-wizard-object-datasource-configure-parameters-value.png)

Click **Finish** to close the Data Source Wizard.

Once you finished the wizard, the data source becomes available in the [Report Explorer](../ui-panels/report-explorer.md)'s **Components** node. The [Field List](../ui-panels/field-list.md) reflects the data source structure.

![](../../../../images/eurd-report-wizard-object-datasource-result.png)
