---
title: Create a Report Parameter
author: Sergey Andreev
---

# Create a Report Parameter

This topic demonstrates how to create a report parameter in the [Report Designer](../first-look-at-the-report-designer.md). The topic also describes the [options](#parameter-options) you can specify for a report parameter.

## Create a Report Parameter in the Report Designer

In the **Report Designer**, you can create a parameter from the [Field List](../report-designer-tools/ui-panels/field-list.md), [Properties panel](../report-designer-tools/ui-panels/properties-panel.md), or [Filter Editor](../use-expressions.md#filter-editor). The created parameter appears in the [Field List](../report-designer-tools/ui-panels/field-list.md)'s **Parameters** node.

![A parameter in the Field List](../../../../images/field-list-parameters-section.png)

### Create From the Field List

Right-click the **Parameters** node in the [Field List](../report-designer-tools/ui-panels/field-list.md) and select **Add Parameter**.

![Create a parameter from the Field List](../../../../images/field-list-add-parameter.png)

Specify [parameter options](#parameter-options) in the invoked **Add New Parameter** dialog and click *OK*.

![Add New Parameter dialog](../../../../images/add-new-parameter-dialog.png)

### Create From the Properties Window

Select a report and click the **Parameters** property's ellipsis button in the [Properties panel](../report-designer-tools/ui-panels/properties-panel.md).

![Create a parameter from the Properties panel](../../../../images/property-grid-add-parameter.png)

Click **Add** in the invoked **Report Parameters Editor** dialog to add a new parameter. Specify [parameter options](#parameter-options) and click *OK*.

![Report Parameters Editor](../../../../images/report-parameters-editor.png)

### Create From the FilterString Editor

You can create a parameter when you construct a condition in the [Filter Editor](../use-expressions.md#filter-editor). Choose the **Select a parameter** field, click the field, and select **Add Parameter** in the invoked context menu.

![Create a parameter from the Filter String editor](../../../../images/filter-string-editor-add-parameter.png)

Specify [parameter options](#parameter-options) in the invoked **Add New Parameter** dialog and click *OK*.

![Add New Parameter dialog](../../../../images/add-new-parameter-dialog.png)

## Parameter Options

### Name

The name by which you can [reference a parameter in a report](reference-report-parameters.md). Note that report parameters should have unique names.

### Description

A parameter description that appears on a report's **Print Preview** in the [Parameters panel](parameters-panel.md).

![Parameter description](../../../../images/parameter-description.png)

### Visible

Specifies whether a parameter is visible in the [Parameters panel](parameters-panel.md).

![Parameter editor](../../../../images/parameter-editor.png)

You can assign an [expression](../use-expressions.md) to this option. The example below specifies an expression that shows/hides a parameter based on a value of another parameter.

![Specify an expression for the Visible option](../../../../images/specify-expression-for-visible-option.png)

![Show/hide a parameter's editor based on a value of another parameter](../../../../images/show-hide-parameter-editor.gif)

### Enabled

Specifies whether a parameter editor is enabled or disabled in the [Parameters panel](parameters-panel.md). You can set this option to **No** to make a parameter's [default value](#default-value) read-only.

![Disabled parameter editor](../../../../images/disabled-parameter-editor.png)

You can also assign an [expression](../use-expressions.md) to this option. The example below specifies an expression that enables/disables a parameter's editor based on a value of another parameter.

![Specify an expression for the Enabled option](../../../../images/specify-expression-for-enabled-option.png)

![Enable/disable a parameter's editor based on a value of another parameter](../../../../images/enable-disable-parameter-editor.gif)

### Type

The type of parameter values. The following types are available:

* String;
* Date;
* Number (16-bit integer);
* Number (32-bit integer);
* Number (64-bit integer);
* Number (floating point);
* Number (double-precision floating point);
* Number (decimal);
* Boolean;
* GUID (Globally Unique Identifier).

### Default Value

A parameter's default value. This value is displayed in the [Parameters panel](parameters-panel.md) when you open a report's **Print Preview**.

You can specify an [expression](../use-expressions.md) for this option. For example, set this option to **Now()** to use the current date as a date parameter's default value.

![Specify an expression for a parameter's Default Value option](../../../../images/specify-expression-for-parameter-default-value.png)

> [!NOTE]
> You can use only [constants](../use-expressions/expression-syntax.md#constants), [operators](../use-expressions/expression-syntax.md#operators), and date-time / logical / math / string [functions](../use-expressions/expression-syntax.md#functions-basic) in an expression for a parameter's default value.

### Allow Null Value

When the **Allow Null Value** option is enabled, you can leave the parameter's value unspecified.

![Allow Null Value option](../../../../images/parameter-editor-null-value.png)

### Allow Multiple Values

When the **Allow Multiple Values** option is enabled, you can specify multiple values for a report parameter.

![Allow Multiple Values option](../../../../images/parameter-editor-multiple-values.png)

### Select All Values

Enable the **Select All Values** option to use all elements from a [custom set of values](#value-source) as a parameter's [default value](#default-value).

> [!NOTE]
> You can specify the **Select All Values** option only when the **Allow Multiple Values** option is enabled.

### Value Source

Use the **Value Source** option to specify a custom set of values a parameter can accept. You can create a static list of values, load values from a data source, or specify a date range. Refer to the following topics for more details:

* [Report Parameters with Predefined Static Values](report-parameters-with-predefined-static-values.md)
* [Report Parameters with Predefined Dynamic Values](report-parameters-with-predefined-dynamic-values.md)
* [Date Range Report Parameters](date-range-report-parameters.md)

# Create a Report Parameter (Old)

This topic describes how to create a basic report parameter and specify its value.

## Create a Parameter

Click the ![plus](../../../../images/eurd-web-parameters-button-plus.png) button next to **Parameters** in the the [Field List](../../report-designer-tools/ui-panels/field-list.md) to invoke the **Add Parameter** dialog.

![Field List - Add Parameter](../../../../images/eurd-web-fieldlist-add-parameter.png)

Specify the following basic options:

| Option | Description |
| --- | --- |
| **Name** | A parameter should have a unique name. You can use this name to refer to this parameter in expressions and filter strings. |
| **Type** | Specifies which values a parameter can accept. |
| **Value** or **[Expression](../../use-expressions.md#expression-syntax)** | Specifies a parameter's value. Expressions can include data source fields or other parameters. When evaluated, expressions are parsed and processed to obtain a value. |

## Use the Parameters Panel to Ask for User Input

Enable the **Visible** option to make your report interactive. The Preview displays the **Parameters** panel that shows editors for report parameters marked as visible. This allows you to specify a value before the report is rendered. Specify the parameter's **Description** to display the editor's caption in the **Parameters** panel.

![Parameters Panel](../../../../images/eurd-web-parameters-create-date-parameter.png)

> [!TIP]
> Disable the report's **Request Parameters** property to avoid the **Waiting for parameter values** message in **Preview** and display the report with default parameter values.

Enable the **Allow Null** property if the parameter's value can be unspecified.

The following image shows editors for different parameter types.

![Parameter Editors](../../../../images/eurd-web-parameter-editors.png)
