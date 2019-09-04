---
title: 'Bind a Report to an Object Data Source'
author: Sergey Andreev
---

# Bind a Report to an Object Data Source

This topic describes how to bind a report to object data at design time.

## Create a Project and Prepare a Data Source

1. [Create a new report](../../report-designer/add-new-reports.md).

2. Select **Add Data Source** from the [designer menu](../report-designer-tools/menu.md).
	
    ![](../../../images/eurd-web-choose-data-source.png)

    This invokes the [Data Source Wizard](../report-designer-tools/data-source-wizard.md).

3. Choose **Object** and click **Next**.
	
    ![](../../../images/eurd-web-data-source-object.png)

4. Specify data source settings on the next screen.

    ![](../../../images/eurd-datasource-wizard-object-datasource.png)

    * Select an object type and constructor from the list. If you select an object type, the default constructor is invoked.

        ![](../../../images/eurd-datasource-wizard-object-datasource-select-object.png)

    * Select the method that should provide data. Alternatively, select **Entire Object** to bind to the object's fields.

        ![](../../../images/eurd-report-wizard-object-datasource-select-member.png)

    * Specify input values for the constructor (if you selected a constructor that requires input values). Specify input values for the data member (if you selected a data member that requires input values).

        ![](../../../images/eurd-report-wizard-object-datasource-configure-parameters.png)

        You can use expressions to provide data source parameter values. Click a parameter's marker and select **Expression** from the popup menu to switch the parameter's editor to the expression mode. Specify an expression in the parameter's editor, or click the parameter's ellipsis button to launch the [Expression Editor](../report-designer-tools/expression-editor.md). You can use [report parameters](../shape-report-data/use-report-parameters.md) in expressions to specify an input value for a data source parameter.

        ![](../../../images/eurd-report-wizard-object-datasource-configure-parameters-expression.png)

Click **Finish** to close the Data Source Wizard.

After you finish the wizard, it creates an **ObjectDataSource** component. This component retrieves the data fields that the selected object type includes. The [Field List](../report-designer-tools/ui-panels/field-list.md) reflects the data source structure.

![](../../../images/eurd-report-wizard-object-datasource-result.png)

## Configure Parameters

Choose an **ObjectDataSource** component in the Field List and click **Edit Parameters**. Reconfigure the parameters on the invoked wizard page and click **Finish** to apply changes.

![](../../../images/eurd-web-data-source-wizard-object-edit-parameters.png)
