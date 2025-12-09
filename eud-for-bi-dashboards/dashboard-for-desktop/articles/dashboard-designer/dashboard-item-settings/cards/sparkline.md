---
title: Sparkline
author: Natalia Kazakova
legacyId: 16588
---
# Sparkline
_Sparklines_ can be used to visualize the variation of [actual or target](providing-data.md) values (for instance, over time).

![Card_StretchedLayout_Sparkline](../../../../images/img128184.png)

To learn how to display the sparkline for different layout types, see [Layout](layout.md).
* [Data Binding Specifics](#binding)
* [Change Sparkline Options](#options)

## <a name="binding"/>Data Binding Specifics
You need to provide a date-time or numeric dimension whose data is used as argument values to display a sparkline within the card.

![Card_Sparkline_DataSections](../../../../images/img128185.png)

If you have provided both actual and target values, a sparkline visualizes the actual value's variation.

## <a name="options"/>Change Sparkline Options
To manage sparkline settings, click the Options button (the ![DataItemsArea_OptionsButton](../../../../images/img20167.png) icon) displayed next to the data item container. In the invoked **Card Settings** dialog, go to the **Sparkline Options** tab:

![CardSettings_SparklineOptionsTab](../../../../images/img128295.png)

The following options are available:

| Sparkline Options | Description |
|---|---|
| Sparkline view type | Defines the sparkline’s view type. Sparkline data points can be represented as **area**, **line**, **bars**, or **win** and **loss** squares. |
| Highlight min/max points | Specifies whether to highlight the minimum/maximum points of a sparkline. |
| Highlight start/end points | Specifies whether to highlight the start/end points of a sparkline. |