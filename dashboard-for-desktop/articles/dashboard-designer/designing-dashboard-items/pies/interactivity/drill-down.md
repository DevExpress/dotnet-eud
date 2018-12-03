---
title: Drill-Down
author: Natalia Kazakova
legacyId: 16580
---
# Drill-Down
The built-in drill-down capability allows you to change the detail level of data displayed in dashboard items on the fly. To learn more about drill-down concepts common to all dashboard items, see the [Drill-Down](../../../interactivity/drill-down.md) topic.

The **Pie** dashboard item supports drill-down on **argument** or **series** values.

## Drill Down on an Argument
When drill down on an argument is enabled, you can click a pie segment to view a detail diagram for the corresponding argument value.

![Anim_Pies_DrillDownOnArguments](../../../../../images/img19909.png)

> [!NOTE]
> When [Filtering by Arguments](master-filtering.md) is enabled, you can view the details by double-clicking a pie segment.

Drill down on an argument requires that the Arguments section contains several data items, from the least detailed to the most detailed item.

![Pies_Interactivity_DrillDown_Arguments_DataItems](../../../../../images/img19972.png)

> [!NOTE]
> In OLAP mode, you can perform drill-down for either a hierarchy data item or several dimension attributes.

To enable drill down on an argument, click the **Drill Down** button in the **Data** Ribbon tab (or the ![Chart_Interactivity_DrillDown_Toolbar](../../../../../images/img21873.png) button if you are using the toolbar menu)...

![Chart_Interactivity_DrillDown_Ribbon](../../../../../images/img21872.png)

...and the **Arguments** button (or the ![Pies_Interactivity_MasterFilter_Arguments_Toolbar](../../../../../images/img19919.png) button if you are using the toolbar menu).

![Pies_Interactivity_MasterFilter_Arguments_Ribbon](../../../../../images/img19915.png)

## Drill Down on a Series
When drill down on a series is enabled, you can click a pie chart to view a detail diagram for the corresponding series value.

![Anim_Pies_DrillDownOnSeries](../../../../../images/img19910.png)

> [!NOTE]
> When [Filtering by Series](master-filtering.md) is enabled, you can view the details by double-clicking a pie chart.

Drill down on a series requires that the Series section contains several data items, from the least detailed to the most detailed item.

![Pies_Interactivity_DrillDown_Series_DataItems](../../../../../images/img19973.png)

> [!NOTE]
> In **OLAP** mode, you can perform drill-down for either a hierarchy data item or several dimension attributes.

To enable drill down on a series, click the **Drill Down** button in the **Data** Ribbon tab (or the ![Chart_Interactivity_DrillDown_Toolbar](../../../../../images/img21873.png) button if you are using the toolbar menu)...

![Chart_Interactivity_DrillDown_Ribbon](../../../../../images/img21872.png)

...and the **Series** button (or the ![Pies_Interactivity_MasterFilter_Series_Toolbar](../../../../../images/img19920.png) button if you are using the toolbar menu).

![Pies_Interactivity_MasterFilter_Series_Ribbon](../../../../../images/img19916.png)

## Drill Up
To return to the previous detail level (drill up), use the **Drill Up** button (the ![DrillDown_DrillUpArrow](../../../../../images/img18627.png) icon) in the [caption](../../../dashboard-layout/dashboard-item-caption.md) area of the Pie dashboard item, or the **Drill Up** command in the context menu.