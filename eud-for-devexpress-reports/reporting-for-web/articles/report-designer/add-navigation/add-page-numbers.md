---
title: Add Page Numbers
author: Anna Vekhina
---
# Add Page Numbers

The tutorial describes how to add page numbers to your reports.

## <a name="numbers"></a>Add Page Numbers
Do the following to add page numbers to a report:

- Create a [PageFooterBand](../introduction-to-banded-reports.md) in your report. To do this, select **Insert Page Footer Band** in the context menu.
	
	![](../../../images/eurd-web-add-page-footer.png)
- Drop the [PageInfo](../use-report-elements/use-basic-report-controls/page-info.md) control from the [Toolbox](../report-designer-tools/toolbox.md) to the **Page Footer** band.
	
	![](../../../images/eurd-web-drop-page-info.png)
- To change the control's display format, specify the **Text Format String** property (e.g., **Page {0} of {1}**, to display the current page number out of the total number of pages) in the **Page Info Tasks** category.
	
	![](../../../images/eurd-web-pageinfo-formatstring.png)

The following image illustrates the resulting report:

![](../../../images/eurd-web-pageinfo_result.png)

## <a name="groups"></a>Add Page Numbers for Groups
Do the following to make your report display page numbers for groups or detail reports:

- Add the **Group Footer** band. To do this, select **Insert Group Footer Band** in the context menu.
	
	![](../../../images/eurd-web-report-bands-add-bands.png)
	
	> [!NOTE]
	> You can force the group header and/or the group footer to be repeated on each page, using the GroupBand's **Repeat Every Page** property.
- Next, force each new group to start on a separate page. Otherwise, group page numbers will be calculated incorrectly.
	
	To do this, select the Group Footer, and set its **Page Break** property to *After the Band*.
	
	![](../../../images/eurd-web-pageinfo-pagebreak.png)
- Drop the [PageInfo](../use-report-elements/use-basic-report-controls/page-info.md) control from the [Toolbox](../report-designer-tools/toolbox.md) onto the **Group Footer** (or **Group Header**) band.
	
	![](../../../images/eurd-web-drop-pageinfo-to-group-footer.png)
- Select the created control, and set its **Running Band** property to *GroupHeader1*.
	
	![](../../../images/eurd-web-pageinfo-runningband.png)
	
	> [!TIP]
	> You can use the **Text Format String** and **Page Information** properties to adjust the way the control represents its contents.

The following image illustrates the resulting report:

![](../../../images/eurd-web-pagenumbers-for-groups.png)