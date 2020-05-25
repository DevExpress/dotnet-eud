---
title: Create a Report Parameter
author: Sergey Andreev
---
# Create a Report Parameter

This topic describes how to create a basic report parameter and specify its value.

## Create a Parameter

The Report Designer offers multiple ways to create a parameter:

* Right-click **Parameters** in the the [Field List](../../report-designer-tools/ui-panels/field-list.md) and select **Add Parameter** from the context menu.

    ![Field List - Add Parameter](../../../../../images/eurd-win-fieldlist-add-parameter.png)

* Select the report and click the **Parameters** property's ellipsis button in the [Property Grid](../../report-designer-tools/ui-panels/property-grid.md). Click **Add** in the invoked **Report Parameters Editor** dialog.

    ![Create Report Parameter from PRoperty Grid](../../../../../images/eurd-win-create-report-parameter-from-property-grid.png)

* Create a parameter in-place in dialogs and wizards. The image below shows how to create a parameter in a [FilterString Editor](../../use-expressions.md#filterstring-editor). Select **Add Parameter** from the context menu when you construct a condition.

    ![Filter String - Add Parameter](../../../../../images/eurd-win-parameters-filter-string-add-parameter.png)

Specify the following basic options:

| Option | Description |
| --- | --- |
| **Name** | A parameter should have a unique name with which you can refer to this parameter in expressions and filter strings. |
| **Type** | Specifies which values a parameter can accept. |
| **Default Value** or **[Expression](../../use-expressions.md#expression-syntax)** | Specifies a parameter's value. Expressions can include data source fields or other parameters. When evaluated, expressions are parsed and processed to obtain a value. |

## Use the Parameters Panel to Ask for User Input

Enable the **Show in the parameters panel** option to make your report interactive. The Preview displays the **Parameters** panel that shows editors for report parameters marked as visible. This allows you to specify a value before the report is rendered. Specify the parameter's **Description** to display the editor's caption in the **Parameters** panel.

![Parameters Panel](../../../../../images/eurd-win-parameters-create-date-parameter.png)

> [!TIP]
> Disable the report's **Request Parameters** property to avoid the **Waiting for parameter values** message in **Preview** and display the report with default parameter values.

Enable the **Allow null value** property if the parameter's value can be unspecified.

The following image shows editors for different parameter types.

![Parameter Editors](../../../../../images/eurd-win-parameter-editors.png)
