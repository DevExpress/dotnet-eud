---
title: 'How to: Use Expressions'
owner: Sergey Andreev
---
# How to: Use Expressions

This topic lists solutions to common [expression](expressions-overview.md)-related tasks.

## Group Clauses with Brackets

Use square brackets to specify a condition under which the expression should return the result.

For instance, the following expression returns all Customers that have an account Date of 8/25/2006 and an account Amount of 100:

`[Accounts][[Date] == #8/25/2006#] && [Accounts][[Amount] == 100]`

Construct an expression as in the following example to search for all Customers that have an Account with both a Date of 8/25/2006 and an Amount of 100:

`[Accounts][[Date] == #8/25/2006# && [Amount] == 100]`

## Calculate Group Summaries

Use the ^ operator to specify an expression that calculates a group summary.

* Sum up the **EFC** field values in a group:

  `[][[GroupFieldName] == [^.GroupFieldName]].Sum([EFC])`

* Specify the group header value:

  `[][[CategoryID] == [^.CategoryID] and [ProductID] == [][[CategoryID] == [^.CategoryID]].Max([ProductID])].Max([ProductName])`

* Count the number of times a value occurs:

  The following expression counts how many times the value _12_ occurs in the data source:

  `[][[FootSize]='12'].Count()`

  The following expression counts the number of records with non-zero values:

  `[][[FootSize]!=0].Avg([FootSize])`

## Reference Report Items

A report's elements are displayed in the Report Designer's Report Explorer. You can access these elements and their properties in an expression. The following example demonstrates how to set a label's BackColor property to another label's BackColor property value:

`[ReportItems].[xrLabel2].[BackColor]`

> [!Note]
> * **[ReportItems]** is a plain list that provides access to all report items at one level.
> * You cannot use the ReportItems collection in a [Calculated Field](../shape-report-data/use-calculated-fields.md)'s expression.

## Specify Images for Picture Boxes

When you specify an expression for the [Picture Box](../use-report-elements/use-basic-report-controls/picture-box.md)'s **Image Source** property, you can use image **Id**s  from the report's **ImageResources** collection.

*IIf([MarchSales]>20, [Images.ArrowUp],[Images.ArrowDown])*

## Use Row/Column Indexes for Cross Tab Cells

Use the following variables to change a Cross Tab cell's appearance settings:

* Arguments.GroupColumnIndex  
  Returns the index of a cell's column within a group.
  ```
  iif([Arguments.GroupColumnIndex] % 2 == 1, Rgb(235, 241, 252), ?)
  /*
  Result: The specified color applies an odd-even color style to the Cross Tab's columns.
  */
  ```

* Arguments.GroupRowIndex  
  Returns the index of a cell's row within a group.
  ```
  iif([Arguments.GroupRowIndex] % 2 == 1, Rgb(235, 241, 252), ?)
  /*
  Result: The specified color applies an odd-even color style to cross tab rows.
  */
  ```

## Use Variables for Event-Related Expressions

* DataSource.RowCount  
  Returns the total amount of data rows in a data source.
  ```
  [DataSource.RowCount] != 0
  /*
  Result: When this expression is applied to a control's Visible property, the control is hidden if the data source contains no data.
  */
  ```

* DataSource.CurrentRowIndex  
  Returns an index of the current data row in a data source.
  ```
  Iif([DataSource.CurrentRowIndex] % 2 = 0, 'red', 'green')
  /*
  Result: When this expression is used for a table row's BackColor property, odd rows are colored in red, even rows are colored in green.
  */
  ```

* DataSource.CurrentRowHierarchyLevel  
  Returns a zero-based level of the current row in a [hierarchical report](../create-reports/hierarchical-reports.md).
  ```
  Iif([DataSource.CurrentRowHierarchyLevel] == 0, Rgb(231,235,244), ?)
  /*
  Result: When this expression is used for the BackColor property of the Detail band that is printed in tree mode, the root level rows are highlighted.
  */
  ```

> [!Note]
> These variables are not valid when the report includes a [table of contents](../use-report-elements/use-basic-report-controls/table-of-contents.md).

## Specify Parent Relations

Use the '^' parent relation operator to refer to a parent in expressions that are written in the context of a child. You can apply this operator successively to span multi-level parent relationships.

You can use this operator to refer to the currently processed report group. This allows you to calculate aggregates within groups, as shown in the following expression:

`[][[^.CategoryID] == [CategoryID]].Sum([UnitPrice])`

## Test Collection Elements

Use brackets to check if a collection contains an element that meets a condition. The following expression returns _true_ if the Accounts collection contains at least one element that meets the _[Amount] == 100_ condition:

`[Accounts][[Amount] == 100]`

The following expression returns _false_ if the Accounts collection is empty:

`[Accounts][]`

Refer to the following topic for an example on how to use this syntax: [Calculate an Aggregate Function](../shape-report-data/use-calculated-fields/calculate-an-aggregate-function.md).