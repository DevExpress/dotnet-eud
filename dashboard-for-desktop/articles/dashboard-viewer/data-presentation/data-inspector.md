---
title: Data Inspector
author: Margarita Zakhodyaeva
---
# Data Inspector
**Data Inspector** is a dialog window that contains two grids that display raw and aggregated data. You can switch from one grid to another with the radio group located at the window top. 

Aggregated Data:

![](../../../images/data-inspector-aggr.png)

Raw Data:

![](../../../images/data-inspector-raw.png)


## Overview

To invoke the Data Inspector window, click the "Inspect Data" button ![](../../../images/inspect-data-winforms.png) in the [dashboard item caption](../../dashboard-designer/dashboard-layout/dashboard-item-caption.md) or select the "Inspect Data" context menu item. 

The "Inspect Data" button and menu item are initially hidden. You can inspect the raw or / and aggregated data depending on the Dashboard Designer configuration.

## Aggregated (Displayed) Data

The data shown as _Aggregated_ is retrieved from the dashboard item's data storage.
The columns are:

* [Dimensions](../../dashboard-designer/designing-dashboard-items/grid/columns/dimension-column.md), except the **Sparkline**.
* [Measures](../../dashboard-designer/designing-dashboard-items/grid/columns/measure-column.md). A list of dimensions does not include unbound measures (the measures without a DataMember, such as [Totals](../../dashboard-designer/designing-dashboard-items/grid/totals.md) and the number of points in a [Cluster](../../dashboard-designer/designing-dashboard-items/geo-point-maps/clustering.md).
 * The [Sparkline](../../dashboard-designer/designing-dashboard-items/grid/columns/sparkline-column.md) is displayed as a column.

## Raw Data

Raw data is the dashboard item's underlying data. 