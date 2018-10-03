---
title: Conditionally Filter Report Data
author: Anna Vekhina
---
# Conditionally Filter Report Data

This document describes how to filter a report's data based on a specific condition.

> [!Warning]
> Use the approach below if expression bindings **are enabled** in the Report Designer (the Designer provides the [Expressions](../../report-designer-tools/ui-panels/expressions-panel.md) panel).
>
> See [Conditionally Filter Report Data](../shape-data-data-bindings/conditionally-filter-report-data.md) if expression bindings **are not enabled** in the Report Designer (the Designer does not provide the [Expressions](../../report-designer-tools/ui-panels/expressions-panel.md) panel).

1. Switch to the [Field List](../../report-designer-tools/ui-panels/field-list.md) panel, select the **Parameters** node and click **Add parameter**.
	
	![](../../../../images/eurd-web-shaping-filter-add-parameter.png)

2. Specify the parameter's description in Print Preview and set its type to **Number (Integer)**.
	
	![](../../../../images/eurd-web-shaping-filter-parameter-settings.png)

3. Select the report's detail band, switch it to the [Expressions](../../report-designer-tools/ui-panels/expressions-panel.md) panel and click the **Visible** property's ellipsis button. In the invoked **Expression Editor**, specify the required visibility condition. For example:
	
	![](../../../../images/eurd-web-shaping-formatting-rule-filter-condition.png)
	
	The expression above makes the **Visible** property return **True** or **False** depending on whether the field value is below the specified parameter value.

Switch to [Print Preview](../../preview-print-and-export-reports.md) to see the result. 

![](../../../../images/eurd-web-shaping-filter-result.png)