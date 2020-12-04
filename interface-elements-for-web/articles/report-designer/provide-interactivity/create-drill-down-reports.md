---
title: Create Drill-Down Reports
author: Anna Vekhina
---
# Create Drill-Down Reports

This tutorial describes how to create a drill-down report. Clicking a link in such a report displays the previously hidden detailed information in the same report:

![](../../../images/eurd-web-drill-down-report-preview.png)

Do the following to create a drill-down report:

1. [Create a master-detail report using Detail Report bands](..\create-reports\master-detail-reports-with-detail-report-bands.md).
2. Drop a label onto the report's detail band. Clicking this label should expand or collapse the hidden report details.
3. Select the [detail report band](..\introduction-to-banded-reports.md), open the **Behavior** category and expand drop-down menu for the band's **Drill-Down Control** property in the [Properties](..\report-designer-tools\ui-panels\properties-panel.md) panel.
	
	This menu displays all report controls available on the report band that is one level above the current band in the report bands' hierarchy. Select the corresponding label in the menu to make the label expand or collapse the detail report's band when clicked in the Print Preview.
	
	![](../../../images/eurd-web-drilldown-set-drilldown-control.png)
	
	You can also specify the band's **Drill-Down Expanded** property to define whether or not the band is initially expanded. This property is enabled by default.
4. Select the label, expand the **Actions** category and click the **Expression** property's ellipsis button.
	
	![](../../../images/eurd-web-drill-down-report-label-smart-tag.png)
	
	This invokes the [Expression Editor](../report-designer-tools/expression-editor.md) where you can make the label display different text based on the detail report's **DrillDownExpanded** property value.
	
	![](../../../images/eurd-web-drill-down-report-expression.png)