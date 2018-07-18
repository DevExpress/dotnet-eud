---
title: Add Gauges to a Report
author: Anna Gubareva
---
# Add Gauges to a Report

## Gauge Overview

The **Gauge** control provides you with the capability to embed graphical gauges into your report.

To add this control to the report, drag the **Gauge** item from the [Toolbox](../../report-designer-tools/toolbox.md) and drop it onto the report.

![](../../../../../images/eurd-win-add-gauge-control-to-report.png)

Use the [Toolbar](../../report-designer-tools/toolbar.md)'s **Gauge Tools** contextual tab to select a gauge's appearance.

![](../../../../../images/eurd-win-gauge-tools-toolbar-contextual-tab.png)

* **View**
	
	Specifies the type of the displayed gauge. The following view types are available:

    * **Linear**
		
		![](../../../../../images/eurd-win-gauge-control-linear-type.png)
		
		Supported view styles: **Horizontal** and **Vertical**.
	
	* **Circular**
		
		![](../../../../../images/eurd-win-gauge-control-circular-type.png)
		
		Supported view styles: **Full**, **Half**, **Quarter Left**, **Quarter Right** and **Three Fourth**.

* **Theme**
	
	Specifies the gauge's color theme. The **Flat Light** and **Flat Dark** view themes are supported.
	
	![](../../../../../images/eurd-win-gauge-control-view-theme.png)

The following properties allow you to customize the gauge scale and specify its displayed values.

* **Actual Value** - specifies the value displayed by a gauge.
* **Target Value** - specifies the position of the target value marker.
* **Maximum** - specifies the gauge's maximum value.
* **Minimum** - specifies the gauge's minimum value.

![](../../../../../images/eurd-win-gauge-control-smart-tag-properties.png)


## Bind a Gauge to Data
To [bind](../../bind-to-data/bind-controls-to-data-expression-bindings.md) the gauge's displayed value to data, click the control's smart tag and in the invoked actions list, expand the **Expression** drop-down list for the **Actual Value** property and select the required data field.

![](../../../../../images/eurd-win-gauge-control-bind-to-data.png)

In the same way, you can bind the **Target Value**, **Minimum** and **Maximum** properties to data. To do this, expand the **Expression** drop-down list for the corresponding property and select the required data field.

Clicking the **Expression** option's ellipsis button invokes the **Expression Editor**, in which you can construct a complex binding expression involving two or more data fields.