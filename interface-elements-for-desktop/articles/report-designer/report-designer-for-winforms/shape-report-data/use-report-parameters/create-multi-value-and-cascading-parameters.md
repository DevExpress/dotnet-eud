---
title: Create Multi-Value and Cascading Parameters
author: Anna Gubareva
---
# Create Multi-Value and Cascading Parameters

This document describes the implementation of multi-value and cascading parameters. Multi-value parameters can accept more than a single value, and cascading parameters display values corresponding to current values of other parameters.

## <a name="multivalue"></a>Multi-Value Parameters
To assign a collection of values to a parameter, enable its **Multi-Value** property. In the **Add New Parameter** dialog, this option corresponds to the **Allow multiple values** checkbox.

![](../../../../../images/eurd-win-parameters-create-multi-value-parameter.png)

Multi-value parameters are useful when you need to [filter report data](../filter-data/filter-data-at-the-report-level.md) against a list of values. The following image illustrates a correct filtering expression that incorporates a multi-value parameter. This expression is assigned to the report's **Filter String** property.

![](../../../../../images/eurd-win-parameters-filter-string-with-multi-value-parameter.png)

The following image demonstrates an editor for a multi-value parameter in a Print Preview.

![](../../../../../images/eurd-win-parameters-multi-value-parameter-result.png)

## <a name="cascading"></a>Cascading Parameters
The list of values available for a parameter in a Print Preview can be filtered based on the current value of another parameter.

To filter the list of parameter values, click the ellipsis button for the parameter's **Filter String** property in the **Add New Parameter** dialog window and specify a filter string that refers to another parameter.

![](../../../../../images/eurd-win-parameters-create-cascading-parameter.png)

Click the report's smart tag, and in the invoked actions list, click the ellipsis button for the **Filter String** property. In the invoked **FilterString Editor**, construct an expression that uses both parameters:

![](../../../../../images/eurd-win-parameters-filter-with-cascading-parameters.png)

The following image illustrates cascading parameters.

![](../../../../../images/eurd-win-parameters-cascading-result.png)