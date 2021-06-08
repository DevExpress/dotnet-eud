---
title: Bind Dashboard Items to Data in OLAP Mode
author: Natalia Kazakova
legacyId: 117958
---
# Bind Dashboard Items to Data in OLAP Mode
In OLAP mode, the cube schema is fetched automatically, and the **Data Sources** page of the [dashboard menu](../ui-elements/dashboard-menu.md) displays the entire OLAP cube structure.

![wdd-data-sources-page-olap](../../../images/img126320.png)

To visualize data, open the dashboard item's **Bindings** menu, click a placeholder and choose the required measure, attribute or hierarchy in the invoked list of data source's available fields, as described in the [Bind Dashboard Items to Data](bind-dashboard-items-to-data-in-the-web-dashboard.md) topic. Note that OLAP measures can only be placed in the Values section, while dimension attributes and hierarchies can be placed within other data sections.

> [!NOTE]
> By default, the dashboard displays only dimension values that have intersections with measures in a cube. To show all available dimension values, add [hidden measures](hidden-data-items.md) to the dashboard item so that all dimension values of the dimension will have not be empty for at least one measure value of these measures.

OLAP hierarchies allow you to customize each of their levels separately. Select the desired level in the dashboard item's [Bindings](../ui-elements/dashboard-item-menu.md) menu to invoke the [data item menu](../ui-elements/data-item-menu.md) to access hierarchy level options.

![wdd-olap-hierarchy-data-item-options](../../../images/img126318.png)

> [!NOTE]
> You can easily drill down through OLAP hierarchies using the [Drill-Down](../interactivity/drill-down.md) feature.