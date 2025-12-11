---
title: Master-Detail Report (Subreports)
author: Anna Gubareva
legacyId: 116207
---
# Master-Detail Report (Subreports)
This tutorial describes the steps needed to create a master-detail report with hierarchically linked data using the [Subreport](../report-elements/report-controls.md) control. For an alternative approach, refer to [Master-Detail Report (Detail Report Bands)](master-detail-report-(detail-report-bands).md).

To create a master-detail report using the subreport controls, do the following.
* [Create a Master Report](#create)
* [Create and Customize a Detail Report](#detail)
* [Embed the Subreport](#subreport)
* [Get the Result](#result)

<a name="create"/>

## Create a Master Report
1. [Create a new report](../creating-reports/basic-operations/create-a-new-report.md) and [bind it to a data source](../creating-reports/providing-data/binding-a-report-to-data.md). This report will be used as the master report.
2. Drop the required fields from the [Field List](../interface-elements/field-list.md) panel onto the [Detail band](../report-elements/report-bands.md). In this example, the following report layout is used.
	
	![EUD_WpfReportDersigner_MasterDetail_Master](../../../../images/img123528.png)
3. Drag the [Subreport](../report-elements/report-controls.md) control from the [Toolbox](../interface-elements/control-toolbox.md) and drop it onto the Detail band.
	
	![EUD_WpfReportDesigner_MasterDetail_Subreport1](../../../../images/img123549.png)

<a name="detail"/>

## Create and Customize the Detail Report
1. Next, [add one more blank report](../report-wizard/empty-report.md) and [bind it to the same data source](../creating-reports/providing-data/binding-a-report-to-data.md). It will be used as a detail report.
2. Drop the required fields from the Field List panel onto the Detail band. This tutorial uses the following layout for the detail report.
	
	![EUD_WpfReportDesigner_MasterDetail_Subreport2](../../../../images/img123550.png)
3. To add a parameter to the report, right-click the **Parameters** section in the **Field List** and choose **Add Parameter** in the invoked context menu.
	
	![EUD_WpfReportDesigner_MasterDetail_Subreport3](../../../../images/img123551.png)
4. In the invoked **Add New Parameter** dialog, specify its options as shown in the image below.
	
	![EUD_WpfReportDesigner_MasterDetail_Subreport3a](../../../../images/img124070.png)
5. Select **Edit...** in the report's context menu. Then, in the **Edit** dialog, click the ellipsis button for the **Filter String** property.
	
	In the invoked **Filter String Editor**, construct an expression where the **Category ID** data field is compared to the **CatID** parameter. To access the parameter, click the icon on the right until it turns into a question mark.
	
	![EUD_WpfReportDesigner_MasterDetail_Subreport4](../../../../images/img123552.png)
6. To save the detail report, click the **Save As** ![WPFDesigner_Toolbar_SaveAsIcon](../../../../images/img120138.png) button  in the [Toolbar](../interface-elements/toolbar.md). Then, in the invoked standard **Save** dialog, specify the folder and file name.

<a name="subreport"/>

## Embed the Subreport
1. Next, switch back to the master report. Right-click the subreport and select **Edit...** in the invoked context menu. In the **Edit** dialog, click the ellipsis button for the **Report Source URL** property and select the previously saved detail report.
	
	![EUD_WpfReportDesigner_MasterDetail_Subreport5](../../../../images/img123553.png)
2. Then, bind the subreport's **CatID** parameter used as a filtering criterion to the master report's **CategoryID** data field, which will serve as a source of the parameter value. To do this, select **Edit Parameter Bindings...** in the subreport's context menu.
	
	![EUD_WpfReportDesigner_MasterDetail_Subreport6](../../../../images/img123554.png)
	
	This will invoke the **Parameter Binding Collection Editor**. Click **Add** to add new binding. In the binding properties list, specify the data field to which you want to bind a subreport parameter and the name of the parameter that you want to bind.
	
	![EUD_WpfReportDesigner_MasterDetail_Subreport7](../../../../images/img123555.png)

<a name="result"/>

## Get the Result
The master-detail report is now ready to be generated. You can view the result by switching to the [Print Preview](../document-preview.md) tab.

![EUD_WpfReportDersigner_MasterDetail_Result](../../../../images/img123532.png)