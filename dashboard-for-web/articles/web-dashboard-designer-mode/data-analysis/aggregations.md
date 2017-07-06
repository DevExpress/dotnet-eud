---
title: Aggregations
---
# Aggregations
The Web Dashboard allows you to prepare underlying data using additional aggregation levels when creating [calculated fields](../../../../dashboard-for-web/articles/web-dashboard-designer-mode/providing-data/calculated-fields.md). This topic shows how to evaluate calculated fields on a visualization (summary) and intermediate levels.

## Summary Level Aggregations
To compute values of the calculated field on a visualization (or summary) level, you can use a set of predefined aggregate functions. In the [Expression Editor](../../../../dashboard-for-web/articles/web-dashboard-designer-mode/providing-data/calculated-fields.md), these functions are available within the **Functions** | **Aggregate**.

| Function | Description |
|---|---|
| Aggr(SummaryExpression, Dimensions) | Aggregates underlying data using the detail level specified by a predefined set of dimensions and a specified summary function. |
| Avg(Value) | Returns the average of all the values in the expression. |
| Count() | Returns the number of values. |
| CountDistinct(Value) | Returns the number of distinct values. |
| Max(Value) | Returns the maximum value across all records. |
| Min(Value) | Returns the minimum value across all records. |
| Median(Value) | Returns the median of the values. |
| Sum(Value) | Returns the sum of all values. |
| Var(Value) | Returns an estimate of the variance of a population where the sample is a subset of the entire population. |
| Varp(Value) | Returns the variance of a population where the population is the entire data to be summarized. |
| StdDev(Value) | Returns an estimate of the standard deviation of a population, where the sample is a subset of the entire population. |
| StdDevp(Value) | Returns the standard deviation of a population where the population is the entire data to be summarized. |

These functions can be used for all types of numeric fields. After creating such calculated fields, you can use them as measures contained in an OLAP cube.

## Intermediate Level Aggregations
The Web Dashboard can aggregate and summarize data on different levels.
* The [Query Builder](../../../../dashboard-for-web/articles/web-dashboard-designer-mode/providing-data/working-with-sql-data-sources/query-builder.md) allows you to prepare an underlying data source before analyzing data. You can apply grouping, sorting, summarization and other data shaping operations during data selection.
* [Dashboard items](../../../../dashboard-for-web/articles/web-dashboard-designer-mode/designing-dashboard-items.md) aggregate and summarize data at a visualization level using dimensions and measures, respectively. To learn more, see [Binding Dashboard Items to Data](../../../../dashboard-for-web/articles/web-dashboard-designer-mode/binding-dashboard-items-to-data.md).
* The **Aggr** function introduces an intermediate detail level that is not related to the visualization level. This allows you to create custom aggregations at different levels and combine these aggregations with existing visualizations.