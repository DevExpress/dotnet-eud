---
title: Passing Parameter Values
---
# Passing Parameter Values
In this topic, it describes how to pass the created dashboard parameter to the dashboard. For instance, you can include a dashboard parameter to a _WHERE_ clause of the SQL query or you can filter a dashboard dynamically according to the required parameter value(s).

The created dashboard parameter can be used in the following scenarios:
* [SQL Queries](#query)
* [Filtering](#filtering)
* [Conditional Formatting](#formatrules)
* [Calculated Fields](#calculatedfields)
* [Window Calculations](#windowscalculations)

## <a name="query"/>SQL Queries
The Web Dashboard provides the capability to bind a dashboard parameter and the existing [SQL query](../../../../../dashboard-for-web/articles/web-dashboard-designer-mode/providing-data/working-with-sql-data-sources/pass-query-parameters.md)/[stored procedure](../../../../../dashboard-for-web/articles/web-dashboard-designer-mode/providing-data/working-with-sql-data-sources/stored-procedures.md) parameter. This can be useful when you need to [filter the SQL query](../../../../../dashboard-for-web/articles/web-dashboard-designer-mode/providing-data/working-with-sql-data-sources/filter-queries.md) dynamically by including the parameter value in the _WHERE_ clause.

![wdd-configure-query-param-page2](../../../../images/Img124955.png)

To bind a dashboard parameter to an SQL query/stored procedure parameter in the [Dashboard Data Source Wizard](../../../../../dashboard-for-web/articles/web-dashboard-designer-mode/providing-data/working-with-sql-data-sources/dashboard-data-source-wizard.md), do the following:
* Select the existing query/stored procedure parameter or create a new query parameter using the **Add** button.
* Set the **Expression** as a parameter value and click the ellipsis button to invoke the Expression Editor for this parameter.
* In the Expression Editor add the required dashboard parameter from the Parameters column.

## <a name="filtering"/>Filtering
You can filter the specified [query](../../../../../dashboard-for-web/articles/web-dashboard-designer-mode/providing-data/working-with-sql-data-sources/filter-queries.md) of the SQL Data Source, the entire [Excel Data Source](../../../../../dashboard-for-web/articles/web-dashboard-designer-mode/providing-data/filter-data-sources.md)/[Object Data Source](../../../../../dashboard-for-web/articles/web-dashboard-designer-mode/providing-data/filter-data-sources.md) or [apply filtering](../../../../../dashboard-for-web/articles/web-dashboard-designer-mode/data-shaping/filtering.md) to a specific dashboard item according to the current parameter value(s) using the Filter Editor.

In the Filter Editor, you can compare a field value with different objects such as static values, values of another field or parameter values. To switch between values, click a down arrow glyph in the operand value placeholder to expand the list of available objects. Select the **Parameter** object to compare a field value with a parameter value.

![wdd-filter-editor-change-object](../../../../images/Img126182.png)

Then, click the operand value to invoke the list of available parameters and select the existing parameter or create a new one.

![wdd-parameters-filtering](../../../../images/Img126539.png)

## <a name="formatrules"/>Conditional Formatting
You can apply conditional formatting to a specific dashboard item according to the current parameter value when creating the **Expression** [format condition](../../../../../dashboard-for-web/articles/web-dashboard-designer-mode/appearance-customization/conditional-formatting.md). Use this capability to format dashboard item elements dynamically, depending on the current parameter value.

![wdd-parameters-conditional-formatting](../../../../images/Img128229.png)

To switch between values, click the down arrow glyph in the operand value placeholder to expand the list of available objects and select the **Parameter** object to create a format rule with a parameter.

## <a name="calculatedfields"/>Calculated Fields
You can use parameters when constructing [expressions](../../../../../dashboard-for-web/articles/web-dashboard-designer-mode/providing-data/calculated-fields.md) for [calculated fields](../../../../../dashboard-for-web/articles/web-dashboard-designer-mode/providing-data/calculated-fields.md). This allows you to evaluate values of the calculated field dynamically depending on the current parameter value.

![wdd-parameters-calculated-field](../../../../images/Img126509.png)

To include a parameter in the expression, double-click the required parameter in the Fields pane.

## <a name="windowscalculations"/>Window Calculations
You can use parameters when customizing expressions for [window calculations](../../../../../dashboard-for-web/articles/web-dashboard-designer-mode/data-analysis/calculations.md). This allows you to apply a calculation dynamically, depending on the current parameter value.

![wdd-parameters-window-calculations](../../../../images/Img126562.png)

To create the calculation with a parameter, select the **Custom** calculation and click **Edit**. In the invoked Expression Editor double-click the required parameter.