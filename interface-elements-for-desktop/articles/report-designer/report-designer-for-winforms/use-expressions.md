---
title: Use Expressions
owner: Mary Sammal
---
# Use Expressions

Expressions specify criteria used to [retrieve and format data](bind-to-data\bind-controls-to-data-expression-bindings.md), [create calculated fields](shape-report-data\use-calculated-fields.md) and [calculate summaries](shape-report-data\shape-data-expression-bindings\calculate-a-summary.md), [conditionally shape data and change a report control's appearance](shape-report-data\shape-data-expression-bindings.md).

## Expression Syntax

An expression is a string that, when parsed and processed, evaluates a value. Expressions consist of field names, constants, operators, and functions. Field names are wrapped in square brackets. Here are examples of expressions:

_"[Quantity] * [UnitPrice] * (1 - [BonusAmount])"_

_"[FirstName] + ' ' + [LastName]"_

_"[Country] == 'USA'"_

_"[OrderDate] > #8/16/1994# AND [Quantity] > 20"_

You can use [Expression Operators, Functions and Constants](use-expressions\expression-syntax.md) in your expressions.

## Expression Editor

The Report Designer allows you to use the Expression Editor that provides functions, operators, data source fields, report elements, constants and variables to construct expressions.

![Expressions_ExpressionEditor](../../../images/eurd-win-expression-editor.png)

The Expression Editor highlights an expression's syntax and supports intelligent code completion. The Editor suggests functions and available data elements as you type.

![Expressions_ExpressionEditor_Intellisense](../../../images/eurd-win-expression-editor_intellisense.png)

The Expression Editor displays all the errors it finds in the specified expression.

![Expressions_ExpressionEditor_ErrorValidation](../../../images/eurd-win-expression-editor_error-validation.png)

## Filter Editor

The Report Designer allows you to use the FilterString Editor to specify filter criteria. The FilterString Editor provides a visual interface where you can use an unlimited number of conditions and combine them with logical operators to create filter criteria. You can also switch to the Text mode and type a filter string.

![Expressions_FilterEditor](../../../images/eurd-win-filter-editor.png)

The FilterString Editor supports intelligent code completion. It suggests functions and available data elements as you type, validates the typed string and highlights errors.

![FilterEditor_New_Features](../../../images/eurd-win-filter-editor-validation.png)