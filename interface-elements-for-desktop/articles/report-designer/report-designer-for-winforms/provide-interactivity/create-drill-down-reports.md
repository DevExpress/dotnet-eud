---

title: Create Drill-Down Reports
---
# Create Drill-Down Reports

This tutorial describes how to create a drill-down report. Clicking a link in such a report displays the previously hidden detailed information in the same report:

![eurd-win-drill-down-report-preview](../../../../images/eurd-win-drill-down-report-preview.png)

Do the following to create a drill-down report:

1. [Create a master-detail report using Detail Report bands](..\create-popular-reports\create-a-master-detail-report-use-detail-report-bands.md).
2. Drop a label onto the report's detail band. Clicking this label should expand or collapse the hidden report details.
3. Select the [detail report band](..\introduction-to-banded-reports.md) by clicking its header and expand the drop-down menu for the band's **DrillDownControl** property in the [Property Grid](..\report-designer-tools\ui-panels\property-grid.md).
	
	This menu displays all report controls available on the report band that is one level above the current band in the report bands' hierarchy. Select the corresponding label in the menu to make the label expand or collapse the detail report's band when clicked in the Print Preview.
	
	![eurd-win-drilldown-set-drilldown-controll](../../../../images/eurd-win-drilldown-set-drilldown-control.png)
	
	You can also specify the band's **DrillDownExpanded** property to define whether or not the band is initially expanded. This property is set to **true** by default.
4. Click this label's smart tag and select the **Expression** property.
	
	![eurd-win-drill-down-report-label-smart-tag](../../../../images/eurd-win-drill-down-report-label-smart-tag.png)
	
	This invokes the **Expression Editor** where you can make the label display different text based on the detail report's **DrillDownExpanded** property value.
	
	![eurd-win-drill-down-report-expression](../../../../images/eurd-win-drill-down-report-expression.png)