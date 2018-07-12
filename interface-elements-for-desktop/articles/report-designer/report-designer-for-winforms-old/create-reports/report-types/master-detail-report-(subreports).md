---
title: Master-Detail Report (Subreports)
author: Anna Gubareva
legacyId: 115568
---
# Master-Detail Report (Subreports)
This tutorial describes the steps needed to create a master-detail report using the [Subreport](../../report-designer-reference/report-controls/subreport.md) control. For an alternative approach, refer to [Master-Detail Report (Detail Report Bands)](master-detail-report-(detail-report-bands).md).

To create a master-detail report using the subreport controls, do the following.
* [Create a Master Report](#create)
* [Create and Customize a Detail Report](#detail)
* [Embed the Subreport](#subreport)
* [Get the Result](#result)

<a name="create"/>

## Create a Master Report
1. [Create a new report](../basic-operations/create-a-new-report.md) and [bind it to a data source](../binding-a-report-to-data.md). This report will be used as the master report.
2. Drop the required fields from the [Field List](../../report-designer-reference/report-designer-ui/field-list.md) panel onto the [Detail Band](../../report-designer-reference/report-bands/detail-band.md). In this example, the following report layout is used.
	
	![RD_MasterDetail_Subreports1](../../../../../images/img122063.png)
3. Drag the [Subreport](../../report-designer-reference/report-controls/subreport.md) control from the **Toolbox** and drop it onto the [Detail Band](../../report-designer-reference/report-bands/detail-band.md).
	
	![RD_MasterDetail_Subreports2](../../../../../images/img122064.png)

<a name="detail"/>

## Create and Customize the Detail Report
1. Next, [add one more blank report](../basic-operations/create-a-new-report.md) and [bind it to the same data source](../binding-a-report-to-data.md). It will be used as a detail report.
2. Drop the required fields from the [Field List](../../report-designer-reference/report-designer-ui/field-list.md) panel onto the [Detail Band](../../report-designer-reference/report-bands/detail-band.md). This tutorial uses the following layout for the detail report.
	
	![RD_MasterDetail_Subreports3](../../../../../images/img122065.png)
3. To add a parameter to the report, right-click the **Parameters** section and choose **Add Parameter** in the [Field List](../../report-designer-reference/report-designer-ui/field-list.md).
	
	![RD_MasterDetail_Subreports4](../../../../../images/img122066.png)
4. In the invoked **Add New Parameter** dialog, specify the parameter's options as shown in the image below.
	
	![RD_MasterDetail_Subreports5](../../../../../images/img122067.png)
5. Then, click the report's [Smart Tag](../../report-designer-reference/report-designer-ui/smart-tag.md), and in its actions list, click the ellipsis button for the **Filter String** property.
	
	In the invoked **FilterString Editor**, construct an expression where the **Category ID** data field is compared to the **CatID** parameter. To access the parameter, click the icon on the right until it turns into a question mark.
	
	![RD_MasterDetail_Subreports6](../../../../../images/img122068.png)
6. To save the detail report, select **File | Save As** in the [Main Menu](../../report-designer-reference/report-designer-ui/main-menu.md). Then, in the invoked standard **Save** dialog, specify the folder and file name.
	
	![Report-SaveAs](../../../../../images/img11066.png)

<a name="subreport"/>

## Embed the Subreport
1. Next, switch back to the master report. Click the subreport control's smart tag, then click the ellipsis button for the **ReportSource URL** property and select the previously saved detail report.
	
	![RD_MasterDetail_Subreports7](../../../../../images/img122069.png)
2. Then, bind the subreport's **CatID** parameter used as a filtering criterion to the master report's **CategoryID** data field, which will serve as a source of the parameter value. To do this, click the subreport's smart tag and select **Edit Parameter Bindings** in the invoked actions list.
	
	![RD_MasterDetail_Subreports8](../../../../../images/img122070.png)
	
	This will invoke a **Parameter Binding Collection Editor**. Click **Add** to add new binding. In the binding properties list, specify the data field to which you want to bind a subreport parameter and the name of the parameter that you want to bind.
	
	![RD_MasterDetail_Subreports9](../../../../../images/img122071.png)

<a name="result"/>

## Get the Result
The master-detail report is now ready to be generated. You can view the result by switching to the [Preview Tab](../../report-designer-reference/report-designer-ui/preview-tab.md).

![RD_MasterDetail_SubreportsResult](../../../../../images/img122073.png)