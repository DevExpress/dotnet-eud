---
title: X-Axis
author: Andrey Aksenov
legacyId: 16557
---
# X-Axis
The **X-axis** is the axis of arguments.

![Chart_XAxis](../../../../../images/img19404.png)

This topic consists of the following sections.
* [General X-Axis Settings](#generalsettings)
* [Continuous and Discrete X-Axes](#continuousanddiscretexaxes)

## <a name="generalsettings"/>General X-Axis Settings
To access X-axis settings, use the **X-Axis Settings** button in the **Diagram** section of the **Design** Ribbon tab.

![Chart_XAxisOptions_Button](../../../../../images/img19467.png)

This will invoke the **X-Axis Settings** dialog.

![Chart_XAxisOptions_Form](../../../../../images/img19403.png)

This dialog contains the following settings.

| Setting | Description |
|---|---|
| **Reverse** | Allows you to reverse the X-axis. If the X-axis is reversed, its values are ordered from right to left. |
| **Show X-axis** | Allows you to hide and show the X-axis. |
| **Show title** | Allows you to hide and show the X-axis title. You can choose whether to use the default text or specify a custom string. |
| **Enable zooming** | Allows you to enable zooming for the X-axis. The X-axis' scroll bar provides the capability to perform navigation in the zoomed diagram. |
| **Limit visible points** | Allows you to limit the number of points displayed on the chart's diagram along the X-axis. The X-axis' scroll bar provides the capability to perform navigation if the number of all points exceeds the number of visible points. |

## <a name="continuousanddiscretexaxes"/>Continuous and Discrete X-Axes
If the dimension in the Arguments section contains numeric data, the Chart can create either a continuous X-axis or a discrete X-axis.

| Continuous X-axis | Discrete X-axis |
|---|---|
| If a continuous axis is used, the distance between argument values is proportional to their values. | On a discrete axis, all argument values are an equal distance from each other. |
| ![Chart_NumericAxis_Continuous](../../../../../images/img18302.png) | ![Chart_NumericAxis_Discrete](../../../../../images/img18303.png) |

To specify the X-axis type in the Designer, invoke the data item menu for the argument dimension and select the axis type.

![Chart_Layout_XAxis_ContinuousDiscrete](../../../../../images/img19550.png)

> Note that the continuous X-axis is not supported in [OLAP](../../../binding-dashboard-items-to-data/binding-dashboard-items-to-data-in-olap-mode.md) mode.