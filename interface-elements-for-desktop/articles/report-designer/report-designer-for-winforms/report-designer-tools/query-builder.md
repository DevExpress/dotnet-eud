---
title: Query Builder
---

# SQL Query Builder (WinForms)

The **Query Builder** allows you to construct SQL queries to retrieve data from an [SQL Database](TODO).

![Query Builder](../../../../images/winforms-sql-query-builder.png)

## Run the Query Builder

Use the [Data Source Wizard](TODO) or [Report Wizard](TODO) to bind your report to an [SQL Database](TODO). Switch to the [query customization page](TODO) and click the *Add* button in the **Queries** row.

![Data Source Wizard's Query Customization Page](../../../../images/winforms-data-source-wizard-query-customization-page.png)

## Select Tables

Drag the table that you want to add to a query from the list of available tables and drop the table onto the **Query Builder** surface.

![Query Builder: Drag and Drop a Table](../../../../images/winforms-query-builder-drag-and-drop-table.png)

To find a table by name, switch to the table list, press *CTRL+F*, and enter the table name in the editor.

![Query Builder: Find a Table by Name](../../../../images/winforms-query-builder-find-table-by-name.png)

Enable checkboxes for the table columns that you want to include in the query.

![Query Builder: Select Columns](../../../../images/winforms-query-builder-select-columns.png)

If you want to include all the columns available in the table, enable **\* (All Columns)**.

Right-click the table and select *Rename* or *Delete* to change the table's name or remove it.

![Query Builder: Rename or Delete Column](../../../../images/winforms-query-builder-delete-or-rename-column.png)

## Join Tables

You can join multiple tables within the same query. Do one of the following to add a table onto the **Query Builder** surface:

- Drag and drop a table from the table list onto the surface. 
- Double-click a table in the table list.

The table list on the left highlights all child and parent tables that are bound to the dropped table by a foreign key. 

![Query Builder: Table Added to a Query](../../../../images/winforms-query-builder-table-added-to-a-query.png)

Add required tables to the surface. The *Inner Join* relation with the previously added table is created automatically. Added tables display the green plus button for the columns that refer to other tables. You can click this icon to add a linked table to the query and create the *Inner Join* relation with this table.

![Query Builder: Create the Inner Join Relation Automatically](../../../../images/winforms-query-builder-create-inner-join-relation-automatically.png)

Right-click a relation to edit, delete, or reverse.

![Query Builder: Edit Relation](../../../../images/winforms-query-builder-edit-relation.png)

The *Edit Relation* command invokes the **Join Editor**. It allows you to specify the join type (*Inner*, *Left Outer*, *Right Outer*, or *Full Outer* ), columns by which the tables should be joined, and a logical operator (*Equal to*, *Is less than*, or others) used to compare table columns.

![Query Builder: Join Editor](../../../../images/winforms-query-builder-join-editor.png)

You can manually join tables if they are not bound by a foreign key at the database level. In this case, when you drag-and-drop a table onto the **Query Builder** surface, the **Join Editor** is automatically invoked, and this editor allows you to construct a custom join relation.

![Query Builder: Create Relation Manually in the Join Editor](../../../../images/winforms-query-builder-create-relation-manually-in-the-join-editor.png)

> [!NOTE]
> When you join multiple tables within a single SQL query, you create a flattened table composed of data records selected based on the specified join relations. You can also create [hierarchical data sources](TODO). In general, [master-detail reports](TODO) are generated faster than similar-looking reports created based on flattened data sources. If possible, use hierarchical data sources instead of flattened ones.

## Shape Data

The **Query Builder** displays a list of the query's columns at the bottom-right corner.

![Query Builder: List of Selected Table Columns](../../../../images/winforms-query-builder-list-of-selected-columns.png)

This list allows you to add new table columns to the query or shape selected table columns. The following options are available:

* **Column** - Specifies the selected column. Click the down-arrow button to display a drop-down column list and replace the column with another column. Click the ellipsis button to replace the column with an [expression](TODO).

    ![Query Builder: Specify an Expression for a Column](../../../../images/winforms-query-builder-specify-expression-for-column.png)

* **Table** - The table that contains the selected column. When you create an expression for a column, this option displays **(All Tables)**.

* **Alias** - A custom column name.

* **Output** - Specifies whether to include the column in the query's resulting set.

* **Sorting Type** - Specifies whether to keep the initial data record order (**Unsorted**) or sort the records by the column (**Ascending** or **Descending**).
	
	> [!NOTE]
	> When you bind a report to an XML file, the **Query Builder** does not support sorting by aggregate functions, the *DISTINCT* and *SELECT ALL* statements, and manual SQL editing.

* Sort Order - Defines the sort order when data is sorted by multiple columns. For example, if column **A** has the sort order set to **1** and column **B** has it set to **2**, data records are first sorted by column **A** and then by column **B**. This option is available if you enable the **Sorting Type** option.

* **Group By** - Specifies whether to group the query's resulting set by this column.

* **Aggregate** - Specifies whether to apply an aggregate function to column values. The following aggregate functions are supported:
	
	* Count
	* Max
	* Min
	* Avg
	* Sum
	* CountDistinct
	* AvgDistinct
	* SumDistinct

When you want to use the **Group By** or **Aggregate** operations, you should apply them either to all columns or none of them. When you use these operations, only the result of aggregation or grouping is included in the result set.

## Filter Data

Click the **Filter** button to invoke the **Filter Editor**.

![Query Builder: Click Filter Button](../../../../images/winforms-query-builder-click-filter-button.png)

![Query Builder: Filter Editor](../../../../images/winforms-query-builder-filter-editor.png)

The editor has the following tabs:

* **Filter Tab** - Allows you to build criteria to filter data for the report. Filter criteria can reference [query parameters](TODO), which you can also map to [report parameters](TODO).
* **Group Filter Tab** - Allows you to specify filter conditions for grouped and aggregated data. This tab is disabled if the data is not grouped.

You can also enable the **Select only** option to limit the number of resulting data records. If you enable the **Sorting Type** option for at least one column, you can specify how many data records should be skipped.

> [!NOTE]
> Some data providers do not support the skip setting in the provider-specific SQL string. If you enable the **Select only** option for such data providers, data records are skipped but the *SKIP* statement is not included in the SQL query.

The **Select only distinct values** option allows you to include only unique values into the resulting set.

## Edit Query Parameters

Click **Edit Parameters** to invoke the **Query Parameters** dialog.

![Query Builder: Click Edit Parameters Button](../../../../images/winforms-query-builder-click-edit-parameters-button.png)

This dialog allows you to add, edit, and remove [query parameters](TODO). The created parameters are available on the [Configure Query Parameters](TODO) wizard page.

![Query Builder: Query Parameters Dialog](../../../../images/winforms-query-builder-query-parameters-dialog.png)

The following properties are available for each query parameter:

* **Name** - The name by which you can reference the parameter.

* **Type** - The data type of the parameter's value.

* **Expression** - Specifies whether the parameter's value is static or generated dynamically. You can enable this option when you need to map the parameter's value to a [report parameter](TODO)'s value.

* **Value** - The parameter's value. If the **Expression** option is enabled, this value is generated dynamically based on the parameter's [expression](TODO).

Refer to the following topic for more information: [](TODO).

## Preview Results

Click the **Preview Results** button to open the **Data Preview** dialog.

![Query Builder: Preview Results Button](../../../../images/winforms-query-builder-preview-results-button.png)

The dialog displays the first 1000 rows of the query result set.

![Query Builder: Preview Results](../../../../images/winforms-query-builder-preview-results.png)

## Manage Queries

Right-click a data source in the [Report Explorer](TODO) or [Field List](TODO) and select **Manage Queries** in the context menu.

![Invoke the Manage Queries Dialog](../../../../images/winforms-invoke-manage-queries-dialog.png)

This invokes the **Manage Queries** dialog that allows you to perform operations on queries and stored procedures.

![Manage Queries Dialog](../../../../images/winforms-manage-queries-dialog.png)

### Add a New Query

Click **Add**, specify a name for the new query, and [select tables](#select-tables) that you want to include in the query.

![Manage Queries Dialog: Add a New Query](../../../../images/winforms-manage-queries-dialog-add-new-query.png)

### Copy and Remove Queries

Select a query and click the *Copy* or *Remove* icon.

![Manage Queries Dialog: Copy or Remove a Query](../../../../images/winforms-manage-queries-dialog-copy-or-remove-query.png)

### Modify Stored Procedures

Select an existing stored procedure and choose a new one that you want to include in a query.

![Manage Queries Dialog: Modify a Stored Procedure](../../../../images/winforms-manage-queries-dialog-modify-a-stored-procedure.png)

### Add a New Stored Procedure

Expand the **Add** menu and select **Stored Procedure**.

![Manage Queries Dialog: Add a Stored Procedure](../../../../images/winforms-manage-queries-dialog-add-a-stored-procedure.png)

### Rename a Query or Stored Procedure

Double-click an item in the list of queries and stored procedures and use the editor to specify a new name for this item.

![Manage Queries Dialog: Change an Item's Name](../../../../images/winforms-manage-queries-dialog-change-item-name.png)

# Query Builder (Old)

The **Query Builder** provides a visual interface for constructing SQL queries used to access database tables and views.

![query-builder](../../../../images/eurd-win-query-builder.png)

> [!NOTE]
> The Query Builder is not available for [object](data-source-wizard\connect-to-an-object-data-source.md), [Entity Framework](data-source-wizard\connect-to-an-entity-framework-data-source.md) and [Excel](data-source-wizard\connect-to-an-excel-data-source.md) data sources.

## <a name="runquerybuilder"></a>Run the Query Builder
You can invoke the **Query Builder** from the [query customization](data-source-wizard\connect-to-a-database\create-a-query-or-select-a-stored-procedure.md) page of the [Report Wizard](report-wizard.md). On this page, click the ![report-wizard-multi-query-page-icon-add](../../../../images/eurd-win-report-wizard-multi-query-page-icon-add.png) button for the **Queries** category to create a new query using the Query Builder.

![eurd-win-report-wizard-invoke-query-builder](../../../../images/eurd-win-report-wizard-invoke-query-builder.png)

You can use the Query Builder to add queries to an existing SQL data source, as well as to edit existing queries. To do this, right-click the data source in the [Report Explorer](ui-panels\report-explorer.md) or [Field List](ui-panels\field-list.md), and select **Manage Queries...** in the context menu.

![report-explorer-field-list-manage-queries](../../../../images/eurd-win-report-explorer-field-list-manage-queries.png)

In the invoked **Manage Queries** dialog, click **Add** to add a new query. To edit an existing query, click the ellipsis button for it.

![query-designer-query-collection-editor](../../../../images/eurd-win-query-designer-query-collection-editor.png)

Finally, click the **Run Query Builder...** button in the invoked **Query Editor**.

## <a name="selecttables"></a>Select Tables
You can add a specific data table or view to a query by dragging the corresponding item from the list of available tables and dropping it onto the list of data tables to be used.

![query-builder-diagram-drop-table](../../../../images/qeurd-win-uery-builder-diagram-drop-table.png)

Enable check boxes for the table fields that you want to include in the query result set.

![query-builder-diagram-select-fields](../../../../images/eurd-win-query-builder-diagram-select-fields.png)

Each table provides the context menu, which allows you to rename the table or remove it from the query.

![query-builder-diagram-table-context-menu](../../../../images/eurd-win-query-builder-diagram-table-context-menu.png)

Click the list of available tables on the left and press CTRL+F to search for a specific table or view.

![query-builder-search-table](../../../../images/eurd-win-query-builder-search-table.png)

## <a name="jointables"></a>Join Tables
You can join multiple tables within the same query. The Query Builder automatically highlights tables related to any of the previously added tables. Drag-and-drop a subordinate table in the same way you added a main table to include it in a query and automatically create an inner join relation based on a key column.

![query-builder-diagram-join-tables](../../../../images/eurd-win-query-builder-diagram-join-tables.png)

Alternatively, you can join tables by clicking the plus button ![QueryBuilderPlusButton](../../../../images/eurd-win-query-builder-plus-button.png) in a row corresponding to a key column.

You can customize the relationship by right-clicking it on the diagram and selecting **Edit Relation** in the invoked context menu. Use the **Join Editor** to select the join type (**Left Outer** or **Inner**), apply a logical operator (**Equals to**, **Is less than**, etc.) and column key fields.

![query-builder-diagram-join-editor](../../../../images/eurd-win-query-builder-diagram-join-editor.png)

A left outer join returns an inner join’s values, along with all the values in the "left" table that do not match the "right" table, including rows with NULL (empty) values in the key field.

When the left outer join is selected, the relationship line displays an arrow pointing to the "right" table.

![query-builder-diagram-left-outer-join](../../../../images/eurd-win-query-builder-diagram-left-outer-join.png)

You can manually join tables if they do not have a relationship at the database level. In this case, when you drag-and-drop a table onto the list of tables, the **Join Editor** is automatically invoked allowing you to construct a custom **join** relationship.

After executing the query, it returns a "flat" table composed of data records selected based on the specified join options.

> [!NOTE]
> Although joining different tables within a single query may be required in some scenarios, creating [hierarchical data sources](data-source-wizard\connect-to-a-database\create-a-query-or-select-a-stored-procedure.md) generally results in better performance (in general, [master-detail reports](..\create-reports\master-detail-reports-with-detail-report-bands.md) are generated faster than similar-looking reports created by grouping "flat" data sources).

## <a name="editparameters"></a>Edit Parameters
Click the **Edit Parameters** button to invoke the **Query Parameters** dialog, which allows you to add and remove [query parameters](../bind-to-data/specify-query-parameters.md) as well as specify parameter settings.

![query-builder-diagram-query-parameters](../../../../images/eurd-win-query-builder-diagram-query-parameters.png)

For each query parameter, the following properties are available.

* **Name** - specifies the name used to refer a parameter.
* **Type** - specifies the data type of the parameter's value.
* **Expression** - determines whether the actual parameter value is static or generated dynamically.
* **Value** - specifies the actual value of a query parameter. If the **Expression** option is enabled, the actual parameter value is produced dynamically by calculating an associated [expression](../use-expressions.md), which is particularly useful when you need to map the query parameter value to the value of a [report parameter](..\shape-report-data\use-report-parameters.md).

The created parameters will be then available on the [Configure Query Parameters](data-source-wizard/connect-to-a-database/configure-query-parameters.md) wizard page.

For general information on query parameters and ways of providing parameter values, see [Specify Query Parameters](../bind-to-data/specify-query-parameters.md).

## <a name="filterdata"></a>Filter Data
To specify filter criteria, click the **Filter...** button in the Query Builder. This invokes the **Filter Editor**, which provides the following capabilities.

![query-designer-filter](../../../../images/eurd-win-query-designer-filter.png)

* **Filter Tab**
	
	The editor contains the **Filter** tab allowing you to specify filter conditions for resulting data. Filter criteria can be assigned [query parameters](data-source-wizard/connect-to-a-database/configure-query-parameters.md) or bound to [report parameters](..\shape-report-data\use-report-parameters.md).
* **Group Filter Tab**
	
	The **Group Filter** tab allows you to specify filter conditions for grouped and aggregated data. If data is not grouped, the second tab is disabled.
* **Other Options**
	
	Using this editor, you can limit the number of resulting data rows. If data is sorted, you can specify how many rows to skip before retrieving the specified number of rows.
	
	> [!NOTE]
	> Depending on the selected data provider, it can be impossible to take into account the skip setting in the provider-specific SQL string.
	
	Another option enables you to include only distinct values into the resulting set.

## <a name="shapedata"></a>Shape Data
The Query Builder displays the column list under the data source editor, which provides various shaping options:

![query-builder-column-list-shaping-data](../../../../images/eurd-win-query-builder-column-list-shaping-data.png)

* **Column**
	
	Specifies the selected column.
	
	You can choose a column from the drop-down list or create a column expression by clicking the corresponding column's ellipsis button.
	
	![query-builder-column-expression](../../../../images/eurd-win-query-builder-column-expression.png)
* **Table**
	
	Specifies the table containing the selected column.
	
	This option indicates **(All Tables)** if you created an expression for the corresponding column.
* **Alias**
	
	Specifies a custom column name (alias).
	
	This option is available only for columns that you included in a query.
* **Output**
	
	Specifies whether to include the column in the query's resulting set.
* **Sorting Type**
	
	Specifies whether to preserve the original data record order within the column or sort them (ascending or descending).
	
	> [!NOTE]
	> When binding to XML files, the Query Builder does not support sorting by aggregate functions, DISTINCT and SELECT ALL statements, and custom SQL.
* **Sort Order**
	
	This option becomes available after applying sorting to the data column records.
	
	It defines the priority in which sorting is applied to multiple columns (a lower number has a higher priority).
	
	For example, if column **A** has the sort order set to **1** and column **B** has it set to **2**, the query is first sorted by column **A** and then by the column **B**.
	
	Changing this setting for one column automatically updates other columns’ sorting order to avoid conflicting priorities.
* **Group By**
	
	Specifies whether to group the query's resulting set by this column.
* **Aggregate**
	
	Specifies whether to aggregate the column's data records.
	
	The following aggregate functions are supported:
	
	* Count
	* Max
	* Min
	* Avg
	* Sum
	* CountDistinct
	* AvgDistinct
	* SumDistinct
	
	Applying any of these functions to a column discards individual data records from the query result set, which only includes the aggregate function result.

> [!NOTE]
> You should apply aggregation/grouping to either all columns or none of them.

## <a name="previewresults"></a>Preview Results
You can preview the query execution's result in a tabular form by clicking the **Preview Results** button.

This opens the **Data Preview** window displaying the query result set (limited to the first 1000 data records).

![query-designer-preview](../../../../images/eurd-win-query-designer-preview.png)