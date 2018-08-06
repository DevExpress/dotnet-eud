---
title: Format Data
author: Anna Gubareva
---
# Format Data

This document demonstrates how to specify value formatting for report elements (for instance, format numeric values as a currency or apply a percent format).

> [!Warning]
> Use the approach below if expression bindings **are not enabled** in the Report Designer (the [Property Grid](../../report-designer-tools/ui-panels/property-grid.md) does not provide the **Expressions** ![](../../../../../images/eurd-win-property-grid-expressions-icon.png) tab ).
>
> See [Format Data](../shape-data-expression-bindings/format-data.md) if expression bindings **are enabled** in the Report Designer (the [Property Grid](../../report-designer-tools/ui-panels/property-grid.md) provides the **Expressions** ![](../../../../../images/eurd-win-property-grid-expressions-icon.png) tab).


After you [bound your report to data](../../bind-to-data.md) and specified a bound data field in a report control's **Data Binding** property, you can format data values in a report.

1. Invoke the control's smart tag and click the **Format String** property's ellipsis button.
	
	![](../../../../../images/eurd-win-shaping-legacy-format-string-property.png)

2. This invokes the **Format String Editor** where you can specify the required format.
	
	![](../../../../../images/eurd-win-format-string-editor-currency.png)


When switching to [Print Preview](../../preview-print-and-export-reports.md), you can view the report control displaying values with the specified format.

![](../../../../../images/eurd-win-format-data-result.png)


You can use the control's **Xlsx Format String** property to assign a native Excel format that is used for exporting reports to [XLSX](../../../../print-preview/print-preview-for-winforms/exporting/xlsx-specific-export-options.md).