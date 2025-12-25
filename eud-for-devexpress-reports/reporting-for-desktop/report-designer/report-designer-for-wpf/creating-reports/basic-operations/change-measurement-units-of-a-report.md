---
title: Change Measurement Units of a Report
author: Anna Gubareva
legacyId: 116288
---
# Change Measurement Units of a Report
For your report, you can choose its global **Measure Units**, which can be **Hundredths of an Inch**, **Inches**, **Tenths of a Millimeter**, **Millimeters**, or **Pixels**.

To specify the **Measure Unit** property, do one of the following:
* Click the report’s smart tag and set this property to the required value.
	
	![EUD_WpfReportDesigner_MeasureUnit_1](../../../images/img123773.png)
* Select the report and switch to the [Properties Panel](../../interface-elements/properties-panel.md). Expand the **Measure Units** drop-down and select the required value.
	
	![EUD_WpfReportDesigner_MeasureUnit_2](../../../images/img123774.png)

This defines the basic measurement unit for all the unit-related options of a report and its [bands](../../report-elements/report-bands.md) and [controls](../../report-elements/report-controls.md) (such as location, size, border width, etc.) as well as the measurement unit of the report's [Snap Grid](control-positioning.md).

> [!Note]
> Changing the system of measurement results in converting the corresponding property values and updating the layout of all report elements in the Report Designer. Notably, the system of measurement determines the minimum increment with which an element's location and sizes can be changed.