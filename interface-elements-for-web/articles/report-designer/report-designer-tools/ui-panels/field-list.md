---
title: Field List
author: Anna Vekhina
---

# Field List

The **Field List** displays the schema of a report's data sources. This panel enables you to manage report data sources and parameters, add calculated fields and create bound report controls.

## Manage Report Data Sources

The Field List shows available report data sources and their structure.

![](../../../../images/eurd-web-fieldlist-manage-data-source.png)

The following actions are available in the Field List for data source customization:

| Button | Description |
|---|---|
| ![](../../../../images/eurd-web-fieldlist-add-data-source-button.png) | Invokes a list of default data sources that you can add to a report. |
| ![](../../../../images/eurd-web-fieldlist-data-source-delete.png) | Removes the selected data source. |
| ![](../../../../images/eurd-web-fieldlist-data-source-edit-relationships.png) | Invokes the [Master-Detail Relation Editor](../master-detail-relation-editor.md). |
| ![](../../../../images/eurd-web-fieldlist-data-source-add-query.png) | Invokes the [Create a Query or Select a Stored Procedure](../data-source-wizard\specify-data-source-settings-database.md) wizard page. |

The following actions are available for query customization:

| Button | Description |
|---|---|
| ![](../../../../images/eurd-web-fieldlist-data-source-delete.png) | Removes the selected query. |
| ![](../../../../images/eurd-web-fieldlist-data-source-edit-relationships.png) | Invokes the [Create a Query or Select a Stored Procedure](../data-source-wizard\specify-data-source-settings-database.md) wizard page. |

## Bind controls to data

Dropping a field onto a report's surface creates a new report control bound to a corresponding field.

![](../../../../images/eurd-web-field-list-drop-fields.png)

Dropping a field onto an existing control binds this control to a corresponding field.

![](../../../../images/eurd-web-field-list-drop-field-to-control.png)

## Create tables

Dropping an entire data table onto a report creates a table with its columns bound to fields contained in the data table.

![](../../../../images/eurd-web-field-list-drop-table.png)

To select multiple fields, click them with holding the CTRL or SHIFT key. Dropping these fields onto a report creates a new table with its cells bound to the corresponding fields.

![](../../../../images/eurd-web-list-drop-multiple-fields.png)

## Data shaping operations

In addition, the Field List can help you solve the following tasks:

* Add [calculated fields](../../shape-report-data/use-calculated-fields/calculated-fields-overview.md) to data columns for performing various calculations in a report.
	
	![](../../../../images/eurd-web-add-calculated-field.png)
* Manage the collection of [report parameters](../../shape-report-data/use-report-parameters.md).
	
	![](../../../../images/eurd-web-parameters-add-parameter-via-field-list.png)