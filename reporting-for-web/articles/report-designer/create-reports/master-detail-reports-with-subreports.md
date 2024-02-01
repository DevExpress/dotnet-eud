---
title: Master-Detail Reports with Subreports
author: Anna Vekhina
---
# Master-Detail Reports with Subreports

This tutorial demonstrates how to create a master-detail report using the [Subreport](../use-report-elements/use-basic-report-controls/subreport.md) control. This approach is useful if your data source does not contain master-detail relationship or you prefer to store master and detail reports in different files. Another approach is described at [Create a Master-Detail Report (Use Detail Report Bands)](master-detail-reports-with-detail-report-bands.md).

![](../../../images/eurd-web-master-detail-result.png)

## Create a Master Report

1. [Create a new report](../add-new-reports.md) or [open an existing one](../open-reports.md) to use it as a master report.

2. [Bind the report](../bind-to-data.md) to a required data table.

3. Drop the required data fields from the [Field List](../report-designer-tools/ui-panels/field-list.md) onto the [Detail](../introduction-to-banded-reports.md) band.

    ![](../../../images/eurd-web-master-report-layout.png)

## Create the Detail Report

1. [Add one more blank report](../add-new-reports.md) to use it as a detail report.

2. [Bind it to data](../bind-to-data.md). For instance, use another table of the same database as for the master report. 

3. Switch to the **Field List**, select the data fields while holding down CTRL or SHIFT and drag-and-drop them onto the Detail band.
	
	![](../../../images/eurd-web-detail-report-layout.png)

4. Add parameter to the detail report. Select the **Parameters** section in the **Field List** and click **Add parameter**.
	
	![](../../../images/eurd-web-parameters-add-parameter-via-field-list.png)

5. Click the **Edit** button for the created parameter and specify the parameter's **Name** and **Type** as well as disable the **Visible** property.
	
	![](../../../images/eurd-web-detail-report-parameter-settings.png)

6. Switch to the [Properties](../report-designer-tools/ui-panels/properties-panel.md) panel, expand the the control's **Tasks** category and click the **Filter String** property's ellipsis button.
	
	In the invoked [Filter Editor](../report-designer-tools/filter-editor.md), construct an expression where the required data field is compared to the created parameter. To access the parameter, invoke the drop-down list on the right and select **Parameter**.
	
	![](../../../images/eurd-web-detail-report-filter-string.png)

7. Click **Save** | **Save As** in the designer [menu](../report-designer-tools/menu.md) to [save the detail report](../save-reports.md) to the server-side report storage. In the invoked standard **Save** dialog, specify the folder and file name.

	![](../../../images/eurd-web-detail-report-save-dialog.png)



## Embed the Subreport

1. Click the corresponding tab in the bottom left corner of the Design Surface to switch back to the master report.
	
	![](../../../images/eurd-web-master-report-subreport-switch-between-reports.png)

2. Drop the [Subreport](../use-report-elements/use-basic-report-controls/subreport.md) control from the [Toolbox](../report-designer-tools/toolbox.md) onto the **Detail** band.
	
	![](../../../images/eurd-web-master-report-add-subreport.png)

3. Expand the **Subreport Tasks** category and select the previously saved detail report in the **Report Source URL** property's drop-down list.
	
	![](../../../images/eurd-web-master-report-subreport-report-source-url.png)

	You can double-click the added subreport to open the detail report.
	
4. Bind the subreport's parameter used as a filter criterion to the master report's corresponding data field, which serve as a source of the parameter value. To do this, expand the **Data** category, select the **Parameter Bindings** section and add a new parameter binding.  In the binding properties list, specify the data field to which you want to bind a subreport parameter and the name of the parameter that you want to bind.
	
	![](../../../images/eurd-web-master-report-subreport-parameter-binding.png)
	
5. If required, customize the report's [appearance](../customize-appearance.md) and [format values](../shape-report-data/format-data.md).

## View the Result

Switch to [Print Preview](../preview-print-and-export-reports.md) to see the resulting report.

![](../../../images/eurd-web-master-detail-result.png)