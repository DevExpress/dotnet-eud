---
title: Interactivity
author: Natalia Kazakova
legacyId: 118005
---
# Interactivity
To enable interaction between the Card and other dashboard items, you can use interactivity features like **Master Filtering** and **Drill-Down**.
* [Master Filtering](#masterfiltering)
* [Drill-Down](#drilldown)

## <a name="masterfiltering"/>Master Filtering
The Dashboard allows you to use the Card dashboard item as a filter for other dashboard items. To learn more about filtering concepts common to all dashboard items, see the [Master Filtering](../../interactivity/master-filtering.md) topic.

When **Master Filtering** is enabled, you can click a card(s) to make other dashboard items only display data related to the selected card(s).

![wdd-cards-master-filtering](../../../../images/img125597.png)

To enable **Master Filtering**, go to the Card's [Interactivity](../../ui-elements/dashboard-item-menu.md) menu and select the required Master Filtering mode.

![wdd-dashboard-items-interactivity-section](../../../../images/img125270.png)

To reset filtering, use the **Clear Master Filter** button (the ![wdd-master-filtering-icon](../../../../images/img125072.png) icon) in the Card's [caption](../../dashboard-layout/dashboard-item-caption.md).

## <a name="drilldown"/>Drill-Down
The built-in drill-down capability allows you to change the detail level of data displayed in dashboard items on the fly. To learn more about drill-down concepts common to all dashboard items, see the [Drill-Down](../../interactivity/drill-down.md) topic.

When drill-down is enabled, you can click a card to view the details.

![wdd-cards-drill-down](../../../../images/img125598.png)

Drill-down requires that the Series section contains several dimensions at the top, from the least detailed to the most detailed dimension.

![wdd-cards-series-section.png](../../../../images/img125599.png)

> [!NOTE]
> In OLAP mode, you can perform drill-down for either a hierarchy data item or several dimension attributes.

To enable **Drill-Down**, go to the Card's [Interactivity](../../ui-elements/dashboard-item-menu.md) menu and turn the **Drill-Down** option on.

![wdd-dashboard-items-interactivity-section](../../../../images/img125270.png)

To return to the previous detail level, click the **Drill Up** button (the ![wdd-drill-up-icon](../../../../images/img125074.png) icon) in the Card's [caption](../../dashboard-layout/dashboard-item-caption.md).