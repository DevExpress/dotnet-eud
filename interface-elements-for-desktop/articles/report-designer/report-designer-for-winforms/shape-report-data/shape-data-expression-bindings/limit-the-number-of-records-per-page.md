---
title: Limit the Number of Records per Page
author: Anna Gubareva
---
# Limit the Number of Records per Page

This document describes how to specify the number of data source records displayed on report pages.

> [!Warning]
> Use the approach below if expression bindings **are enabled** in the Report Designer (the [Property Grid](../../report-designer-tools/ui-panels/property-grid.md) provides the **Expressions** ![](../../../../../images/eurd-win-property-grid-expressions-icon.png) tab ).
>
> See [Limit the Number of Records per Page](../shape-data-data-bindings/limit-the-number-of-records-per-page.md) if expression bindings **are not enabled** in the Report Designer (the [Property Grid](../../report-designer-tools/ui-panels/property-grid.md) does not provide the **Expressions** ![](../../../../../images/eurd-win-property-grid-expressions-icon.png) tab).

After you [bound your report to data](../../bind-to-data.md) and provided content to the report's [Detail band](../../introduction-to-banded-reports.md), you can limit the number of records each report page displays. This example demonstrates how to pass the required record count as a parameter value.

1. Switch to the [Field List](../../report-designer-tools/ui-panels/field-list.md), right-click the **Parameters** section and add a new report parameter.
	
	![](../../../../../images/eurd-win-shaping-filter-add-parameter.png)

2. Specify the parameter's description displayed in Print Preview and set its type to **Number (Integer)**.
	
	![](../../../../../images/eurd-win-shaping-limit-parameter-settings.png)

3. Drop a [Page Break](../../use-report-elements/use-basic-report-controls/page-break.md) control onto the report's detail band and switch to the [Property Grid](../../report-designer-tools/ui-panels/property-grid.md). Switch to its **Expressions** tab and click the **Visible** property's ellipsis button .
	
	![](../../../../../images/eurd-win-shaping-page-break-visible-property.png)

4. In the invoked **Expression Editor**, specify the required [expression](../../use-expressions.md).
	
	![](../../../../../images/eurd-win-shaping-page-break-visible-expression.png)
	
	For example:
	
	**([DataSource.CurrentRowIndex] % [Parameters.parameter1] == 0) And ([DataSource.CurrentRowIndex] !=0)**

When switching to [Print Preview](../../preview-print-and-export-reports.md), you can specify how many rows each report page should display by entering the corresponding parameter value:

![](../../../../../images/eurd-win-shaping-limit-rows-result.png)