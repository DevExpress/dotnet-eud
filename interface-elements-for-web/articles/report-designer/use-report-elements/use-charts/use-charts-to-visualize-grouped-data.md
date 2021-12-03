---
title: Use Charts to Visualize Grouped Data
author: Anna Vekhina
---
# Use Charts to Visualize Grouped Data

This topic describes how to use charts to visualize grouped data in a report.

![](../../../../images/eurd-web-chart-in-group-footer.png)

In this tutorial, the report data is grouped against a data field (the report's group field). A chart is placed in the Group Footer band and is not bound to data. The report's data source is used to populate the chart with data.

![](../../../../images/eurd-web-chart-group-footer-report-layout.png)

Follow the steps below to make each chart instance display data for its group.

1. Create a chart parameter to pass a group value from the report's group field to the chart.

	Select the chart and expand the **Data** group in the **Properties** panel. Click the plus button next to the **Parameters** property.

	![](../../../../images/eurd-web-chart-add-parameter.png)

	Set the parameter's **Binding** property to the report's group field.

	![](../../../../images/eurd-web-chart-bind-parameter.png)

1. Click **Run Designer** to invoke the Chart Designer.

	![](../../../../images/eurd-web-chart-run-designer.png)

1. Bind the chart to data. Specify the **Data Source** and **Data Member** fields.

	![](../../../../images/eurd-web-chart-bind-to-data-designer.png)

1. Add a new series. Click the plus button next to the Series item in the Chart Designer.

	![](../../../../images/eurd-web-chart-designer-add-series.png)

1. Provide data for the argument and value axes. Set the **Argument Data Member** and **Value** properties.

	![](../../../../images/eurd-web-chart-designer-groups-bind-series-to-data.png)

1. Filter the chart. Click the **Filter String** property's ellipsis button.

	![](../../../../images/eurd-web-chart-for-groups-designer-filterstring.png)

	Add a filter condition. On the left side, specify the field by which chart data should be filtered.

	![](../../../../images/eurd-web-chart-for-groups-create-filterstring.png)

	On the right side, use the chart parameter to obtain a group value from the report's group field. Click the right side's down arrow and select **Parameter**. Then select the chart parameter from the context menu.

	![](../../../../images/eurd-web-chart-for-groups-specify-parameter.png)

Click **OK** in the Filter Editor and in the Chart Designer to apply changes.

Switch to [Print Preview](../../preview-print-and-export-reports.md) to see the result.

![](../../../../images/eurd-web-chart-in-group-footer.png)