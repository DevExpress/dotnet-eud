---
title: Use Report Parameters
author: Sergey Andreev
---

# Use Report Parameters

Report parameters allow you to filter report data dynamically.

![Report parameters example](../../images/eurd-web-report-parameters-example.gif)

## Supported Features/Capabilities

* Built-in parameter types (String, Date, Number, Boolean, and GUID)

    ![Built-in parameter types](../../images/eurd-web-built-in-parameter-types.png)

* [Multi-value parameters](use-report-parameters/multi-value-report-parameters.md) (filter report data against multiple criteria)

    ![Multi-value report parameters](../../images/eurd-web-parameter-editor-multiple-values.png)

* [Cascading parameters](use-report-parameters/cascading-report-parameters.md) (filter a parameter’s value list against selections made in a different parameter)

    ![Cascading report parameters](../../images/cascadingparametersresult124540.png)

* [Date-range parameters](use-report-parameters/date-range-report-parameters.md) (filter report data against a specified time period)

    ![Date-range report parameters](../../images/eurd-web-date-range-report-parameters.png)

* [Static parameter values](use-report-parameters/report-parameters-with-predefined-static-values.md) (create pre-defined (static) parameter value lists)

    ![Static parameter values](../../images/eurd-web-static-parameter-values.png)

* [Dynamic parameter values](use-report-parameters/report-parameters-with-predefined-dynamic-values.md) (load parameter values from a data source dynamically)

    ![Dynamic parameter values](../../images/eurd-web-dynamic-parameter-values.png)

Refer to the following documentation section for more details: [Create a Report Parameter](use-report-parameters/create-a-report-parameter.md).

## Reference Report Parameters

Once you [create](use-report-parameters/create-a-report-parameter.md) a parameter, you can reference it in your report’s [filter string](shape-report-data/filter-data/filter-data-at-the-report-level.md) to filter underlying report data.

![Reference parameter in report filter string](../../images/eurd-web-reference-parameter-in-report-filter-string.png)

You can also reference the parameter in a report control’s [expression](use-expressions.md) or its **Text** property.

![Reference report parameter in a control's expression](../../images/eurd-web-report-parameters-reference-in-expression.png)

When used in this manner, you can filter data displayed within an individual report control (such as [Label](use-report-elements/use-basic-report-controls/label.md)) conditionally.

You can also bind data source parameters to report parameters and filter data at the data source level. Refer to the following help topic for more information: [Reference Report Parameters](use-report-parameters/reference-report-parameters.md).

## Specify Parameter Values

Available report parameters appear within a report’s **Print Preview** window (inside the [Parameters panel](use-report-parameters/parameters-panel.md)). Use this panel to specify desired parameter values:

![Specify parameter values in the Parameters Panel](../../images/eurd-web-parameters-panel.png)

# Use Report Parameters (Old)

Report parameters pass data to a report before it is generated in **Preview**. You can specify parameter values.

The topics in this section describe how to create report parameters of different types and specify their values:

* [Create a Report Parameter](use-report-parameters/create-a-report-parameter.md)
* [Report Parameters with Predefined Static Values](use-report-parameters/report-parameters-with-predefined-static-values.md)
* [Report Parameters with Predefined Dynamic Values](use-report-parameters/report-parameters-with-predefined-dynamic-values.md)
* [Multi-Value Report Parameters](use-report-parameters/multi-value-report-parameters.md)
* [Cascading Report Parameters](use-report-parameters/cascading-report-parameters.md)
* [Date Range Report Parameters](use-report-parameters/date-range-report-parameters.md)

Use report parameters in the following cases:

* **In [Filter Strings](filter-data.md)**

    Report parameters can be referenced in a filter string.

    ![Parameter in FIlter String](../../../images/eurd-web-parameters-filter-string-with-multi-value-parameter.png)

    > [!TIP]
    > Data can be filtered:
    > * On the report level. All data is loaded from the data source before a filter is applied.
    > * On the data source level. Only the filtered data is loaded. See [Filter Data at the Data Source Level](filter-data/filter-data-at-the-data-source-level.md) for more information.

* **In [Expressions](../use-expressions.md)**

    You can create a report parameter and use it in expressions. For instance, you can do the following:

    * Specify a [calculated field](use-calculated-fields/calculated-fields-overview.md)'s value.
    * [Bind](../use-report-elements/bind-controls-to-data.md) a control to data. 
    * Conditionally change [a band's visibility](specify-conditions-for-report-elements/conditionally-change-a-bands-visibility-expression-bindings.md) or [a control's appearance](specify-conditions-for-report-elements/conditionally-change-a-control-appearance.md).
 
    ![Parameters in Expression Editor](../../../images/eurd-web-parameters-expression-editor.png)

* **In [Mail Merge](../use-report-elements/use-embedded-fields-mail-merge.md)**

    You can use a report parameter in a control's text.

    ![MailMerge Parameters](../../../images/eurd-web-mail-merge-insert-parameters.png)

* **As a Value Source for Control Parameters**

    The following controls have internal collections of parameters. You can bind these internal parameters to report parameters.

    * **[Chart](../use-report-elements/use-charts-and-pivot-grids/use-charts-in-reports.md)**

	    [Filter chart data](../use-report-elements/use-charts-and-pivot-grids/use-charts-to-visualize-grouped-data.md) by parameters.

    * **[Subreport](../use-report-elements/use-basic-report-controls/subreport.md)**

	    Use the control's parameters collection to specify parameter values in the report that the **Subreport** control references.

* **As a Value Source for Data Source Parameters**

    The following data sources have internal collections of parameters. You can bind these internal parameters to report parameters to make them dependent on an external value.

    * **[Database](../bind-to-data/bind-a-report-to-a-database.md)**

        Use [query parameters](../bind-to-data/specify-query-parameters.md) to filter data on the database level or pass values to a stored procedure.

    * **[JSON](../bind-to-data/bind-a-report-to-json-data.md)**

        Use path, query, and header parameters to configure HTTP requests to the web service endpoint.

    * **[Object](../bind-to-data/bind-a-report-to-an-object-data-source.md)**

        Use object data source parameters to pass variables to the method that fetches data.

* **Display a Report Parameter Value in a Report Explicitly**

    ![Display Parameters Explicitly](../../../images/eurd-web-parameters-for-data-binding.png)

Wherever you specify a parameter name, prefix it with the question mark character.

![Prepend Parameters with Question Mark](../../../images/eurd-web-parameters-prepend-with-question-mark.png)
