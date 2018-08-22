---
title: Add Page Numbers
---
# Add Page Numbers

The tutorial describes how to add page numbers to your reports.

## <a name="numbers"></a>Add Page Numbers
Do the following to add page numbers to a report:

- Create a [PageFooterBand](..\introduction-to-banded-reports.md) in your report. To do this, right-click anywhere in the report designer, and in the context menu point to **Insert Band**, and then click **PageFooter**.
	
	![eurd-win-add-page-footer](../../../../images/eurd-win-add-page-footer.png)
- Drop the [PageInfo](..\use-report-elements\use-basic-report-controls\page-info.md) control from the [Toolbox](..\report-designer-tools\toolbox.md) to the **PageFooter** band.
	
	![eurd-win-drop-page-info](../../../../images/eurd-win-drop-page-info.png)
- To change the control's display format, click its smart tag, and in the invoked actions list, specify the **TextFormatString** property (e.g., **Page {0} of {1}**, to display the current page number out of the total number of pages).
	
	![eurd-win-pageinfo-formatstring](../../../../images/eurd-win-pageinfo-formatstring.png)

The following image illustrates the resulting report:

![eurd-win-pageinfo_result](../../../../images/eurd-win-pageinfo_result.png)

## <a name="groups"></a>Add Page Numbers for Groups
Do the following to make your report display page numbers for groups or detail reports:

- Add the **GroupFooter** band. To do this, right-click anywhere on the report's surface, and in the invoked menu, point to **Insert Band** and click **GroupFooter**.
	
	![eurd-win-add-groupfooter](../../../../images/eurd-win-add-groupfooter.png)
	
	> [!NOTE]
	> You can force the group header and/or the group footer to be repeated on each page, using the GroupBand's **RepeatEveryPage** property.
- Next, force each new group to start on a separate page. Otherwise, group page numbers will be calculated incorrectly.
	
	To do this, select the Group Footer, and set its **PageBreak** property to *AfterBand*.
	
	![eurd-win-pageinfo-pagebreak](../../../../images/eurd-win-pageinfo-pagebreak.png)
- Drop the [PageInfo](..\use-report-elements\use-basic-report-controls\page-info.md) control from the [Toolbox](..\report-designer-tools\toolbox.md) onto the **GroupFooter** (or **GroupHeader**) band.
	
	![eurd-win-droppageinfo-to-grou-footer.png](../../../../images/eurd-win-droppageinfo-to-grou-footer.png)
- Select the created control, and set its **RunningBand** property to *GroupHeader1*.
	
	![eurd-win-pageinfo-runningband](../../../../images/eurd-win-pageinfo-runningband.png)
	
	> [!TIP]
	> You can use the **TextFormatString** and **PageInfo** properties to adjust the way the control represents its contents.

The following image illustrates the resulting report:

![eurd-win-pagenumbers-for-groups](../../../../images/eurd-win-pagenumbers-for-groups.png)