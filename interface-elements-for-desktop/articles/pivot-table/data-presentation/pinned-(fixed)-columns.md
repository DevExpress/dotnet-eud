---
title: Pinned (Fixed) Columns 
author: Margarita Zakhodyaeva
---

# Pinned (Fixed) Columns

The Pivot Grid Control allows you to pin columns to the left or rightmost edge. The pinned columns are never scrolled horizontally, so you can use them as a reference point for adjacent cell values. 

 ![](../../../images/win-pivot-fixed-pinned-columns.png)

 To pin or unpin a column, right-click the column's header and select the corresponding command:

 ![](../../../images/win-pivot-fixed-columns-pin-column.png)  

## Limitations
Fixed columns have the following limitations:
* You cannot pin [custom totals](https://docs.devexpress.com/WindowsForms/DevExpress.XtraPivotGrid.PivotGridCustomTotalCollection).
* In [Legacy and Legacy-optimized](https://docs.devexpress.com/CoreLibraries/401531/devexpress-pivot-grid-core-library/data-processing-engines/legacy-and-legacy-optimized-calculation-engines) mode, the values in the pinned column are not displayed if you [collapse](https://docs.devexpress.com/WindowsForms/1940/controls-and-libraries/pivot-grid/end-user-capabilities/expanding-and-collapsing-grouping-columns-and-rows) the corresponding column in the scrollable area.