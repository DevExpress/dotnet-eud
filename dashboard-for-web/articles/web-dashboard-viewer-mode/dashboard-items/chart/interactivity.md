---
title: Interactivity
author: Andrey Aksenov
legacyId: 16731
---
# Interactivity
This topic describes features that enable interaction between the **Chart** and other dashboard items. These features include **Master Filtering** and **Drill-Down**.

## Master Filtering
The Web Dashboard allows you to use any data aware dashboard item as a filter for other dashboard items (**Master Filter**). To learn more about filtering concepts common to all dashboard items, see the [Master Filtering](../../data-presentation/master-filtering.md) topic.

The Chart dashboard item supports filtering by **argument** or **series** values.
* **Filtering by Arguments**
	
	When filtering by arguments is enabled, you can click series points to make other dashboard items display only data related to selected argument values.
	
	![Chart_FilterByArguments_Web](../../../../images/img22475.png)
* **Filtering by Series**
	
	When filtering by series is enabled, you can click a series point to make other dashboard items display only data related to the selected series.
	
	![Chart_FilterBySeries_Web](../../../../images/img22476.png)

To clear the selection in the Master Filter item, use the **Clear Master Filter** button (the ![WebViewer_ClearMasterFilterIcon](../../../../images/img22461.png) icon) in the chart's [caption](../../data-presentation/dashboard-layout.md) area.

## Drill-Down
The built-in drill-down capability allows you to change the detail level of data displayed in dashboard items on the fly. To learn more, see [Drill-Down](../../data-presentation/drill-down.md).

The Chart dashboard item supports drill-down on argument or series values.
* **Drill Down on Arguments**
	
	When drill-down on arguments is enabled, you can click a series point to view a detail chart for the corresponding argument value.
	
	![Chart_DrillDownOnArguments_Web](../../../../images/img22477.png)
	
	> [!NOTE]
	> When **Filtering by Arguments** is enabled, you can view the details by clicking a selected series point.
* **Drill-Down on a Series**
	
	When drill-down on a series is enabled, you can click a series point (or corresponding legend item) to view a detail chart for the corresponding series.
	
	![Chart_DrillDownOnSeries_Web](../../../../images/img22478.png)
	
	> [!NOTE]
	> When **Filtering by Series** is enabled, you can view the details by clicking a selected series point.

To return to the previous detail level (drill up), use the **Drill Up** button (the ![WebViewer_DrillUpIcon](../../../../images/img22464.png) icon) in the chart's [caption](../../data-presentation/dashboard-layout.md).