---
title: Create a Combined Report Layout
author: Eugeniy Burmistrov
legacyId: 14332
---
# Create a Combined Report Layout
Snap allows you to create a single combined report, incorporating features of different report layout types. There is no limits on how many reports you can combine.

In this tutorial, we will create a combined report that uses the features of mail-merge and chart-based reports.

The tutorial consists of the following sections.
* [Add Mail-Merge Report Functionality](#mailmerge)
* [Add Chart-Based Report Functionality](#chart)
* [View the Result](#result)

## <a name="mailmerge"/>Add Mail-Merge Report Functionality
In this section, we will create a simple **Mail-Merge Report**.
1. Create a new Snap document and [provide it with a master-detail data connection](../connect-to-data/create-a-master-detail-data-source.md).
2. Specify which data source will be used for mail merge by right-clicking the required data source in the Data Explorer and select **Use For Mail Merge** in the invoked drop-down menu.
	
	![combined-report-0](../../../images/img23854.png)
3. Insert a master report part. To do this, drag-and-drop data fields from the [Data Explorer](../graphical-user-interface/snap-application-elements/data-explorer.md) onto the  [Design Surface](../graphical-user-interface/snap-application-elements/design-surface.md).
	
	![combined-report-1](../../../images/img23857.png)
4. To insert a detail report part, drag-and-drop fields from a subordinate node of the data source.
	
	![combined-report-2](../../../images/img23858.png)
	
	The added detail part will have a tabular form by default.
	
	![combined-report-7](../../../images/img23864.png)

For more information on the creation mail-merge report, see the tutorial [Create a Mail-Merge Report](create-a-mail-merge-report.md).

## <a name="chart"/>Add Chart-Based Report Functionality
In this section we will add a **Chart** to the Snap document.
1. Click the **Chart** command in the [Insert](../graphical-user-interface/main-toolbar/general-tools-insert.md) tab of the main toolbar.
	
	![combined-report-3](../../../images/img23859.png)
2. In the created chart, the blue circles correspond to the values and arguments of the chart. Drop one field from a subordinate node of the data source onto the "values" region in the chart...
	
	![combined-report-4](../../../images/img23860.png)
	
	...and the other onto the "arguments" region.
	
	![combined-report-5](../../../images/img23861.png)

For more information on the creation of a chart-based report, see the tutorial [Create a Chart-Based Report](create-a-chart-based-report.md).

## <a name="result"/>View the Result
* The Snap mail merge document is now ready. To view the result, click the **Finish &amp; Merge** button in the [Mail Merge](../graphical-user-interface/main-toolbar/data-tools-mail-merge.md) tab, and select **Print Preview...** in the invoked  drop-down menu. In the invoked **Export Range** dialog, select **All records** and click **OK**.
	
	![snap-mail-merge-print-preview](../../../images/img22411.png)
	
	The following image illustrates a print preview for the final document.
	
	![combined-report-6](../../../images/img23862.png)