---
title: Converting Dashboard Items
author: Andrey Aksenov
legacyId: 16809
---
# Converting Dashboard Items
The Dashboard Designer provides the capability to convert data-bound dashboard items to another type. To convert the selected dashboard item to another type, use the **Convert** button in the ribbon's **Home** tab or the corresponding command in the item's context menu.

![Ribbon_ConvertDashboardItem](../../images/img23151.png)

The Dashboard Designer always preserves the following settings for data-bound dashboard items.
* The set of [data items](binding-dashboard-items-to-data.md) used to bind the dashboard item to data.
* [Data shaping](data-shaping.md) settings of data items and their names.
* A custom name displayed within the dashboard item [caption](dashboard-layout/dashboard-item-caption.md).

The following settings are kept if the dashboard item is being converted to an item that also supports this feature.
* [Master Filtering](interactivity/master-filtering.md) settings (e.g., the specified master filter mode) and [Drill-Down](interactivity/drill-down.md) settings (e.g., the target dimension).
* [Conditional Formatting](appearance-customization/conditional-formatting.md) settings.
* [Coloring](appearance-customization/coloring.md) settings.
* [Calculation](data-analysis/window-calculations.md) settings.

For different types of dashboard items, some specific settings can be preserved. For example, the following settings are preserved.
* Legend settings for the [Chart](designing-dashboard-items/chart.md)/[Scatter Chart](designing-dashboard-items/scatter-chart.md) dashboard items.
* Series types for the [Chart](designing-dashboard-items/chart.md)/[Range Filter](designing-dashboard-items/range-filter.md) dashboard items.
* Element arrangement settings for the [Pie](designing-dashboard-items/pies.md)/[Card](designing-dashboard-items/cards.md)/[Gauge](designing-dashboard-items/gauges.md) dashboard items.
* Caption settings for the [Pie](designing-dashboard-items/pies.md)/[Gauge](designing-dashboard-items/gauges.md) dashboard items.
* Navigation settings for [Choropleth Map](designing-dashboard-items/choropleth-map.md)/[Geo Point Maps](designing-dashboard-items/geo-point-maps.md).
* The attribute whose values are displayed within shape titles for [Choropleth Map](designing-dashboard-items/choropleth-map.md)/[Geo Point Maps](designing-dashboard-items/geo-point-maps.md).
* Legend settings for the [Choropleth Map](designing-dashboard-items/choropleth-map.md)/[Geo Point Maps](designing-dashboard-items/geo-point-maps.md).
* [Clustering](designing-dashboard-items/geo-point-maps/clustering.md) settings for [Geo Point Maps](designing-dashboard-items/geo-point-maps.md).