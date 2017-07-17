---
title: Filtering Data
author: Anna Gubareva
legacyId: 116282
---
# Filtering Data
If a report is [bound to a data source](../../../report-designer-for-winforms/create-reports/binding-a-report-to-data.md) that contains far more data rows than are necessary for processing report creation, you can exclude excessive or undesired data. To accomplish this, construct a filtering expression using single or multiple data fields.

This document describes two approaches to filtering data in the Report Designer.
* [Filter Data at the Report Level](#report)
* [Filter Data at the Data Source Level](#datasource)

<a name="report"/>

## Filter Data at the Report Level
To filter a report's data, do the following.
1. Right-click the report and select **Edit...** in the context menu. In the invoked dialog, click the ellipsis button for the **Filter String** property.
	
	![EUD_WpfReportDersigner_Filtering_1](../../../../../images/img123691.png)
2. Then, in the invoked Filter String Editor, specify the filtering expression.
	
	![EUD_WpfReportDersigner_Filtering_2](../../../../../images/img123692.png)
	
	When creating a filter criteria, you can create and edit logical expressions, and also join the expression groups with And, Or, NotAnd, and NotOr operators. In every filter condition, the left part contains either the data field name, or the name of the [calculated field](../providing-data/calculated-fields.md), which exists in this data source at the same level. The right part of the condition contains either a certain numerical or string value, or the name of the [report parameter](../providing-data/report-parameters.md).
	
	To access parameters, click the icon on the right, until it turns into a question mark.
	
	![EUD_WpfReportDersigner_Filtering_3](../../../../../images/img123693.png)
	
	To quit the dialog and save the changes, click **OK**.

<a name="datasource"/>

## Filter Data at the Data Source Level
To filter data before it has been supplied to a report, you can modify a query of an SqlDataSource assigned to the report's **Data Source** property. To do this, perform the following steps.
1. Invoke the **Manage Queries** dialog using one of the following ways.
	* Switch to the [Report Explorer](../../interface-elements/report-explorer.md) and right-click the data source item under the **Components** node. In the invoked context menu, select the **Manage Queries...** command.
		
		![EUD_WpfReportDersigner_MasterDetail_1](../../../../../images/img123522.png)
	* Select a data source, and in the [Properties Panel](../../interface-elements/properties-panel.md), click the ellipsis button for the **Queries** property.
		
		![EUD_WpfReportDersigner_sqlDataSourceQueries](../../../../../images/img123855.png)
2. In the invoked dialog, click the ellipsis button corresponding to the required query.
	
	![EUD_WpfReportDersigner_ManageQueriesDialog](../../../../../images/img123861.png)
3. Next, in the invoked **Data Source Wizard**, click the **Run Query Builder...** button.
	
	![EUD_WpfReportDersigner_Filtering_4](../../../../../images/img123870.png)
4. In the **Query Builder**, click the **Filter...** button.
	
	![EUD_WpfReportDersigner_Filtering_5](../../../../../images/img123871.png)
5. In the invoked **Filter Editor**, construct a filtering expression that will be used to filter resulting data at the data source level.
	
	![EUD_WpfReportDersigner_Filtering_6](../../../../../images/img123872.png)
	
	Note that it is possible to embed [query parameters](../providing-data/query-parameters.md) into the expression.