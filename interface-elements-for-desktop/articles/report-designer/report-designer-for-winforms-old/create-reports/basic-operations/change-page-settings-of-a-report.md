---
title: Change Page Settings of a Report
author: Eugeniy Burmistrov
legacyId: 5211
---
# Change Page Settings of a Report
In the Report Designer, page settings of a report can be specified in one of two ways. The first approach forces the default printer settings to be used when the report is printed, while the other one enables you to alter page settings independently.
* **Using settings of the default printer**
	
	For the orientation, margins and paper size, you can specify a requirement that applies the corresponding printer settings instead of the report's. In this instance, the page properties in the [Property Grid](../../report-designer-reference/report-designer-ui/property-grid.md) are disabled and displayed as grayed out. This may be useful when the report is printed in several places with different printers and printer settings.
	
	![RD_PageSettings_0](../../../../../images/img8896.png)
* **Specify the report's page settings**
	
	While designing the report, you can specify the page settings via the Property Grid:
	
	![RD_PageSettings_1](../../../../../images/img8897.png)
	
	You can set the page orientation and modify the margins. The margin values are expressed in the report's [measurement units](change-measurement-units-of-a-report.md). You can select from the predefined paper sizes (**Paper Kind** property), choose **Custom** and create your own paper size, or select one which is already defined for this printer (**Paper Name** property).
	
	These settings affect the layout of the report's design surface. After their modification, you may notice red warning marks, indicating that the controls go beyond the page width. These warnings can be switched off by setting the **Show Printing Warnings** property of the report to **No**.
	
	![RD_Report_ShowPrintingWarnings](../../../../../images/img8528.png)
* **Modify the settings in Preview Tab**
	
	The report's [Preview Tab](../../report-designer-reference/report-designer-ui/preview-tab.md) toolbar has a corresponding button that enables you to modify the page settings. Clicking this button invokes the **Page Setup** dialog, which allows you to adjust the page layout before printing or exporting, and select the printer.
	
	![RD_PageSettings_1a](../../../../../images/img8899.png)
	
	The margins can also be set visually by dragging the dashed lines in the Preview Tab as needed.
	
	To change the measurement units shown in the margins tooltips, customize the report's **Measure Units** property.

| **Measure Units = Hundredths of an Inch** |
|---|
| ![RD_PageSettings_2](../../../../../images/img8898.png) |
| **Measure Units = Tenths of a Millimeter** |
| ![RD_PageSettings_2a](../../../../../images/img9042.png) |

To learn about other options available for a report, refer to [Report Settings](../../report-designer-reference/report-settings.md).