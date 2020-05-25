---
title: Query Parameters
author: Anna Vekhina
---
# Query Parameters

This document provides information on query parameters and describes how to use parameterized SQL queries to filter data at data source level.

## Query Parameters Overview
A query parameter holds an external value that is inserted into an SQL statement before query execution. This value can be static or an associated expression can generate it dynamically.

The query parameter value is inserted into the resulting SQL query string in the "\@QueryParameterName" placeholder's position.

Query parameters are used in the following scenarios:

* When filtering report data at the data source level using the [Query Builder](../../report-designer-tools/query-builder.md).
	
	The Query Builder helps you construct SQL queries when creating a new data-bound report or [binding an existing report to an SQL data source](../../bind-to-data/bind-a-report-to-a-database.md),
	
	![](../../../../images/eurd-web-query-parameters-create-query.png)
	
	... or when adding queries to an existing SQL data source or editing existing queries.
	
	![](../../../../images/eurd-web-query-parameters-add-edit-queries.png)
	
	You can filter the constructed queries using query parameters. Expand the **Parameters** section in the **Query Builder** to add a new query parameter.
	
	![](../../../../images/eurd-web-query-parameters-add-in-query-builder.png)
	
	Expand the **Query Properties** section and click the **Filter** property's ellipsis button to invoke the Filter Editor and filter data using the created query parameters.
	
	![](../../../../images/eurd-web-query-parameters-in-filter-editor.png)
	
	The criteria based on the specified query parameters are added as an SQL statement's WHERE part.
	
* When binding a report to a stored procedure provided by an SQL data source.
	
	The Data Source Wizard includes the following page. 
    
    ![](../../../../images/eurd-web-query-parameters-select-stored-procedure.png)
    
    If you select a stored procedure, the wizard creates a query parameter for each procedure parameter and allows you to configure the query parameters in the next **Configure query parameters** page.
	
	![](../../../../images/eurd-web-query-parameters-for-stored-procedure.png)

## Configure Query Parameters
The following properties are available for each query parameter:

* **Name** - specifies the parameter's name.
* **Type** - specifies the parameter value's data type.
* **Expression** - determines whether the actual parameter value is static or generated dynamically.
* **Value** - determines the query parameter's actual value. If the **Expression** option is enabled, the actual parameter value is produced dynamically by calculating an associated expression. This is useful when you map the query parameter value to the [report parameter](parameters-overview.md) value. Refer to the next document section for more information.

## Provide the Query Parameter Value
Below, you can see how a value is specified for a query parameter within the Data Source Wizard's page. You can also specify query parameter values in the Report Wizard or the Query Parameters dialog in the same way.

* **Specifying a static value**
	
	Choose a query parameter's value type and set a static value to the **Value** property according to the selected type.
	
	![](../../../../images/eurd-web-query-parameters-static-value.png)

* **Providing a dynamic value**
	
	Create a complex expression by expanding the **Type** property's drop-down list and selecting **Expression**.
		
	![](../../../../images/eurd-web-query-parameters-dynamic-expression.png)
		
	Click the **Value** property's ellipsis button and construct an expression in the invoked [Expression Editor](../../report-designer-tools/expression-editor.md). You can map a report parameter that already exists in a report to a query parameter.
		
	![](../../../../images/eurd-web-query-parameters-expression-editor.png)

## Pass a Multi-Value Parameter Value to a Query
You can map [multi-value parameters](multi-value-and-cascading-parameters.md) to query parameters. 
For instance, the following query selects the orders whose IDs can be found within the values the _\@OrderID_ query parameter provides.

![](../../../../images/eurd-web-query-parameters-map-to-multi-value-parameter.png)

## Pass a Multi-Value Report Parameter Value to a Stored Procedure
You cannot pass a [multi-value parameter](multi-value-and-cascading-parameters.md) value to a stored procedure directly. Use one of the following expression functions:

* Use the [Join() expression function](../../use-expressions/expression-syntax.md) to convert the array of parameter values to a string if you use MS SQL Server, MySQL or Oracle database systems.

	![](../../../../images/eurd-web-query-parameters-join-expression-function.png)

* Use the [CreateTable() expression function](../../use-expressions/expression-syntax.md) to prepare a table using values of several multi-value parameters.

	![](../../../../images/eurd-web-query-parameters-createtable-expression-function.png)