---
title: Add Sparklines to a Report
author: Anna Gubareva
---
# Add Sparklines to a Report

## Sparkline Overview
The **Sparkline** control displays a compact chart that is commonly used to illustrate the data flow for every row in a report.

To add this control to the report, drag the **Sparkline** item from the [Toolbox](../../report-designer-tools/toolbox.md) and drop it onto the report.

![](../../../../../images/eurd-win-add-sparkline-control-to-report.png)

## Bind the Sparkline to Data
You can connect the sparkline to individual data without accessing a report's data source. Click the control's smart tag, expand the **Data Source** drop-down list and select the required data source.

![](../../../../../images/eurd-win-sparkline-select-data-source.png)

The sparkline uses the report's data source if you do not specify the **DataSource** property.

After that, specify the **Data Member** property and set the **Value Member** property to a data field that provides point values for the sparkline.

To create a new data source for a sparkline, open the [Toolbar](../../report-designer-tools/toolbar.md)'s **Sparkline Tools** contextual tab and click the **Add Data Source** button. This invokes the [Data Source Wizard](../../report-designer-tools/data-source-wizard.md) that allows you to set up a required data source.

## Adjust the Sparkline View
You can select the sparlkline's view type in the **Sparkline Tools** toolbar tab's **View** gallery.

![](../../../../../images/eurd-win-sparkline-tools-toolbar-tab.png)

Alternatively, you can click the sparkline's smart tag and select the required view type in the **View** drop-down list.

The sparkline supports the **Line**, **Area**, **Bar** and **WinLoss** view types.

The **View** property provides access to options that change the sparkline's appearance.

![](../../../../../images/eurd-win-sparkline-view-property.png)

Each view type has properties that define the extreme values' visibility:

* **Highlight Start Point** and **Highlight End Point**;
* **Highlight Min Point** and **Highlight Max Point**.

Specific properties differ between view types, such as the **Highlight Negative Points** setting that is available only for the **Bar** sparkline.

The following image illustrates a [table report](../../create-popular-reports/create-a-table-report.md) containing sparklines that provide maximum and minimum value indicators in their data range:

![](../../../../../images/eurd-win-report-with-sparklines.png)