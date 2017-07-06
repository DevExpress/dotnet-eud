---
title: Expression Editor
---
# Expression Editor
The **Expression Editor** provides the capability for constructing expressions in the [Web Report Designer](../../../../interface-elements-for-web/articles/report-designer.md).

This topic consists of the following section.
* [Expression Editor Overview](#overview)
* [Expression Syntax](#syntax)
* [Using the Expression Editor](#using)

## <a name="overview"/>Expression Editor Overview
The Expression Editor's visual interface allows you to type an expression manually or select predefined functions, operators and operands. The editor supports a variety of aggregate, date-time, logical, math and string functions. You can also use logical and arithmetic operators and fields of a data source to which a report is bound.

![expression-editor-calc-field-1](../../../images/Img118342.png)

After you finish constructing an expression, click **Save**. If an expression contains any errors, the ![expression-editor-error-icon](../../../images/Img118339.png) icon appears meaning that the expression should be rewritten.

## <a name="syntax"/>Expression Syntax
The following syntax conventions should be taken into account when using the Expression editor.
* A data field is referenced in the expression by enclosing its name in square brackets (e.g., **[ProductName]**).
* Report parameters are inserted using the "Parameters." prefix before their names (e.g., **[Parameters.parameter1]**).
* String values are denoted with apostrophes. To embed an apostrophe into an expression's text, type a double apostrophe (e.g., **'It''s sample text'**).
* Date-time constants should be enclosed with hashtags (e.g., **[OrderDate] >= #1/1/2016#**).
* To specify a null reference (one that does not refer to any object), use a question mark (e.g., **[Region] != ?**).
* If an expression involves the use of different types, you can convert them to the same type using dedicated functions (e.g., **Max(ToDecimal([Quantity]),[UnitPrice])**).

## <a name="using"/>Using the Expression Editor
Expressions can be used for calculating [query parameters](../../../../interface-elements-for-web/articles/report-designer/creating-reports/providing-data/query-parameters.md) and [calculated fields](../../../../interface-elements-for-web/articles/report-designer/creating-reports/providing-data/calculated-fields.md) values as well as for specifying conditions of [formatting rules](../../../../interface-elements-for-web/articles/report-designer/creating-reports/appearance-customization/conditionally-change-a-control's-appearance.md).
* To edit an expression for a calculated field, access its settings in the [Field List](../../../../interface-elements-for-web/articles/report-designer/interface-elements/field-list.md) and click the ellipsis button for the **Expression** property.
	
	![expression-editor-calc-field-0](../../../images/Img118338.png)
* To specify an expression for a query parameter, in the [Configure Query Parameters](../../../../interface-elements-for-web/articles/report-designer/wizards/sql-data-source-wizard/adding-a-new-data-source/configure-query-parameters.md) wizard page, set the parameter type to **Expression** and click the ellipsis button for the **Value** property.
	
	![web-designer-report-wizard-04-configure-parameters-expression](../../../images/Img125713.png)
* To construct a condition for a formatting rule, access its settings in the **Properties** panel and click the ellipsis button for the **Condition** property.
	
	![expression-editor-formatting-rules-0](../../../images/Img118337.png)
	
	If the specified expression does not return a **Boolean** value, the error ![expression-editor-error-icon](../../../images/Img118339.png) icon appears on an attempt to save the condition.