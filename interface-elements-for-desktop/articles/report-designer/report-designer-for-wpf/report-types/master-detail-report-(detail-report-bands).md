---
title: Master-Detail Report (Detail Report Bands)
author: Anna Gubareva
legacyId: 116206
---
# Master-Detail Report (Detail Report Bands)
This tutorial describes the steps needed to create a _master-detail report_ with hierarchically linked data using the [Detail Report band](../report-elements/report-bands.md). For an alternative approach, refer to [Master-Detail Report (Subreports)](master-detail-report-(subreports).md).

To start with this tutorial, [create a new report](../creating-reports/basic-operations/create-a-new-report.md) and [bind it to a data source](../creating-reports/providing-data/binding-a-report-to-data.md). For this tutorial, in the [Report Wizard](../report-wizard.md), select the table that will be used as the principal table in the master-detail relation.

The topic consists of the following sections.
* [Provide a Report Data Source with a Master-Detail Relation](#masterdetail)
* [Design a Master-Detail Report](#designareport)
* [View the Result](#result)

<a name="masterdetail"/>

## Provide a Report Data Source with a Master-Detail Relation
This section of the tutorial describes how to provide an SQL data source with a master-detail relation. If you are using an Entity Framework data source that contains data members with master-detail relations between them, the existing relations will be used automatically. In this case, you can skip this section of the tutorial and proceed to the next section: [Design a Master-Detail Report](#designareport).

To add a master-detail relation to an SQL data source, do the following.
1. Add a detail table to the report data source. To do this, right-click the data source in the [Report Explorer](../interface-elements/report-explorer.md), and select **Manage Queries...** in the invoked context menu.
	
	![EUD_WpfReportDersigner_MasterDetail_1](../../../../images/img123522.png)
2. In the invoked **Manage Queries** dialog, click **Add**.
	
	![EUD_WpfReportDersigner_MasterDetail_2](../../../../images/img123523.png)
3. Then, in the invoked  **Data Source Wizard**, click **Run Query Builder...**.
	
	![EUD_WpfReportDersigner_MasterDetail_3](../../../../images/img123524.png)
4. Add the detail table to the query and click **OK**.
	
	![WPDDesigner_QueryBuilder_AddTable](../../../../images/img122117.png)
5. Click **Finish** to exit the **Data Source Wizard**. Then, click **OK** to exit the **Manage Queries** dialog.
6. Next, specify the relation between the data source tables. To do this, right-click the data source in the **Report Explorer**, and select **Manage Relations...** in the invoked context menu.
	
	![EUD_WpfReportDersigner_MasterDetail_4](../../../../images/img123525.png)
7. In the invoked **Master-Detail  Relation Editor**, click the plus button next to the master query to add a new relation. Specify a relation condition as shown in the following image and click **OK** to exit the dialog.
	
	![EUD_WpfReportDersigner_MasterDetail_5](../../../../images/img123526.png)
8. The **Field List** will be updated to reflect the added relation.
	
	![EUD_WpfReportDersigner_MasterDetail_6](../../../../images/img123527.png)

<a name="designareport"/>

## Design a Master-Detail Report
To create the layout of a master-detail report, do the following.
1. Allocate parts of a master report on the report's Detail band.
	
	![EUD_WpfReportDersigner_MasterDetail_Master](../../../../images/img123528.png)
	­
	
	For the master report to be generated properly, the report's **Data Member** should be set to the master query. If you added the master query first, this property is set to the required value automatically. Otherwise, you should manually specify the data member (for instance, in the [Properties Panel](../interface-elements/properties-panel.md)).
2. To add a detail report band, right-click anywhere on the report's surface, and in the invoked context menu, select **Insert Detail Report**. When the report's data source contains a data relationship, it is displayed in the context menu.
	
	![EUD_WpfReportDersigner_MasterDetail_7](../../../../images/img123529.png)
3. Then, drop the required data fields from the Field List onto the Detail Report band.
	
	Note that you should drop items from the _relation node_ (in this example it is the **CategoriesProducts** section) for the detail report to be generated correctly.
	
	![EUD_WpfReportDersigner_MasterDetail_8](../../../../images/img123531.png)

<a name="result"/>

## View the Result
The master-detail report is now ready. Switch to the [Print Preview](../document-preview.md) tab and view the result.

![EUD_WpfReportDersigner_MasterDetail_Result](../../../../images/img123532.png)