---
title: Drill-Down
author: Natalia Kazakova
legacyId: 16552
---
# Drill-Down
The built-in drill-down capability allows you to change the detail level of data displayed in dashboard items on the fly. To learn more about drill-down concepts common to all dashboard items, see the [Drill-Down](../../../interactivity/drill-down.md) topic.

The Chart dashboard item supports drill down on argument or series values.

## Drill Down on an Argument
When drill down on arguments is enabled, you can click a series point to view a detail chart for the corresponding argument value.

![Chart_Interactivity_DrillDownOnArguments](../../../../../images/img21870.png)

> [!NOTE]
> When [Filtering by Arguments](master-filtering.md) is enabled, you can view the details by double-clicking a series point.

Drill down on arguments requires that the Arguments section contains several data items, from the least detailed to the most detailed item.

![Chart_Interactivity_DrillDownOnArguments_DataItems](../../../../../images/img19557.png)

> [!NOTE]
> In OLAP mode, you can perform drill-down for either a hierarchy data item or several dimension attributes.

To enable drill down on arguments, click the **Drill Down** button in the **Data** Ribbon tab (or the ![Chart_Interactivity_DrillDown_Toolbar](../../../../../images/img21873.png) button if you are using the toolbar menu)...

![Chart_Interactivity_DrillDown_Ribbon](../../../../../images/img21872.png)

...and the **Arguments** button (or the ![Chart_Interactivity_FilterByArguments_Toolbar](../../../../../images/img19511.png) button if you are using the toolbar menu).

![Chart_Interactivity_FilterByArguments_Ribbon](../../../../../images/img19310.png)

## Drill Down on a Series
When drill down on a series is enabled, you can click a series point (or corresponding legend item) to view a detail chart for the corresponding series.

![Chart_Interactivity_DrillDownOnSeries](../../../../../images/img21871.png)

> [!NOTE]
> When [Filtering by Series](master-filtering.md) is enabled, you can view the details by double-clicking a series point.

Drill down on a series requires that the Series section contains several data items, from the least detailed to the most detailed item.

![Chart_Interactivity_DrillDownOnSeries_DataItems](../../../../../images/img19556.png)

> [!NOTE]
> In OLAP mode, you can perform drill-down for either a hierarchy data item or several dimension attributes.

To enable drill down on a series, click the **Drill Down** button in the **Data** Ribbon tab (or the ![Chart_Interactivity_DrillDown_Toolbar](../../../../../images/img21873.png) button if you are using the toolbar menu)...

![Chart_Interactivity_DrillDown_Ribbon](../../../../../images/img21872.png)

...and the **Series** button (or the ![Chart_Interactivity_FilterBySeries_Toolbar](../../../../../images/img19512.png) button if you are using the toolbar menu).

![Chart_Interactivity_FilterBySeries_Ribbon](../../../../../images/img19311.png)

## Drill Up
To return to the previous detail level (drill up), use the **Drill Up** button within the Chart [caption](../../../dashboard-layout/dashboard-item-caption.md) or in the context menu.

![Chart_Interactivity_DrillUp](../../../../../images/img19460.png)