---
title: Drill-Down
author: Natalia Kazakova
legacyId: 118489
---
# Drill-Down
The built-in drill-down capability allows you to change the detail level of data displayed in dashboard items on the fly. To learn more about drill-down concepts common to all dashboard items, see the [Drill-Down](../../../interactivity/drill-down.md) topic.

When drill-down is enabled, you can click a tile to view its details.

> [!NOTE]
> When [Master Filtering](../../../interactivity/master-filtering.md) is enabled, you can view the details by double-clicking a tile.

![Treemap_DrillDown](../../../../../images/img127987.png)

Drill-down requires that the **Arguments** section contains several dimensions, from the least detailed to the most detailed dimension.

![Treemap_DrillDown_Arguments](../../../../../images/img127988.png)

> [!NOTE]
> In OLAP mode, you can perform drill-down for either a hierarchy data item or several dimension attributes.

To enable drill-down, click the **Drill Down** button in the **Data** Ribbon tab (or the ![DataShaping_Interactivity_DrillDown_Toolbar](../../../../../images/img19513.png) button if you are using the toolbar menu).

![DataShaping_Interactivity_DrillDown_Ribbon](../../../../../images/img19415.png)

To return to the previous detail level (drill up), use the **Drill Up** (![DrillDown_DrillUpArrow](../../../../../images/img18627.png)) button in the caption of the Treemap dashboard item, or the **Drill Up** command in the context menu.

> [!NOTE]
> [Grouping](../grouping.md) is not in effect when the drill-down is enabled.