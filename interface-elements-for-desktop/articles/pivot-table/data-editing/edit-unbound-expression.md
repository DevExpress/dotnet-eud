---
title: Edit Unbound Expression
author: Natalia Kazakova
legacyId: 114400
---
# Edit Unbound Expression
To edit the unbound field's expression, use the [Expression Editor](../../expression-editor.md). Select the **Expression Editor** menu command to invoke it. 

Expressions allow you to calculate values based on values of other fields. 

![_EU_ExpressionEditorInvoking](../../../images/img118797.png)

An expression is a string that, when parsed and processed, evaluates a value. Expressions consist of field names, constants, operators, and functions. Field names must be wrapped in brackets. Here are examples of expressions:

_"[Quantity] * [UnitPrice] * (1 - [BonusAmount])"_

_"[FirstName] + ' ' + [LastName]"_

_"[Country] == 'USA'"_

_"[OrderDate] > #8/16/1994# AND [Quantity] > 20"_

For more information about syntax you can use in expressions, see [Pivot Grid Expression Syntax](pivot-grid-expression-syntax.md).