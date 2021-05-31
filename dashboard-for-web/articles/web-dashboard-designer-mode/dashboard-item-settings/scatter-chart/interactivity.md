---
title: Interactivity
author: Natalia Kazakova
legacyId: 117984
---
# Interactivity
To enable interaction between the Scatter Chart and other dashboard items, you can use the interactivity features, as **Master Filtering** and **Drill-Down**.
* [Master Filtering](#masterfiltering)
* [Drill-Down](#drilldown)

## <a name="masterfiltering"/>Master Filtering
The Web Dashboard allows you to use any data aware dashboard item as a filter for other dashboard items. To learn more about filtering concepts common to all dashboard items, see the [Master Filtering](../../interactivity/master-filtering.md) topic.

The Scatter Chart dashboard item supports filtering by points that correspond to specific argument values or their combinations.

When Master Filtering is enabled, you can click a point (or multiple points) to make other dashboard items only display data related to the selected point(s).

![wdd-grid-interactivity-master-filtering](../../../../images/img125268.png)

To enable **Master Filtering**, go to the Scatter Chart's [Interactivity](../../ui-elements/dashboard-item-menu.md) menu and select the required Master Filtering mode.

![wdd-dashboard-items-interactivity-section](../../../../images/img125270.png)

To reset filtering, use the **Clear Master Filter** button (the ![wdd-master-filtering-icon](../../../../images/img125072.png) icon) in the Scatter Chart's [caption](../../dashboard-layout/dashboard-item-caption.md).

## <a name="drilldown"/>Drill-Down
The Drill-Down feature allows you to change the detail level of data displayed in dashboard items. To learn more about concepts common to all dashboard items, see the [Drill-Down](../../interactivity/drill-down.md) topic.

When drill-down is enabled, you can click a point to view the details (or double-click a point in case of enabled Master Filtering).

![wdd-grid-interactivity-drill-down](../../../../images/img125267.png)

Drill-down requires that the **Arguments** section contains several dimensions, from the least to the most detailed dimension.

![wdd-scatter-chart-arguments-section](../../../../images/img125269.png)

> [!NOTE]
> In OLAP mode, you can perform drill-down for either a hierarchy data item or several dimension attributes.

To enable **Drill-Down**, go to the Scatter Chart's [Interactivity](../../ui-elements/dashboard-item-menu.md) menu and turn the **Drill-Down** option on.

![wdd-dashboard-items-interactivity-section](../../../../images/img125270.png)

To return to the previous detail level, click the **Drill Up** button (the ![wdd-drill-up-icon](../../../../images/img125074.png) icon) in the Scatter Chart's [caption](../../dashboard-layout/dashboard-item-caption.md).