---
title: Query Builder
author: Anna Gubareva
legacyId: 117891
---
# Query Builder
This document describes the **Query Builder** that provides a visual interface for constructing SQL queries and enables you to solve a variety of tasks.

![eud-win-report-designer-query-builder](../../../../../images/img126867.png)

> [!NOTE]
> The Query Builder is not available for [object](../../report-wizard/data-bound-report/connect-to-an-object-data-source.md), [Entity Framework](../../report-wizard/data-bound-report/connect-to-an-entity-framework-data-source.md) and [Excel](../../report-wizard/data-bound-report/connect-to-an-excel-data-source.md) data sources.

The document consists of the following sections.
* [Run the Query Builder](#runquerybuilder)
* [Select Tables](#selecttables)
* [Join Tables](#jointables)
* [Edit Parameters](#editparameters)
* [Filter Data](#filterdata)
* [Shape Data](#shapedata)
* [Enable Custom SQL Editing](#customsql)
* [Preview Results](#previewresults)

## <a name="runquerybuilder"/>Run the Query Builder
You can invoke the **Query Builder** from the [query customization](../../report-wizard/data-bound-report/connect-to-a-database/create-a-query-or-select-a-stored-procedure.md) page of the [Report Wizard](../../report-wizard.md) when creating a new data-bound report or when [binding an existing one to an SQL data source](../../create-reports/binding-a-report-to-data/bind-a-report-to-a-database.md). On this page, click the ![report-wizard-multi-query-page-icon-add](../../../../../images/img125532.png) button for the **Queries** category to create a new query using the Query Builder.

![eud-win-report-wizard-create-query-page](../../../../../images/img126805.png)

If you use an older Report Wizard version, the [query customization](../../report-wizard/data-bound-report/connect-to-a-database/create-a-query-or-select-a-stored-procedure-2.md) page allows you to create a single query. In this case, select the **Query** option to specify that you want to construct an SQL query and then click the **Run Query Builder** button.

![eud-win-report-wizard-old-create-query-page](../../../../../images/img126806.png)

You can also use the Query Builder to add queries to an existing SQL data source, as well as to edit existing queries. To do this, right-click the data source in the **Report Explorer** or **Field List**, and select **Manage Queries** in the context menu.

![eud-win-report-explorer-field-list-manage-queries](../../../../../images/img126807.png)

In the invoked **Manage Queries** dialog, click **Add** to add a new query. To edit an existing query, click the ellipsis button for it.

![eud-win-manage-queries-dialog](../../../../../images/img126808.png)

Finally, click the **Run Query Builder** button in the invoked **Query Editor**.

## <a name="selecttables"/>Select Tables
To add a specific data table or view to a query, drag the corresponding item from the list of available tables and drop it onto the list of data tables to be used.

![eud-win-query-builder-add-table](../../../../../images/img126809.png)

Enable check boxes for the table fields that you want to include in the query result set.

![eud-win-query-builder-select-table-fields](../../../../../images/img126810.png)

Each table provides the context menu, which allows you to rename the table or remove it from the query.

![eud-win-query-builder-table-context-menu](../../../../../images/img126811.png)

To search for a specific table or view, click the list of available tables on the left and press CTRL+F.

![eud-win-query-builder-search-tables](../../../../../images/img126812.png)

## <a name="jointables"/>Join Tables
You can join multiple tables within the same query. The Query Builder automatically highlights tables related to any of the previously added tables. Drag-and-drop a subordinate table the same way you would a principal table to include in a query and automatically create an inner join relation based on a key column.

![eud-win-query-builder-join-tables](../../../../../images/img126816.png)

Another way to join tables is to click the plus button ![QueryBuilderPlusButton](../../../../../images/img120747.png) in a row corresponding to a key column.

To customize the relationship, right-click it on the diagram and select **Edit Relation** in the invoked context menu. Use the **Join Editor** to select the join type (**Left Outer** or **Inner**), applied logical operator (**Equals to**, **Is less than**, etc.) and column key fields.

![eud-win-query-builder-join-editor](../../../../../images/img126817.png)

A left outer join returns all the values from an inner join along with all values in the "left" table that do not match to the "right" table, including rows with NULL (empty) values in the key field.

When the left outer join is selected, the relationship line displays an arrow pointing to the "right" table of the join clause.

![eud-win-query-builder-tables-left-outer-join](../../../../../images/img126818.png)

If tables don't have a relationship at the database level, you can manually join tables. In this case, when you drag-and-drop the required table onto the list of tables to be used, the **Join Editor** is automatically invoked allowing you to construct a custom **join** relationship.

After executing the query, it will return a "flat" table composed of data records selected based on the specified join options.

> [!NOTE]
> Although joining different tables within a single query may be required in some scenarios, creating [hierarchical data sources](../../report-wizard/data-bound-report/connect-to-a-database/create-a-query-or-select-a-stored-procedure.md) generally results in better performance (in general, [master-detail reports](../../create-reports/report-types/master-detail-report-(detail-report-bands).md) are generated faster than similar-looking reports created by grouping "flat" data sources).

## <a name="editparameters"/>Edit Parameters
Click the **Edit Parameters** button to invoke the **Query Parameters** dialog, which allows you to add and remove [query parameters](../../report-editing-basics/use-query-parameters.md) as well as specify parameter settings.

![eud-win-query-builder-manage-query-parameters](../../../../../images/img127045.png)

For each query parameter, the following properties are available.
* **Name** - specifies the name used to refer a parameter.
* **Type** - specifies the data type of the parameter's value.
* **Expression** - determines whether the actual parameter value is static or generated dynamically.
* **Value** - specifies the actual value of a query parameter. If the **Expression** option is enabled, the actual parameter value is produced dynamically by calculating an associated expression, which is particularly useful when you need to map the query parameter value to the value of a [report parameter](../../report-editing-basics/add-parameters-to-a-report.md).

The created parameters will be then available on the [Configure Query Parameters](../../report-wizard/data-bound-report/connect-to-a-database/configure-query-parameters.md) wizard page.

For general information on query parameters and ways of providing parameter values, see [Use Query Parameters](../../report-editing-basics/use-query-parameters.md).

## <a name="filterdata"/>Filter Data
To specify filter criteria, click the **Filter** button in the Query Builder. This invokes the **Filter Editor**, which provides the following capabilities.

![eud-win-query-builder-filter-editor](../../../../../images/img126822.png)
* **Filter Tab**
	
	The editor contains the **Filter** tab allowing you to specify filter conditions for resulting data. Filter criteria can be assigned [query parameters](../../report-editing-basics/use-query-parameters.md) or bound to [report parameters](../../report-editing-basics/add-parameters-to-a-report.md).
* **Group Filter Tab**
	
	The **Group Filter** tab allows you to specify filter conditions for grouped and aggregated data. If data is not grouped, the second tab is disabled.
* **Other Options**
	
	Using this editor, you can limit the number of resulting data rows. If data is sorted, you can specify how many rows to skip before retrieving the specified number of rows.
	
	> [!NOTE]
	> Depending on the selected data provider, it can be impossible to take into account the skip setting in the provider-specific SQL string.
	
	Another option enables you to include only distinct values into the resulting set.

## <a name="shapedata"/>Shape Data
The Query Builder displays the column list under the data source editor, which provides various shaping options.

![eud-win-query-builder-column-list](../../../../../images/img126823.png)

The following options are available.
* **Column**
	
	Specifies the selected column.
	
	You can choose a required column in the drop-down list or create a column expression by clicking the ellipsis button for the corresponding column.
	
	![eud-win-query-builder-column-expression](../../../../../images/img126824.png)
* **Table**
	
	Specifies the table containing the selected column.
	
	This option indicates **(All Tables)** if an expression is specified for the corresponding column.
* **Alias**
	
	Specifies a custom column name (alias).
	
	This option is available only for columns that are included into a query.
* **Output**
	
	Specifies whether or not the column is included into the query’s resulting set.
* **Sorting Type**
	
	Specifies whether to preserve the original order of data records within the column, or sort them (in an ascending or descending order).
	
	> [!NOTE]
	> When binding to XML files, the Query Builder does not support sorting by aggregate functions, DISTINCT and SELECT ALL statements, and custom SQL.
* **Sort Order**
	
	This option becomes available after applying sorting to the data column records.
	
	It defines the priority in which sorting is applied to multiple columns (the less this number is, the higher the priority).
	
	For example, if column **A** has the sort order set to **1** and column **B** has it set to **2**, the query will be first sorted by column **A** and then by the column **B**.
	
	Changing this setting for one column automatically updates the sort order of other columns to avoid a conflict of priorities.
* **Group By**
	
	Specifies whether or not the query’s resulting set should be grouped by this column.
* **Aggregate**
	
	Specifies whether or not the column's data records should be aggregated.
	
	The following aggregate functions are supported.
	* Count
	* Max
	* Min
	* Avg
	* Sum
	* CountDistinct
	* AvgDistinct
	* SumDistinct
	
	Applying any of these functions to a column will discard individual data records from the query result set, which will only include the aggregate function result.

> [!NOTE]
> You should apply aggregation/grouping either to all columns or to none of them.

## <a name="customsql"/>Enable Custom SQL Editing
If custom SQL editing is enabled by your software provider, the Query Builder contains the **Allow Edit SQL** check box. Selecting this option disables the visual features of the Query Builder and allows users to specify the custom SQL string manually.

![eud-win-query-builder-allow-edit-sql](../../../../../images/img126870.png)

## <a name="previewresults"/>Preview Results
You can preview the result of the query execution in the form of a tabular data sample by clicking the **Preview Results** button.

This opens the **Data Preview** window displaying the query result set limited by the first 1000 data records.

![eud-win-query-builder-data-preview](../../../../../images/img126826.png)