---
title: Report Explorer
---
# Report Explorer

The **Report Explorer** shows a report structure in a tree-like form and provides access to components assigned to a report (such as its data sources).

![RD_Elements_ReportExplorer](../../../images/eurd-win-report-explorer.png)

## Search fields

Enter a search string in the search box. The Report Explorer filters report elements, styles, and data sources to match the entered string.

![Report Explorer - Search](../../../images/eurd-win-field-list-search.png)
## Report Bands and Controls

Bands and controls are listed in a hierarchical tree-like structure.

Select an element and invoke the context menu to access the available actions.

![eurd-win-report-explorer-context-menu](../../../images/eurd-win-report-explorer-context-menu.png)

Select an element and navigate to the **Property Grid** to edit the element's options.

![design-time-report-explorer-right-click](../../../images/eurd-win-report-explorer-properties.png)

Data-bound controls are marked with a yellow database icon.

![eurd-win-report-explorer-bound-controls](../../../images/eurd-win-report-explorer-bound-controls.png)

Right-click an element in the **Report Explorer** and select **Navigate To Control** from the context menu to move the design surface's visible area to this element.

![eurd-win-navigate-to-control](../../../images/eurd-win-navigate-to-control.gif)

Drag elements to change their location.

![eurd-win-move-controls](../../../images/eurd-win-move-controls.gif)

Check the following topics for more information on how to manipulate report elements:

* [Manipulate Bands](../../introduction-to-banded-reports.md#access-the-bands-collection)
* [Manipulate Report Controls](../../use-report-elements/manipulate-report-elements/move-and-resize-report-elements.md)
* [Manipulate Table Elements](../../use-report-elements/use-tables/manipulate-table-elements.md#reorder-table-rows-and-cells)

## Report Styles

Drop a style onto a report element. This applies the selected style to the element.

![design-time-drag-style](../../../images/eurd-win-drag-style.gif)

You can select all report elements with a specific style.

![design-time-report-explorer-style-select-controls](../../../images/eurd-win-report-explorer-style-select-controls.png)

## Report Data Sources

The Data Sources node lists all [data sources](../../bind-to-data.md) configured for the report. Right-click a data source to customize its settings or add it to the [Report Gallery](report-gallery.md).

![design-time-report-explorer-data-source-add-to-gallery](../../../images/eurd-win-report-explorer-data-source-add-to-gallery.png)

You can convert a **Data Set** data source to an SQL data source. Right-click the Data Set and select **Convert to SqlDataSource** from the context menu. Click **Yes** in the invoked dialog to confirm the selected action.

![design-time-report-explorer-data-source-convert-data-set](../../../images/eurd-win-report-explorer-data-source-convert-data-set.png)
