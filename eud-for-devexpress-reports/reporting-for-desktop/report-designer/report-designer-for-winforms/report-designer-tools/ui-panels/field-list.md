---
title: Field List
owner: Anna Gubareva
seealso: []
---
# Field List

This panel displays the schemas of a report’s data sources.

![Field List](../../../../images/eurd-win-field-list.png)

Right-click a data source to access its settings. For instance, you can add the data source to the [Report Gallery](report-gallery.md) to reuse it in other reports.

![Field List - Add Data Source to Report Gallery](../../../../images/eurd-win-field-list-data-source-add-to-gallery.png)

The Field List allows you to do the following:

## Search fields

Enter a search string in the search box. The Field List filters fields and tables to match the entered string.

![Field List - Search](../../../../images/eurd-win-field-list-search.png)

## Bind controls to data

Drop a field onto a report's surface to create a new report control bound to this field.

![Field List - Drop Field Onto the Surface](../../../..//images/eurd-win-field-list-drop-fields.png)

Drop a field onto an existing report control to bind this control to the field.

![Field List - Drop Field Onto a Control](../../../../images/eurd-win-field-list-drop-field-to-control.png)

Hold the CTRL key when you drop a field on top of an existing control to keep the control's current data binding setting. In this case, a new report control is created.

![Field List - Drop Field Onto a Control and Keep Binding](../../../../images/eurd-win-field-list-avoid-data-binding.png)

**Select which control to create**

Do any of the following:

* Hold the SHIFT key when you drop a data field onto the report surface.
* Right-click a data field and drop it onto the report surface.

This invokes a context menu where you can select which control to create.

![Field List - Select Which Control to Create](../../../../images/eurd-win-fieldlist-create-specific-contols.png)

## Create tables

Drop an entire data table onto the report to create a report table with columns bound to the data table's fields.

![Field List - Drop Table](../../../../images/eurd-win-field-list-drop-table.png)

Hold the CTRL or SHIFT key to select multiple data fields in the Field List. Drop these fields onto the report to create a report table that only has the selected fields.

![Field List - Select Specific Fields](../../../../images/eurd-win-list-drop-multiple-fields.png)

Hold the SHIFT key when you drop the selected fields onto the report to only create column headers. This creates a new table whose cells display the selected field names. Alternatively, you can drag and drop fields with the right mouse button.

![Field List - Create Column Headers](../../../../images/eurd-win-field-list-multi-select-bound-table-cells.png)

## Data shaping operations

The Field List can help you do the following:

* Add [calculated fields](../../shape-report-data/use-calculated-fields/calculated-fields-overview.md) to data tables.

	![Field List - Add Calculated Field](../../../../images/eurd-win-field-list-add-calculated-field.png)

* Add [report parameters](../../use-report-parameters.md) or change existing parameters.

	![Field List - Add Report Parameter](../../../../images/eurd-winield-list-add-report-parameter.png)
