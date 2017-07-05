---
title: Interactivity
---
To enable interaction between the Pie and other dashboard items, you can use interactivity features like **Master Filtering** and **Drill-Down**.
* [Master Filtering](#masterfiltering)
* [Drill-Down](#drilldown)

## <a name="masterfiltering"/>Master Filtering
You can use the Pie dashboard item as a filter for other dashboard items. To learn more about filtering concepts common to all dashboard items, see the [Master Filtering](../../../../../dashboard-for-web/articles/web-dashboard-designer-mode/interactivity/master-filtering.md) topic.

The Pie dashboard item supports filtering by **arguments**, **series** or **points**.
* Filtering **by arguments** allows you to make other dashboard items display only data related to selected argument values by clicking a pie segment.
	
	![Pies_FilteringByArguments_Web](../../../../images/Img22485.png)
* When filtering **by series** is enabled, you can click a pie to make other dashboard items display only data related to the selected pie.
	
	![Pies_FilteringBySeries_Web](../../../../images/Img22486.png)
* When filtering **by points** is enabled, you can click a single pie segment to make other dashboard items display only data related to the selected segment.
	
	![wdd-pies-master-filter-points](../../../../images/Img125780.png)

To configure filtering type, open the Pie's [Interactivity](../../../../../dashboard-for-web/articles/web-dashboard-designer-mode/ui-elements/dashboard-item-menu.md) menu and select **Arguments**, **Series** or **Points** as a target dimension.

![wdd-chart-interactivity-set-points](../../../../images/Img125061.png)

To reset filtering, use the **Clear Master Filter** button (the ![wdd-master-filtering-icon](../../../../images/Img125072.png) icon) in the Pie's [caption](../../../../../dashboard-for-web/articles/web-dashboard-designer-mode/dashboard-layout/dashboard-item-caption.md).

## <a name="drilldown"/>Drill-Down
The drill-down capability allows you to change the detail level of data displayed in the Pie dashboard item. To learn more about drill-down concepts common to all dashboard items, see the [Drill-Down](../../../../../dashboard-for-web/articles/web-dashboard-designer-mode/interactivity/drill-down.md) topic.

The Pie supports drill-down on **argument** or **series** values.
* To drill down on **arguments**, click a pie segment to view a detail diagram for the corresponding argument value.
	
	![Pies_DrillDownOnArguments_Web](../../../../images/Img22487.png)
	
	Drill-down on arguments requires that the **Arguments** section contains several data items, from the least detailed to the most detailed item.
	
	![wdd-pies-interactivity-arguments](../../../../images/Img125781.png)
* When drill-down on **series** is enabled, you can click a pie chart to view a detail diagram for the corresponding series value.
	
	![Pies_DrillDownOnSeries_Web](../../../../images/Img22488.png)
	
	Drill-down on series requires that the **Series** section contains several data items, from the least detailed to the most detailed item.
	
	![wdd-pies-interactivity-series](../../../../images/Img125782.png)

> In OLAP mode, you can perform drill-down for either a hierarchy data item or several dimension attributes.

To specify drill-down type, go to the Pie's [Interactivity](../../../../../dashboard-for-web/articles/web-dashboard-designer-mode/ui-elements/dashboard-item-menu.md) menu and set **Arguments** or **Series** as the target dimension.

![wdd-chart-interactivity-set-series](../../../../images/Img125060.png)

To return to the previous detail level, click the **Drill Up** button (the ![wdd-drill-up-icon](../../../../images/Img125074.png) icon) in the Pie's [caption](../../../../../dashboard-for-web/articles/web-dashboard-designer-mode/dashboard-layout/dashboard-item-caption.md).