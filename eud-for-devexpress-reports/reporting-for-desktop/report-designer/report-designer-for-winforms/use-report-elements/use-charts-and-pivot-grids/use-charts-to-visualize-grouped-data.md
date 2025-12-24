---
title: Use Charts to Visualize Grouped Data
author: Anna Gubareva
---
# Use Charts to Visualize Grouped Data

This topic describes how to use charts to visualize grouped data in a report.

![](../../../../images/eurd-win-chart-for-groups-result.png)

In this tutorial, the report data is grouped against a data field (the report's group field). A chart is placed in the Group Footer band and is not bound to data. The report's data source is used to populate the chart with data.

![](../../../../images/eurd-win-chart-group-footer-report-layout.png)

Follow the steps below to make each chart instance display data for its group.

1. Select the chart. Open the [Toolbar](../../report-designer-tools/toolbar.md)'s **Chart Tools** contextual tab and click **Run Designer**.

	![](../../../../images/eurd-win-chart-run-designer-button.png)

1. Add a new series. Click the plus button next to the **Series** item in the Chart Designer.

	![](../../../../images/eurd-win-chart-designer-add-series.png)

	Select a series type.

	![](../../../../images/eurd-win-chart-designer-select-view-type.png)

1. Provide data for the argument and value axes.

	Switch to the created series' **Data** tab. Drop fields onto the **Argument** and **Value** areas.
	
	![](../../../../images/eurd-win-chart-for-groups-designer-data-settings.png)

1. Filter the chart. Go to the **Properties** tab. Click the **Filter String** property's ellipsis button to invoke the FilterString Editor.
	
	![](../../../../images/eurd-win-chart-for-groups-designer-data-filters.png)

	Add a filter condition. On the left side, specify the field by which chart data should be filtered.

	![](../../../../images/eurd-win-chart-group-footer-create-filter-string.png)

	On the right side, use a chart parameter to obtain a group value from the report's group field. Click the right side's icon until it turns into a question mark and select **Add Parameter** from the context menu to invoke the Add New Parameter dialog.

	![](../../../../images/eurd-win-chart-group-footer-create-filter-string-set-parameter.png)

	Set the **Binding** property to the report's group field and click **OK**.

	![](../../../../images/eurd-win-chart-group-footer-add-new-parameter.png)

Click OK in the FilterString Editor and in the Chart Designer to apply changes.

Switch to [Print Preview](../../preview-print-and-export-reports.md) to see the result.

![](../../../../images/eurd-win-chart-for-groups-result.png)