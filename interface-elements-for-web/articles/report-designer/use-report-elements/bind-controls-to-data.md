---
title: Bind Report Controls to Data
author: Anna Vekhina
---
# Bind Report Controls to Data

You can use the following approaches to include a data source's information in your report:

* [Use the Field List](#use-the-field-list)
* [Use the Properties Panel](#use-the-properties-panel)

## Use the Field List

After you [bind your report to data](../bind-to-data.md), the [Field List](../report-designer-tools/ui-panels/field-list.md) panel displays the data source's hierarchy and provides access to the available data fields. 

Drop a data field from this panel onto a report's surface to create a new report control bound to the corresponding field.

![](../../../images/eurd-web-field-list-drop-fields.png)

Drop a data field onto an existing control to bind this control to the corresponding field.

![](../../../images/eurd-web-field-list-drop-field-to-control.png)

You can also drop an entire data table onto a report to create a [Table](../use-report-elements/use-tables.md) control with its cells bound to the corresponding data table fields. 

![](../../../images/eurd-web-field-list-drop-table.png)

To select multiple fields in the Field List, hold CTRL or SHIFT and click the fields. Drop these fields onto a report to create a new table.

![](../../../images/eurd-web-list-drop-multiple-fields.png)

## Use the Properties Panel

Select a report control and switch to the [Properties](../report-designer-tools/ui-panels/properties-panel.md) panel. Click the **Text** property's marker and select **Text Expression** from the popup menu. Select a data field or construct a binding [expression](../use-expressions/expression-language.md) in the invoked [Expression Editor](../report-designer-tools/expression-editor.md).

![](../../../images/eurd-web-expression-editor.png)

You can use the same approach to specify expressions for all the control properties. See [Shape Report Data](../shape-report-data.md) for more tutorials.
