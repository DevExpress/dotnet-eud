---
title: Design Surface
author: Anna Vekhina
---
# Design Surface

The **Design Surface** displays a report that is being edited in the [Web Report Designer](../../report-designer.md).

![](../../../images/eurd-web-designer-surface.png)

## Rulers

The horizontal and vertical rulers display tickmarks in your report's specified [measurement units](../configure-design-settings/change-a-report-measurement-units.md). Click an element to evaluate its size and location using the rulers.

The horizontal ruler also allows you to modify the report's side margins (the report's **Margins** property value) by moving the left and right sliders on the ruler.

![](../../../images/eurd-web-designer-surface-horizontal-ruler.png)

You can move a report band's vertical ruler resizing rectangles to change its height.

![](../../../images/eurd-web-designer-surface-vertical-ruler.png)

## Band Captions

In the Report Designer, each [report band](../introduction-to-banded-reports.md) carries a caption, the tab title and color, which depends on the band kind. These captions are not printed in the resultant report document and are only visible at design time.

You can expand or collapse a band's content at design time by clicking the tab on the left side of the band.

![](../../../images/eurd-web-designer-surface-band.png)

To access a band's properties, click the band's caption and switch to the [Properties Panel](ui-panels/properties-panel.md).

## Context Menus

Context menus provide quick access to actions for the selected report element. Right-click a report element to invoke the context menu:

![Web Report Designer - Context Menu for Report Controls](../../../images/web-report-designer-context-menu-control.png)

Context menus allow you to do the following:

* Add new bands, if you selected a report.
    
    ![Web Report Designer - Context Menu for Bands](../../../images/web-report-designer-context-menu-bands.png)

* Manage cells, rows, and columns in a table.
    
    ![Web Report Designer - Context Menu for Table Cells](../../../images/web-report-designer-context-menu-table-cells.png)

* Change element layout (for example, align elements to each other, snap to grid, change content alignment).
    
    ![Web Report Designer - Align and Position Elements](../../../images/web-report-designer-context-menu-align.png)

Context menus are also available in [Field List](ui-panels/field-list.md) and [Report Explorer](ui-panels/report-explorer.md) windows.

## Smart Tags

When you select a report element (report, band, or report control), a smart tag and expression button are displayed next to the element on the Design Surface:

![Web Report Designer - Smart Tag and Expression Buttons](../../../images/web-report-designer-smart-tags-expressions.png).

The expression button invokes the [Expression Editor](ui-panels/expressions-panel.md).

The smart tag opens a panel with the element's most commonly used properties:

![Web Report Designer - Smart Tag](../../../images/web-report-designer-smart-tag.png)

The smart tag contains properties from the element's **Task** group of the Properties Panel. Note that complex properties (for example, `Symbology`  for a Barcode control) need to be configured in the **Properties Panel**. 

## Data Binding Indication

The Report Designer displays a database barrel icon above [data-bound](../use-report-elements/bind-controls-to-data.md) report controls.

You can click the [Validate Bindings](../use-report-elements/validate-report-data-bindings.md) toolbar button to highlight report controls with invalid [expression/data bindings](../use-expressions/data-binding-modes.md). This allows you to determine if the specified expression has an incorrect syntax or uses non-existing data source fields.

![](../../../images/eurd-web-validation-bindings.png)

## In-Place Editors

In-place editors allow you to edit the text-oriented controls' content ([Barcode](../use-report-elements/use-bar-codes.md), [Character Comb](../use-report-elements/use-basic-report-controls/character-comb.md), [Check Box](../use-report-elements/use-basic-report-controls/check-box.md), [Label](../use-report-elements/use-basic-report-controls/label.md), [Table Cell](../use-report-elements/use-tables.md)) by double-clicking them.

![](../../../images/eurd-web-designer-surface-in-place-editor.png)

You can switch between a report's **Design** and **Preview** mode using the corresponding buttons in the [Main Toolbar](toolbar.md).