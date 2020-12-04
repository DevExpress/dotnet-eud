---
title: Totals
author: Natalia Kazakova
legacyId: 17423
---
# Totals
The Grid dashboard item enables you to add a summary value (a **total**) calculated against displayed values of an individual column, and show the result under this column. Note that you can add any number of totals for each column. For example, you can obtain the number of column records, average or maximum value, etc.

![Dashboard-Grid-Totals-Main](../../../../images/img120084.png)

This topic describes how to create, edit or clear totals.

The topic consists of the following sections.
* [Totals Overview](#overview)
* [Create and Edit Totals](#create)
* [Clear Totals](#clear)

<a name="overview"/>

## Totals Overview
You can use the following summary functions when creating totals.
* **Count** - The number of records.
* **Sum** - The sum of the values.
	
	![func_sum](../../../../images/img4460.png)
* **Min** - The smallest value.
* **Max** - The largest value.
* **Average** - The average of the values.
	
	![func_average](../../../../images/img4457.png)
* **Auto** - The total is calculated using the type of [summary function](../../data-shaping/summarization.md) specified for the measure corresponding to the current Grid column. Note that in this case, the total is calculated based on values of the corresponding data field from the underlying data source. Note that the **Auto** type is not supported when the Grid is bound to the [OLAP](../../provide-data/connecting-to-olap-cubes.md) data source.

You can create totals using different sets of summary functions. This depends on the type of the data source field providing data for the target column.

| Icon | Data Source Field Type | Supported Totals |
|---|---|---|
| ![field-list-icon-boolean](../../../../images/img18791.png) | Boolean | Count |
| ![field-list-icon-byte](../../../../images/img18792.png) | Byte | Count |
| ![field-list-icon-date-time](../../../../images/img18795.png) | Date-time | Min, Max, Count |
| ![field-list-icon-number](../../../../images/img18796.png) ![UIElements_DataSourceBrowser_FieldListIconNumericFloat](../../../../images/img20881.png) | Numeric | All available types |
| ![field-list-icon-string](../../../../images/img18798.png) | String | Min, Max, Count |

> [!IMPORTANT]
> Note that the **Auto** type is available only for the [Measure](columns/measure-column.md) column.

<a name="create"/>

## Create and Edit Totals
To create a total, use the context menu of the column header. Right-click the required column header, select **Add Total** and specify the type of summary function used to calculate a total.

![Dashboard-Grid-Totals-AddTotal](../../../../images/img120080.png)

To change the total type, right-click the required total and select a new total type.

![Dashboard-Grid-Totals-ChangeTotalType](../../../../images/img120104.png)

<a name="clear"/>

## Clear Totals
You can delete one total or all the totals in a particular column.
* To delete a single total, right-click a total and select **Remove**.
	
	![Dashboard-Grid-Totals-DeleteOneTotal](../../../../images/img120107.png)
* To delete all column totals, right-click the column header and select **Clear Totals** in the invoked context menu.
	
	![Dashboard-Grid-Totals-ClearTotals](../../../../images/img120106.png)