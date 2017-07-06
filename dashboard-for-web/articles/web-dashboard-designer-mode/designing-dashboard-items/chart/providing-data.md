---
title: Providing Data
---
# Providing Data
The **Web Dashboard** allows you to bind various dashboard items to data in a virtually uniform manner. To learn more, see the [Binding Dashboard Items to Data](../../../../../dashboard-for-web/articles/web-dashboard-designer-mode/binding-dashboard-items-to-data.md) topic.

The only difference is in the data sections that the required dashboard item has. This topic describes how to bind a **Chart** dashboard item to data.

## Binding to Data in the Web Dashboard
The image below shows a sample Chart dashboard item that is bound to data.

![wdd-chart-binding](../../../../images/Img125010.png)

To bind the Chart dashboard item to data, click a placeholder contained in one of the available data sections and select the required data source field in the **Binding** section of the invoked [data item menu](../../../../../dashboard-for-web/articles/web-dashboard-designer-mode/ui-elements/data-item-menu.md).

The table below lists and describes the Chart's data sections.

| Section | Processed as | Description |
|---|---|---|
| **Values** | Measure | Contains data items against which the Y-coordinates of data points are calculated. The data item menu allows you to select the series type and specify different options. Note that some types of series accept several measures. To learn more, see the documentation for the required [series type](../../../../../dashboard-for-web/articles/web-dashboard-designer-mode/designing-dashboard-items/chart/series.md). |
| **Arguments** | Dimension | Contains data items that provide values displayed along the X-axis of the chart. |
| **Series** | Dimension | Contains data items whose values are used to create chart series. |