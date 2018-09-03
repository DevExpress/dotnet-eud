---
title: Use Expressions
owner: Mary Sammal
---
# Use Expressions

Expressions are used to specify criteria for [retrieving and formatting data](bind-to-data\bind-controls-to-data-expression-bindings.md), [creating calculated fields](shape-report-data\use-calculated-fields.md) and [calculating summaries](shape-report-data\shape-data-expression-bindings\calculate-a-summary.md), [conditionally shaping data and changing a report control's appearance](shape-report-data\shape-data-expression-bindings.md).

## Expression Syntax
An expression is a string that, when parsed and processed, evaluates a value. Expressions consist of field names, constants, operators, and functions. Field names must be wrapped in brackets. Here are examples of expressions:

_"[Quantity] * [UnitPrice] * (1 - [BonusAmount])"_

_"[FirstName] + ' ' + [LastName]"_

_"[Country] == 'USA'"_

_"[OrderDate] > #8/16/1994# AND [Quantity] > 20"_

There is a list of operators, constants and functions that you can use in expressions. Refer to the [Expression Syntax](use-expressions\expression-syntax.md) topic for details on their usage.

## Expression Editor
The Report Designer allows you to use the Expression Editor that provides functions, operators, data source fields, report elements, constants and variables to construct expressions.

![Expressions_ExpressionEditor](../../../images/eurd-win-expression-editor.png)

The Expression Editor supports syntax highlighting and intelligent code completion (suggesting functions and available data elements as you type).

![Expressions_ExpressionEditor_Intellisense](../../../images/eurd-win-expression-editor_intellisense.png)

The Expression Editor displays all the errors it finds in the specified expression.

![Expressions_ExpressionEditor_ErrorValidation](../../../images/eurd-win-expression-editor_error-validation.png)

## Filter Editor
The Report Designer allows you to use the Filter Editor to specify filter criteria. The Filter Editor provides a visual interface for constructing filter criteria with an unlimited number of filter conditions combined by logical operators. You can also switch to the Text mode to type a filter string manually.

![Expressions_FilterEditor](../../../images/eurd-win-filter-editor.png)

The Filter Editor supports intelligent code completion (suggesting functions and available data elements as you type) and error validation features.

![FilterEditor_New_Features](../../../images/eurd-win-filter-editor-validation.png)