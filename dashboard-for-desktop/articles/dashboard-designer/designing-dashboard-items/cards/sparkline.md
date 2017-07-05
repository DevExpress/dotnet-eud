---
title: Sparkline
---
_Sparklines_ can be used to visualize the variation of [actual or target](../../../../../dashboard-for-desktop/articles/dashboard-designer/designing-dashboard-items/cards/providing-data.md) values (for instance, over time).

![Card_StretchedLayout_Sparkline](../../../../images/Img128184.png)

To learn how to display the sparkline for different layout types, see [Layout](../../../../../dashboard-for-desktop/articles/dashboard-designer/designing-dashboard-items/cards/layout.md).
* [Data Binding Specifics](#binding)
* [Change Sparkline Options](#options)

## <a name="binding"/>Data Binding Specifics
You need to provide a date-time or numeric dimension whose data is used as argument values to display a sparkline within the card.

![Card_Sparkline_DataSections](../../../../images/Img128185.png)

If you have provided both actual and target values, a sparkline visualizes the actual value's variation.

## <a name="options"/>Change Sparkline Options
To manage sparkline settings, click the Options button (the ![DataItemsArea_OptionsButton](../../../../images/Img20167.png) icon) displayed next to the data item container. In the invoked **Card Settings** dialog, go to the **Sparkline Options** tab:

![CardSettings_SparklineOptionsTab](../../../../images/Img128295.png)

The following options are available:

| Sparkline Options | Description |
|---|---|
| Sparkline view type | Defines the sparkline’s view type. Sparkline data points can be represented as **area**, **line**, **bars**, or **win** and **loss** squares. |
| Highlight min/max points | Specifies whether to highlight the minimum/maximum points of a sparkline. |
| Highlight start/end points | Specifies whether to highlight the start/end points of a sparkline. |