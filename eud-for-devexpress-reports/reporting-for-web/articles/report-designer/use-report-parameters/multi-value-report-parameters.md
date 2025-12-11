---
title: Multi-Value Report Parameters
author: Sergey Andreev
---

# Multi-Value Report Parameters

This document describes how to create a multi-value parameter and use this parameter to [filter report data](../shape-report-data/filter-data.md).

![multi-value-parameters-preview](../../../images/eurd-web-multi-value-parameters-preview.png)

> [!TIP]
> Refer to this help article for information on how to use multi-value parameters in an SQL query: [Specify Query Parameters](../bind-to-data/specify-query-parameters.md#pass-a-multi-value-parameter-value-to-a-query).

## Create a Multi-Value Parameter in the Report Designer

Follow the steps below to create a multi-value parameter in the [Report Designer](../first-look-at-the-report-designer.md):

1. [Create a report parameter](create-a-report-parameter.md) and enable the **Allow multiple values** option.

    ![Enable the Allow multiple values option](../../../images/enable-allow-multiple-value-option.png)

1. Specify a list of predefined values for the parameter. You can create a static list of values or load values from a data source. Refer to the following topics for instructions on how to do it:

    * [Report Parameters with Predefined Static Values](report-parameters-with-predefined-static-values.md)
    * [Report Parameters with Predefined Dynamic Values](report-parameters-with-predefined-dynamic-values.md)

## Filter a Report's Data by a Multi-Value Parameter

To filter a report's data by a multi-value parameter, use the **Is any of** operator for this parameter in the report's [filter string](../shape-report-data/filter-data/filter-data-at-the-report-level.md):

![parameters-multi-value-filter-string](../../../images/eurd-web-parameters-multi-value-filter-string.png)

## Specify Default Values for a Multi-Value Parameter

A multi-value parameter's default values are selected automatically when you open a report's **Print Preview**:

![Specify default values for a multi-value parameter](../../../images/eurd-web-parameters-multi-value-preselect-values.png)

Use one of the following methods to specify default values:

* Click the *Add* button right to the **Value** option and specify a value in a new editor.

    ![Specify default values for a multi-value parameter](../../../images/parameters-multi-value-preselect-values-specify.png)

* Enable the **Select all values** property to populate the parameter value with all items from the parameter's value source (static or dynamic). 

    ![Select all values as defaults for a multi-value parameter](../../../images/multi-value-parameters-select-all.png)

> [!TIP]
> Disable a report's **Request Parameters** property to avoid the **Waiting for parameter values** message on the report's **Print Preview** and display the report with default parameter values.

> [!NOTE]
> Ensure that the type of default values match the parameter type when you specify these values for the parameter.

## Create an Optional Multi-Value Parameter

Optional parameters allow you to filter report data only if parameter values are specified. Otherwise, if parameter values are not set, the parameter is ignored.

![Create an optional multi-value parameter](../../../images/eurd-web-parameters-multi-value-optional.png)

Do the following to make a multi-value parameter optional.

1. Create a multi-value report parameter and specify its **Allow null value**, **Value**, and **Select all values** options as shown below:

    ![parameters-multi-value-optional-settings](../../../images/parameters-multi-value-optional-settings.png)

    | Option | Value |
    | --- | --- |
    | **Allow null value** | **true** |
    | **Value** | Not specified |
    | **Select all values** | **false** |

2. Disable the report's **Request Parameters** property.

    ![report-requestparameters-disable](../../../images/eurd-web-report-requestparameters-disable.png)

3. Assign the following filter condition to the report's filter string:

    ```
    ?category Is Null or [Category ID] In (?category)
    ```

    ![parameters-multi-value-empty-value](../../../images/eurd-web-parameters-multi-value-empty-value.png)

    > [!TIP]
    > You can also use the filter string shown above to filter report data at the data source level. Refer to this help article for more information: [Filter Data at the Data Source Level](../shape-report-data/filter-data/filter-data-at-the-data-source-level.md).