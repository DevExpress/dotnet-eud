---
title: Use Charts to Visualize Data in Report Groups
author: Anna Gubareva
---
# Use Charts to Visualize Data in Report Groups

This tutorial describes how to use charts to visualize data in each report group.

![](../../../../../images/eurd-win-chart-for-groups-result.png)

## Group Report Data

Do the following to group data in a report:

1. [Bind the report](../../bind-to-data.md) to a database table (for instance, **Products**).

1. Drop the **ProductName** field from the [Field List](../../report-designer-tools/ui-panels/field-list.md) onto the report's Detail band.

	![](../../../../../images/eurd-win-chart-for-groups-add-field-to-detail-band.png)

1. Click **Add a Group** in the [Group and Sort](../../report-designer-tools/ui-panels/group-and-sort-panel.md) panel and select group criteria (for example, the **CategoryID** field).

	![](../../../../../images/eurd-win-chart-for-groups-group-data.png)

1. Enable the **Show Footer** check box to add a Group Footer to the report.

	![](../../../../../images/eurd-win-chart-for-groups-show-footer.png)

1. Drop the **CategoryID** field onto the Group Header to display group titles in the report.

	![](../../../../../images/eurd-win-chart-for-groups-add-field-to-group-header.png)

## Create a Chart

Do the following to add a chart to the report:

1. Drop the **Chart** control from the [Toolbox](../../report-designer-tools/toolbox.md) onto the Group Footer.

	![](../../../../../images/eurd-win-chart-for-groups-add-chart.png)

    Close the Chart Designer if it is invoked.

1. Click the chart's smart tag. Click the **Parameters** property's ellipsis button.

	![](../../../../../images/eurd-win-chart-group-footer-click-parameters.png)

1. Click **Add** in the invoked editor. This creates a new chart parameter.

	![](../../../../../images/eurd-win-chart-group-footer-add-parameter.png)

1. Expand the **Binding** drop-down list and select a data field.

	![](../../../../../images/eurd-win-chart-group-footer-bind-parameter.png)

	Click **OK** to close the editor.

1. Open the [Toolbar](../../report-designer-tools/toolbar.md)'s **Chart Tools** contextual tab and click the **Run Designer** button.

	![](../../../../../images/eurd-win-chart-run-designer-button.png)

1. Click the plus button next to the **Series** item in the **Chart Designer** to add a new series.

	![](../../../../../images/eurd-win-chart-designer-add-series.png)

	Select a series view type.

	![](../../../../../images/eurd-win-chart-designer-select-view-type.png)

1. Switch to the created series' **Data** tab.
	
	Drop the **ProductName** field onto the Argument area and the **UnitPrice** field onto the Value area.
	
	![](../../../../../images/eurd-win-chart-for-groups-designer-data-settings.png)

1. Switch to the **Properties** tab. Click the **Filter String** property's ellipsis button. Construct filter criteria in the invoked FilterString Editor and click OK.
	
	![](../../../../../images/eurd-win-chart-for-groups-designer-data-filters.png)

	Click **OK** to close the **Chart Designer** window.

Switch to [Print Preview](../../preview-print-and-export-reports.md) to see the resulting report.

![](../../../../../images/eurd-win-chart-for-groups-result.png)