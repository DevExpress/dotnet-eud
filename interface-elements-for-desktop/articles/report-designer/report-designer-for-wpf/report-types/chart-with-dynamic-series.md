---
title: Chart with Dynamic Series
author: Anna Gubareva
legacyId: 116212
---
# Chart with Dynamic Series
This document describes how to create a report with a [Chart](../report-elements/report-controls.md) control bound to data, so that all series are auto-created based on a common template, which specifies universal options for all series. This is possible when data for all series (their names, along with point arguments and values) is stored in the same data table.

Note that in this scenario, the view type and certain other settings will be the same for all series.

To adjust a Chart with automatically created series, do the following.
1. [Create a new empty report](../creating-reports/basic-operations/create-a-new-report.md).
2. Drop the [Chart](../report-elements/report-controls.md) control from the [Toolbox](../interface-elements/control-toolbox.md) onto the report's [Detail band](../report-elements/report-bands.md).
	
	![EUD_WpfReportDersigner_Chart_1](../../../../images/img123911.png)
	
	After you drop the Chart, the **Chart Designer** is automatically invoked. At this step, click **Cancel** to close the Designer, it will be used later.
3. To bind the Chart to a data source, right-click it and select **Edit...** in the context menu. Then, in the invoked dialog, expand the **Data Source** drop-down and click **Add New**.
	
	![EUD_WpfReportDersigner_Chart_2](../../../../images/img123912.png)
	
	The invoked **Data Source Wizard** will guide you through the process of assigning a data source to the Chart. For detailed instructions on the Wizard's steps, refer to [Binding a Report to Data](../creating-reports/providing-data/binding-a-report-to-data.md), as this process is similar.
	
	After the data source is created, it is assigned to the Chart's **Data Source** property. Its **Data Member** property defines from which table or view of your data source the Chart obtains its data.
	
	![EUD_WpfReportDersigner_ChartDyn_3](../../../../images/img123921.png)
	
	> [!NOTE]
	> Since you have placed a Chart in the Detail band, the report's **Data Source** property should not be set. Otherwise, the Chart will be repeated at the preview as many times as there are records in the data source.
	> 
	> ![EUD_WpfReportDesigner_CrossTabReport_4](../../../../images/img123582.png)
4. Once again, right-click the Chart and select **Run Designer...** in the context menu.
	
	![EUD_WpfReportDersigner_ChartStat_4](../../../../images/img123914.png)
5. When the chart is added to the report, a new static series is created automatically. In the invoked **Chart Designer**, remove this series by clicking the corresponding button.
	
	![chart-designer-remove-default-series](../../../../images/img126211.png)
6. Then, go to the **Data** tab at the right of the Designer's window. Choose an existing data source in the dedicated drop-down list and drag-and-drop the required data fields to the corresponding cells.
	
	The **Series** cell specifies the data field, which should provide data for the series names, so that a new series is created for each record in that data field. Use the **Argument** and **Value** cells to define from where data for point arguments and values is obtained.
	
	![chart-designer-auto-created-series](../../../../images/img126212.png)
7. Switch to the **Properties** tab and expand the **Series Template** option. As you can see, the **Argument Data Member** and **Value Data Members** properties have been automatically assigned to the corresponding data fields. Make sure that the **Argument Scale Type** and **Value Scale Type** properties are set to appropriate values.
	
	![chart-designer-auto-created-series-properties](../../../../images/img126213.png)
8. At this point, the chart's data options are completely defined, so in this step, certain additional customization capabilities are described.
	* **Adjust the Series Name Template**
		
		By default, the name for every auto-created series is obtained directly from an appropriate data field in the bound data source. However, you can add some text to the beginning or to the end of every series name using the Chart's **Series Name Template** property. For instance, set the **Begin Text** property to "GSP in ".
	* **Customize Series Labels**
		
		To avoid the overlapping of series labels, expand the Chart's **Series Template** property and set the **Labels Visibility** property to **No**.
	
	If required, it is possible to customize many other properties for the Chart, which are not described here.

The chart is now ready. Switch to the [Print Preview](../document-preview.md) tab and view the result.

![EUD_WpfReportDersigner_ChartDyn_Result](../../../../images/img123926.png)