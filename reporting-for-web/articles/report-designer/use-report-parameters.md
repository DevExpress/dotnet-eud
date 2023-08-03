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

    ![Cascading report parameters](../../images/eurd-web-cascading-parameter-result.png)

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