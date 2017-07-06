---
title: Interactivity
---
# Interactivity
To enable interaction between the Grid and other dashboard items, you can use the interactivity features, as **Master Filtering** and **Drill-Down**.
* [Master Filtering](#masterfiltering)
* [Drill-Down](#drilldown)

## <a name="masterfiltering"/>Master Filtering
You can use the **Grid** dashboard item as a filter for other dashboard items. To learn more about filtering concepts common to all dashboard items, see the [Master Filtering](../../../../../dashboard-for-web/articles/web-dashboard-designer-mode/interactivity/master-filtering.md) topic.

The Grid dashboard item supports filtering by rows.

When **Master Filtering** is enabled, you can click a grid row (or multiple rows) to make other dashboard items only display data related to the selected record(s).

![WebViewer_MasterFiltering](../../../../images/Img22459.gif)

To enable **Master Filtering**, go to the Grid's [Interactivity](../../../../../dashboard-for-web/articles/web-dashboard-designer-mode/ui-elements/dashboard-item-menu.md) menu and select the required Master Filtering mode.

![wdd-dashboard-items-interactivity-section](../../../../images/Img125270.png)

To reset filtering, use the **Clear Master Filter** button (the ![wdd-master-filtering-icon](../../../../images/Img125072.png) icon) in the Grid's [caption](../../../../../dashboard-for-web/articles/web-dashboard-designer-mode/dashboard-layout/dashboard-item-caption.md).

## <a name="drilldown"/>Drill-Down
The built-in drill-down capability allows you to change the detail level of data displayed in dashboard items on the fly. To learn more about drill-down concepts common to all dashboard items, see the [Drill-Down](../../../../../dashboard-for-web/articles/web-dashboard-designer-mode/interactivity/drill-down.md) topic.

The **Grid** dashboard item supports drill-down for rows.When drill-down is enabled, you can click a grid row to view the details.

![wdd-grid-interactivity-drill-down](../../../../images/Img125412.png)

Drill-down requires that the Columns section contains several dimensions at the top, from the least detailed to the most detailed dimension.

![wdd-grid-interactivity-several-dimensions](../../../../images/Img125410.png)

> In OLAP mode, you can perform drill-down for either a hierarchy data item or several dimension attributes.

To enable **Drill-Down**, go to the Grid's [Interactivity](../../../../../dashboard-for-web/articles/web-dashboard-designer-mode/ui-elements/dashboard-item-menu.md) menu and turn the **Drill-Down** option on.

![wdd-dashboard-items-interactivity-section](../../../../images/Img125270.png)

To return to the previous detail level, click the **Drill Up** button (the ![wdd-drill-up-icon](../../../../images/Img125074.png) icon) in the Grid's [caption](../../../../../dashboard-for-web/articles/web-dashboard-designer-mode/dashboard-layout/dashboard-item-caption.md).