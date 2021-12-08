---
title: Multi-Value Report Parameters
author: Sergey Andreev
---

# Multi-Value Report Parameters

This document describes how to create a multi-value parameter and use this parameter to [filter report data](../shape-report-data/filter-data.md).

![multi-value-parameters-preview](../../../../images/multi-value-parameters-preview118131.png)

> [!TIP]
> Refer to this help article for information on how to use multi-value parameters in an SQL query: [Specify Query Parameters](../bind-to-data/specify-query-parameters.md#PassMultiValueParameterValueToQuery).

## Create a Multi-Value Parameter in the Report Designer

Follow the steps below to create a multi-value parameter in the [Report Designer](../first-look-at-the-report-designer.md):

1. [Create a report parameter](create-a-report-parameter.md) and enable the **Allow multiple values** option.

    ![Enable the Allow multiple values option](../../../../images/enable-allow-multiple-value-option.png)

1. Specify a list of predefined values for the parameter. You can create a static list of values or load values from a data source. Refer to the following topics for instructions on how to do it:

    * [Report Parameters with Predefined Static Values](report-parameters-with-predefined-static-values.md)
    * [Report Parameters with Predefined Dynamic Values](report-parameters-with-predefined-dynamic-values.md)

## Filter a Report's Data by a Multi-Value Parameter

To filter a report's data by a multi-value parameter, use the **Is any of** operator for this parameter in the report's filter string:

![parameters-multi-value-filter-string](../../../../images/parameters-multi-value-filter-string.png)

The filtered report is displayed after you specify parameter values.

![parameters-multi-value-filter-report](../../../../images/parameters-multi-value-filter-report.png)

## Specify Default Values for a Multi-Value Parameter

A multi-value parameter's default values are selected automatically when you open a report's **Print Preview**:

![Specify default values for a multi-value parameter](../../../../images/parameters-multi-value-preselect-values.png)

Use one of the following methods to specify default values:

* Assign an array of values to the **Default Value** option.

    ![Specify default values for a multi-value parameter](../../../../images/parameters-multi-value-preselect-values-specify.png)

* Enable the **Select all values** property to populate the parameter value with all items from the parameter's value source (static or dynamic). 

    ![Select all values as defaults for a multi-value parameter](../../../../images/multi-value-parameters-select-all.png)

> [!TIP]
> Disable a report's **Request Parameters** property to avoid the **Waiting for parameter values** message on the report's **Print Preview** and display the report with default parameter values.

> [!NOTE]
> Ensure that the type of default values match the parameter type when you specify these values for the parameter.

## Create an Optional Multi-Value Parameter

Optional parameters allow you to filter report data only if parameter values are specified. Otherwise, if parameter values are not set, the parameter is ignored.

![Create an optional multi-value parameter](../../../../images/parameters-multi-value-optional.png)

Do the following to make a multi-value parameter optional.

1. Create a multi-value report parameter and specify its **Allow null value**, **Default Value**, and **Select all values** options as shown below:

    ![parameters-multi-value-optional-settings](../../../../images/parameters-multi-value-optional-settings.png)

    | Option | Value |
    | --- | --- |
    | **Allow null value** | **true** |
    | **Default Value** | Not specified |
    | **Select all values** | **false** |

2. Disable the report's **Request Parameters** property.

    ![report-requestparameters-disable](../../../../images/report-requestparameters-disable.png)

3. Assign the following filter condition to the report's filter string:

    ```
    ?category Is Null or [Category ID] In (?category)
    ```

    ![parameters-multi-value-empty-value](../../../../images/parameters-multi-value-empty-value.png)

    > [!TIP]
    > You can also use the filter string shown above to filter report data at the data source level. Refer to this help article for more information: [Filter Data at the Data Source Level](../shape-report-data/filter-data/filter-data-at-the-data-source-level.md).

# Multi-Value Report Parameters (Old)

This document describes how to create a multi-value parameter and [filter report data](../filter-data.md) by the specified parameter values.

![Multi-Value Parameter in Preview](../../../../images/eurd-web-multi-value-parameters-preview.png)

## Create a Multi-Value Parameter

1. [Create a report parameter](create-a-report-parameter.md) and enable the **Multi-Value** option.

    ![Create Multi-Value Parameter](../../../../images/eurd-web-multi-value-parameters-create-parameter.png)

1. Specify a list of predefined values for the parameter. See the following topics for more information:

    * [Report Parameters with Predefined Static Values](report-parameters-with-predefined-static-values.md) - to directly specify the list of values.
    * [Report Parameters with Predefined Dynamic Values](report-parameters-with-predefined-dynamic-values.md) - to specify the storage that contains the list of values.

## Filter a Report by a Multi-Value Parameter

Use the **Is any of** operator in the report’s [filter string](../filter-data/filter-data-at-the-report-level.md):

![Filter Report by Multi-Value Parameter](../../../../images/eurd-web-parameters-multi-value-filter-string.png)

## Pre-Select Parameter Values

Use one of the following methods to pre-select multiple parameter values when a report is first rendered.

![Multi-Value Parameter - Preselect Values](../../../../images/eurd-web-parameters-multi-value-preselect-values.png)

* Assign an array of values to the parameter.

    ![Specify Multi-Value Parameters Preselected Values](../../../../images/eurd-web-parameters-multi-value-preselect-values-specify.png)

* Set the **Expression** property to an expression that evaluates to an array of values. You can use data source fields and other parameters in expressions.

    ![Set Expression to Preselect Multi-Value Parameter Values](../../../../images/eurd-web-parameters-multi-value-preselect-values-expression.png)

* Enable the **Select All Values** property to populate the parameter value with all items from its data source (static or dynamic).

    ![Select All Multi-Value Parameter Values](../../../../images/eurd-web-multi-value-parameters-select-all.png)

> [!TIP]
> Disable the report's **Request Parameters** property to avoid the **Waiting for parameter values** message in **Preview** and display the report with pre-selected parameter values.

## Optional Multi-Value Parameter

You can leave the parameter unspecified and display all report data, or choose parameter values to filter the report.

![Optional Multi-Value Parameter](../../../../images/eurd-web-parameters-multi-value-optional.png)

Do the following to make a multi-value parameter optional.

1. Configure the parameter:

    ![parameters-multi-value-optional-settings](../../../../images/eurd-web-parameters-multi-value-optional-settings.png)

    | Property | Value |
    | --- | --- |
    | **Allow Null** | Checked |
    | **Value** | Not specified |
    | **Expression** | Not specified |
    | **Select All Values** | Unchecked |

1. Disable the report's **Request Parameters** property.

    ![Disable Request Parameters](../../../../images/eurd-web-report-requestparameters-disable.png)

1. Use the following report filter string:

    ```
    ?category Is Null or [CategoryID] In (?category)
    ```

![Empty Multi-Value Parameter](../../../../images/eurd-web-parameters-multi-value-empty-value.png)

> [!TIP]
> You can also use the filter string shown above to [filter report data at the data source level](../filter-data/filter-data-at-the-data-source-level.md).