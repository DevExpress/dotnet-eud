---
title: Field List
author: Anna Gubareva
legacyId: 113890
---
# Field List
This document describes the **Field List** panel that enables you to explore and manage report data sources and parameters.

![web-designer-field-list](../../../images/img24630.png)

This document consists of the following sections.
* [Manage Report Data Sources](#datasources)
* [Manage Report Parameters](#reportparameters)

## <a name="datasources"/>Manage Report Data Sources
The Field List lists available report data sources and displays their structure. Dragging a field from the Field List onto the [Design Surface](design-surface.md) creates a new [Label](../report-elements/report-controls.md) bound to that data field.

![web-designer-field-list-adding-bound-control](../../../images/img24631.png)

The following actions are available in the Field List for data source customization.

| Button | Description |
|---|---|
| ![web-designer-field-list-data-source-delete](../../../images/img125719.png) | Removes the selected data source. |
| ![web-designer-field-list-data-source-edit-relationships](../../../images/img125720.png) | Invokes the [Master-Detail Relation Editor](master-detail-relation-editor.md). |
| ![web-designer-field-list-data-source-add-query](../../../images/img125721.png) | Invokes the [Create a Query or Select a Stored Procedure](../wizards/sql-data-source-wizard/editing-an-existing-data-source/create-a-query-or-select-a-stored-procedure.md) wizard page. |
| ![web-designer-field-list-data-source-add-calculated-field](../../../images/img125722.png) | Adds a new [calculated field](../creating-reports/providing-data/calculated-fields.md) to the data source. |

The following actions are available for query customization.

| Button | Description |
|---|---|
| ![web-designer-field-list-data-source-delete](../../../images/img125719.png) | Removes the selected query. |
| ![web-designer-field-list-data-source-add-query](../../../images/img125721.png) | Invokes the [Create a Query or Select a Stored Procedure](../wizards/sql-data-source-wizard/editing-an-existing-data-source/create-a-query-or-select-a-stored-procedure.md) wizard page. |
| ![web-designer-field-list-data-source-add-calculated-field](../../../images/img125722.png) | Adds a new [calculated field](../creating-reports/providing-data/calculated-fields.md) to the query. |

## <a name="reportparameters"/>Manage Report Parameters
To access the collection of [report parameters](../creating-reports/providing-data/report-parameters.md), expand the corresponding category in the Field List.

![web-designer-field-list-report-parameters](../../../images/img125916.png)

The following actions are available for parameter customization.

| Button | Description |
|---|---|
| ![web-designer-report-wizard-button-query-add](../../../images/img125709.png) | Creates a new report parameter. |
| ![web-designer-field-list-data-source-delete](../../../images/img125719.png) | Removes the selected parameter. |
| ![web-designer-field-list-data-source-edit-relationships](../../../images/img125720.png) | Enables customization of the selected parameter. |

For more information on report parameters, see [Report Parameters](../creating-reports/providing-data/report-parameters.md).