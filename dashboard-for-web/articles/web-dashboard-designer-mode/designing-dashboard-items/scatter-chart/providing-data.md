---
title: Providing Data
---
The **Web Dashboard** allows you to bind various dashboard items to data in a virtually uniform manner. To learn more, see the [Binding Dashboard Items to Data](../../../../../dashboard-for-web/articles/web-dashboard-designer-mode/binding-dashboard-items-to-data.md) topic.

The only difference is in the data sections that the required dashboard item has. This topic describes how to bind a **Scatter Chart** dashboard item to data.

## Binding to Data in the Web Dashboard
The image below shows a sample Scatter Chart dashboard item that is bound to data.

![wdd-scatter-chart-bindings](../../../../images/Img125600.png)

To bind the Scatter Chart dashboard item to data, click a placeholder contained in one of the available data sections and select the required data source field in the **Binding** section of the invoked [data item menu](../../../../../dashboard-for-web/articles/web-dashboard-designer-mode/ui-elements/data-item-menu.md).

The table below lists and describes the Scatter Chart's data sections.

| Section | Processed as | Description |
|---|---|---|
| **X-Axis** | Measure | Contains the data item against which the X-coordinates of data points are calculated. |
| **Y-Axis** | Measure | Contains the data item against which the Y-coordinates of data points are calculated. |
| **Weight** | Measure | Contains the data item whose values are used to calculate the weight of data points. |
| **Arguments** | Dimension | Contains data items that provide scatter chart arguments used to create data points. |