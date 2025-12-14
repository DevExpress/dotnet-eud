---
title: Change a Report's Measurement Units
author: Natalia Kazakova
---
# Change a Report's Measurement Units

Most metrics of report elements (i.e., element locations, dimensions and margins) can be expressed in units that correspond to one of the following systems of measurement.

* **Imperial system**: hundredths of an inch, inches.
	
	This is the default system that is assigned to each new report.
* **Metric system**: tenths of a millimeter, millimeters.
* **Screen coordinates**: pixels.

To assign a system of measurements to a report, use its **Measure Units** property. You can specify this property in the report's smart tag:

![](../../../images/eurd-win-measure-units-in-smart-tag.png)

Alternatively, you can enable this property in the [Property Grid](../report-designer-tools/ui-panels/property-grid-tabbed-view.md)'s **Behavior** tab:

![](../../../images/eurd-win-measure-units-in-property-grid.png)

> [!Note]
> Changing the system of measurement results in converting the corresponding property values and updating the layout of all report elements in the Report Designer. Notably, the system of measurement determines the minimum increment with which an element's [location and size](../use-report-elements/manipulate-report-elements/arrange-report-controls.md) can be changed.

You can control whether to display exact element size while resizing. For this, toggle the **Dimension Notation** option in the View tab:

![Report Designer - Control Dimension Notations Visibility in UI](~/eud-for-devexpress-reports/reporting-for-desktop/images/vs-dimension-notation-ui.png)

The notation are based on a selected report unit:

| System of Measurement | Displayed Unit | Image |
| --- | --- | --- |
| Imperial system     | inches | ![Report Designer - Dimension Notations in inches](~/eud-for-devexpress-reports/reporting-for-desktop/images/vs-dimension-notation-imperial-unit.png)     |
| Metric system     | millimeters | ![Report Designer - Dimension Notations in millimeters](~/eud-for-devexpress-reports/reporting-for-desktop/images/vs-dimension-notation-metric-unit.png)     |
| Screen coordinates | pixels |![Report Designer - Dimension Notations in pixels](~/eud-for-devexpress-reports/reporting-for-desktop/images/vs-dimension-notation-pixels-unit.png) |