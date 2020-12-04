---
title: Data Inspector
author: Margarita Zakhodyaeva
---
# Data Inspector
**Data Inspector** is a dialog window that displays raw or aggregated data.

## Overview

To invoke the Data Inspector window, click the "Inspect Data" button ![](../../../images/inspect-data-web.png) in the [dashboard item caption](../dashboard-layout/dashboard-item-caption.md) or select the "Inspect Data" context menu item.

## Aggregated (Displayed) Data

The data shown as _Aggregated_ is retrieved from the dashboard item's data storage.

![](../../../images/data-inspector-aggr.png)

The columns are:

* [Dimensions](../dashboard-item-settings/grid/columns.md), except the **Sparkline**.
* [Measures](../dashboard-item-settings/grid/columns.md). A list of dimensions does not include unbound measures (the measures without a DataMember, such as [Totals](../dashboard-item-settings/grid/totals.md) and the number of points in a [Cluster](../dashboard-item-settings/geo-point-maps/clustering.md).
 * The [Sparkline](../dashboard-item-settings/grid/columns.md) is displayed as a column.

## Raw Data

Raw data is the dashboard item's underlying data. 

![](../../../images/data-inspector-raw.png)