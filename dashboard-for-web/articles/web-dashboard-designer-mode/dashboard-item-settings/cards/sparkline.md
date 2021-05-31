---
title: Sparkline
author: Natalia Kazakova
legacyId: 118004
---
# Sparkline
_Sparklines_ can be used to visualize the variation of [actual or target](providing-data.md) values (for instance, over time).

![wdd-cards-sparkline](../../../../images/img125308.png)

To learn how to display the sparkline for different layout types, see [Layout](layout.md).
* [Data Binding Specifics](#binding)
* [Change Sparkline Options](#options)

## <a name="binding"/>Data Binding Specifics
You need to provide a date-time or numeric dimension (in the **[Sparkline](providing-data.md)** section) whose data is used as argument values to display a sparkline within the card.

![Card_BindingMenu_SparklineArgument](../../../../images/img128476.png)

If you have provided both actual and target values, a sparkline visualizes the actual value's variation.

## <a name="options"/>Change Sparkline Options
To change sparkline settings in the Web Dashboard's UI, invoke the **[Binding menu](../../ui-elements/dashboard-item-menu.md)**, click the required data item in the **[Cards](providing-data.md)** section and go to **Sparkline Options** in the [data item's menu](../../ui-elements/data-item-menu.md).
The following options are available:

| Sparkline Options | Description |
|---|---|
| View type | Defines the sparkline’s view type. Sparkline data points can be represented as **area**, **line**, **bars**, or **win** and **loss** squares. |
| Highlight min/max points | Specifies whether to highlight the minimum/maximum points of a sparkline. |
| Highlight start/end points | Specifies whether to highlight the start/end points of a sparkline. |