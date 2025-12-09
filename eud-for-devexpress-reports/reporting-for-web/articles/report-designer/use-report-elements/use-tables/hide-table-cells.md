---
title: Hide Table Cells
author: Anna Vekhina
---
# Hide Table Cells

You can hide a specific table cell conditionally, for instance, based on a [report parameter](../../use-report-parameters.md) value.

Select the **Parameters** node in the [Field List](../../report-designer-tools/ui-panels/field-list.md) and click the **Add parameter** button.

![](../../../../images/eurd-web-create-parameter-to-hide-table-cells.png)

Click the **Edit** button to expand the property list and specify the parameter's name and description for Print Preview, and set the type to **Boolean**.

![](../../../../images/eurd-web-parameter-settings-to-hide-table-cells.png)

Open the [Expressions](../../../report-designer/report-designer-tools/ui-panels/expressions-panel.md) panel and specify an [expression](../../shape-report-data/specify-conditions-for-report-elements/conditionally-supress-controls.md) for the cell's **Visible** property to define a logical condition for displaying or hiding this cell.

The image below demonstrates how to provide the visibility expression for the cell bound to the **CategoryID** field. For a report to display correctly, you should specify the same expression for the cell that displays the field caption in the Page Header.

![](../../../../images/eurd-web-hide-table-cell-using-expression.png)

The **Process Hidden Cell Mode** property allows you to define how to distribute the remaining space between the table's visible cells.


![](../../../../images/eurd-web-table-process-hidden-cell-mode.png)

The image below illustrates how the original table looks like:

![](../../../../images/eurd-web-table-hidden-cell-mode-initial-layout.png)

The following modes are available to process hidden cells:

* **StretchPreviousCell** - A cell to the left of the hidden cell is stretched to occupy the available space. If the hidden cell is the first in the row, the next cell is stretched.

    ![](../../../../images/eurd-web-table-hidden-cell-mode-stretch-previous-cell.png)

* **StretchNextCell** - A cell to the right of the hidden cell is stretched to occupy the available space. If the hidden cell is the last in the row, the previous cell is stretched.

    ![](../../../../images/eurd-web-table-hidden-cell-mode-stretch-next-cell.png)

* **ResizeCellsEqually** - All visible cells are resized to divide the space that a hidden cell reserved equally.

    ![](../../../../images/eurd-web-table-hidden-cell-mode-resize-cells-equally.png)

* **ResizeCellsProportionally** - All visible cells are resized to proportionally divide the space that a hidden cell reserved based on their weights in the whole table width.

    ![](../../../../images/eurd-web-table-hidden-cell-mode-resize-cells-proportionally.png)

* **DecreaseTableWidth** - The table width is decreased, and visible cells are shifted to a hidden cell's location without changing their size.

    ![](../../../../images/eurd-web-table-hidden-cell-mode-descrease-table-width.png)

* **LeaveEmptySpace** (the default mode) - A space remains at a hidden cell's location, and other cells are not affected.

    ![](../../../../images/eurd-web-table-hidden-cell-mode-leave-empty-space.png)

