---
title: Interactivity
author: Natalia Kazakova
legacyId: 117978
---
# Interactivity
To enable interaction between the Chart and other dashboard items, you can use the interactivity features, as **Master Filtering** and **Drill-Down**.
* [Master Filtering](#masterfiltering)
* [Drill-Down](#drilldown)

## <a name="masterfiltering"/>Master Filtering
You can use the Chart dashboard item as a filter for other dashboard items. To learn more about filtering concepts common to all dashboard items, see the [Master Filtering](../../interactivity/master-filtering.md) topic.

The Chart supports filtering by **argument**, **series** or **points**.
* Filtering **by arguments** allows you to make other dashboard items display only data related to selected argument values by clicking series points.
	
	![wdd-chart-master-filter-arg](../../../../images/img125063.png)
* When filtering **by series** is enabled, you can click a series point to make other dashboard items display only data related to the selected series.
	
	![wdd-chart-master-filter-series](../../../../images/img125065.png)
* Filtering **by points** makes other dashboard items display only data related to the selected point.
	
	![wdd-chart-master-filter-points](../../../../images/img125064.png)

To configure filtering type, open the Chart's [Interactivity](../../ui-elements/dashboard-item-menu.md) menu and select **Arguments**, **Series** or **Points** as a target dimension.

![wdd-chart-interactivity-set-points](../../../../images/img125061.png)

To reset filtering, use the **Clear Master Filter** button (the ![wdd-master-filtering-icon](../../../../images/img125072.png) icon) in the Chart's [caption](../../dashboard-layout/dashboard-item-caption.md).

## <a name="drilldown"/>Drill-Down
The drill-down capability allows you to change the detail level of data displayed in the Chart dashboard item. To learn more about drill-down concepts common to all dashboard items, see the [Drill-Down](../../interactivity/drill-down.md) topic.

The Chart supports drill-down on **argument** or **series** values.
* To drill down on arguments, click a series point to view a detail chart for the corresponding argument value.
	
	![wdd-chart-drill-down-arguments](../../../../images/img125058.png)
	
	Drill-down on arguments requires that the Arguments section contains several data items, from the least detailed to the most detailed item.
	
	![wdd-chart-drill-down-set-arguments](../../../../images/img125076.png)
* When drill-down on series is enabled, you can click a series point to view a detail chart for the corresponding series.
	
	![wdd-chart-drill-down-series](../../../../images/img125062.png)
	
	Drill-down on series requires that the Series section contains several data items, from the least detailed to the most detailed item.
	
	![wdd-chart-drill-down-set-series](../../../../images/img125075.png)

> [!NOTE]
> In OLAP mode, you can perform drill-down for either a hierarchy data item or several dimension attributes.

To specify drill-down type, go to the Chart's [Interactivity](../../ui-elements/dashboard-item-menu.md) menu and set **Arguments** or **Series** as a target dimension.

![wdd-chart-interactivity-set-series](../../../../images/img125060.png)

To return to the previous detail level, click the **Drill Up** button (the ![wdd-drill-up-icon](../../../../images/img125074.png) icon) in the Chart's [caption](../../dashboard-layout/dashboard-item-caption.md).