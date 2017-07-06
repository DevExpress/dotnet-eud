---
title: Data Presentation Basics
---
# Data Presentation Basics
The **Grid** displays data in a two-dimensional table that supports four types of columns.

![Grid_ColumnTypes](../../../../images/Img19187.png)
* The **dimension column** displays values from the bound data item "as is".
* The **measure column** displays summaries calculated from data in the bound data item.
* The **delta column**, bound to two measures, calculates summaries for both measures, and displays the difference between these summaries.
* The **sparkline column** visualizes the variation of summary values over time.

## Sort Grid Rows
To sort records by a column's values and replace existing sort conditions that are applied to the current or other columns, click the target column's header until an _Up_ or _Down_ arrow icon is displayed within the header. The _Up_ and _Down_ arrows indicate ascending and descending sort orders, respectively.

![Grid_SortRows](../../../../images/Img22369.png)

To sort records by a column's values while preserving existing sort conditions, click a column header while holding the **SHIFT** key until an _Up_ or _Down_ arrow icon is displayed within the header.

![Grid_SortRows_Preserved](../../../../images/Img22371.png)

To remove sorting by a column, click a column header while holding down the **CTRL** key.

## Filter Grid Data
To filter grid data, click the filter button (the ![Grid_FilterIcon](../../../../images/Img22372.png) icon) and select the required filter value in the invoked filter dropdown list.

![Grid_FilterValues](../../../../images/Img22374.png)

Click **Custom** to construct filter criteria involving up to two conditions. This will invoke the **Custom AutoFilter** dialog, allowing you to compare a column with one or two values.

![Grid_CustomAutoFilter](../../../../images/Img22375.png)

To clear the filter applied to a specific column, invoke the filter dropdown list and click **All**.

![Grid_ClearFilter_All](../../../../images/Img22377.png)

To clear all filter criteria, click the **Close Filter** button within the Filter Panel.

![Grid_CloseFilter](../../../../images/Img22378.png)

## Tooltips
A Grid dashboard item can display a tooltip when the mouse pointer is hovered over the bar in the measure column.

![GridBar_Tooltip](../../../../images/Img23712.png)

The tooltip shows the value in the measure column as text.

When the mouse pointer is hovered over the cell in the sparkline column, the tooltip can display start/end values and minimum/maximum values.

![GridSparkline_Tooltip](../../../../images/Img23713.png)