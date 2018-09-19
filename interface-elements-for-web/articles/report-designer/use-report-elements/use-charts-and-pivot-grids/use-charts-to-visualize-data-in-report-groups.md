---
title: Use Charts to Visualize Data in Report Groups
author: Anna Vekhina
---
# Use Charts to Visualize Data in Report Groups

This tutorial describes how to use charts to visualize data in each report group. 

![](../../../../images/eurd-web-chart-in-group-footer.png)

## Group Report Data
Do the following to group data in a report:

* [Bind the report](../../bind-to-data.md) to the required database table (for instance, **Products**).

* Drop the **ProductName** field from the [Field List](../../report-designer-tools/ui-panels/field-list.md) onto the report's Detail band.
	
	![](../../../../images/eurd-web-chart-for-groups-add-field-to-detail-band.png)

*  Switch to the [Properties](../../report-designer-tools/ui-panels/properties-panel.md) panel and add a Group Header band to the report by clicking the corresponding button in the **Actions** category.

    ![](../../../../images/eurd-web-chart-add-group-band.png)

*  Select the Group Header band and expand the **Actions** category. Then, in the **Group Fields** section, click the **Add** button to add a new grouping.

    ![](../../../../images/eurd-web-chart-add-grouping.png)

*  Next, choose a data member across which the report is to be grouped (for example, the **CategoryID** field). Note that grouping across [calculated fields](../../shape-report-data/use-calculated-fields/calculated-fields-overview.md) is supported as well.

    ![](../../../../images/eurd-web-chart-bind-grouping-to-data-field.png)

To manage the sorting order of the group's items, use the corresponding arrow button.  

* Drop the **Category ID** field onto the Group Header to display group titles in the report.

    ![](../../../../images/eurd-web-chart-drop-data-field-onto-group-field.png)


## Create a Chart
Do the following to add a chart to the report:

* Drop the **Chart** control from the [Toolbox](../../report-designer-tools/toolbox.md) onto the Group Footer.
	
	![](../../../../images/eurd-web-chart-add-to-group-footer.png)
   
* Click **Run Designer** to invoke the Chart Designer. Locate the **Series** element in the chart elements tree and click the plus button. Select the view type (for example, **Bar**) in the invoked series type list.
	
	![](../../../../images/eurd-web-chart-designer-add-series.png)

* Specify the **Argument Data Member** and **Value** properties.
	
	![](../../../../images/eurd-web-chart-designer-bind-series-to-data.png)

* Expand the **Data Filters** category and click the plus button to add a new data filter. 
	
	Set the filter's **Column Name** and **Value Binding** properties to the **CategoryID** field that is used as group criteria in the report.
	
	![](../../../../images/eurd-web-chart-for-groups-designer-data-filter-editor.png)
	
	Only the **Value Binding** setting is taken into account when the **Value** and **Value Binding** properties are specified for a data filter.

Switch to [Print Preview](../../preview-print-and-export-reports.md) to see the resulting report.