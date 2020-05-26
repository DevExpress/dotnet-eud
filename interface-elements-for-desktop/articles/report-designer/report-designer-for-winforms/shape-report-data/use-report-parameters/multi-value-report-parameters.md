---
title: Multi-Value Report Parameters
author: Sergey Andreev
---
# Multi-Value Report Parameters

This document describes how to create a multi-value parameter and [filter report data](../filter-data.md) by the specified parameter values.

![Multi-Value Parameter in Preview](../../../../../images/eurd-win-multi-value-parameters-preview.png)

## Create a Multi-Value Parameter

1. [Create a report parameter](create-a-report-parameter.md) and enable the **Allow multiple values** option.

    ![Create Multi-Value Parameter](../../../../../images/eurd-win-multi-value-parameters-create-parameter.png)

1. Specify a list of predefined values for the parameter. See the following topics for more information:

    * [Report Parameters with Predefined Static Values](report-parameters-with-predefined-static-values.md) - to directly specify the list of values.
    * [Report Parameters with Predefined Dynamic Values](report-parameters-with-predefined-dynamic-values.md) - to specify the storage that contains the list of values.

## Filter a Report by a Multi-Value Parameter

Use the **Is any of** operator in the report’s [filter string](../filter-data/filter-data-at-the-report-level.md):

![Filter Report by Multi-Value Parameter](../../../../../images/eurd-win-parameters-multi-value-filter-string.png)

## Pre-Select Parameter Values

Use one of the following methods to pre-select multiple parameter values when a report is first rendered.

![Multi-Value Parameter - Preselect Values](../../../../../images/eurd-win-parameters-multi-value-preselect-values.png)

* Assign an array of values to the **Default Value** property.  

    ![Specify Multi-Value Parameters Preselected Values](../../../../../images/eurd-win-parameters-multi-value-preselect-values-specify.png)

* Set the **Expression** property to an expression that evaluates to an array of values. You can use data source fields and other parameters in expressions.

    ![Set Expression to Preselect Multi-Value Parameter Values](../../../../../images/eurd-win-parameters-multi-value-preselect-values-expression.png)

* Enable the **Select all values** property to populate the parameter value with all items from its data source (static or dynamic).

    ![Select All Multi-Value Parameter Values](../../../../../images/eurd-win-multi-value-parameters-select-all.png)

> [!TIP]
> Disable the report's **Request Parameters** property to avoid the **Waiting for parameter values** message in **Preview** and display the report with pre-selected parameter values.

## Optional Multi-Value Parameter

You can leave the parameter unspecified and display all report data, or choose parameter values to filter the report.

![Optional Multi-Value Parameter](../../../../../images/eurd-win-parameters-multi-value-optional.png)

Do the following to make a multi-value parameter optional.

1. Configure the parameter:

    ![parameters-multi-value-optional-settings](../../../../../images/eurd-win-parameters-multi-value-optional-settings.png)

    | Property | Value |
    | --- | --- |
    | **Allow null value** | Checked |
    | **Default Value** | Not specified |
    | **Expression** | Not specified |
    | **Select all values** | Unchecked |

1. Disable the report's **Request Parameters** property.

    ![Disable Request Parameters](../../../../../images/eurd-win-report-requestparameters-disable.png)

1. Use the following report filter string:

    ```
    ?category Is Null or [CategoryID] In (?category)
    ```

![Empty Multi-Value Parameter](../../../../../images/eurd-win-parameters-multi-value-empty-value.png)

> [!TIP]
> You can also use the filter string shown above to [filter report data at the data source level](../filter-data/filter-data-at-the-data-source-level.md).