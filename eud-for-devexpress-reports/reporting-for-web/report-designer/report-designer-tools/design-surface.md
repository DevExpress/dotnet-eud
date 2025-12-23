---
title: Design Surface
author: Anna Vekhina
---
# Design Surface

The **Design Surface** displays a report that is being edited in the [Web Report Designer param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } .

![](..\/..\/images/eurd-web-designer-surface.png)

## Rulers

The horizontal and vertical rulers display tickmarks in your report's specified [measurement units param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } . Click an element to evaluate its size and location using the rulers.

The horizontal ruler also allows you to modify the report's side margins (the report's **Margins** property value) by moving the left and right sliders on the ruler.

![](..\/..\/images/eurd-web-designer-surface-horizontal-ruler.png)

You can move a report band's vertical ruler resizing rectangles to change its height.

![](..\/..\/images/eurd-web-designer-surface-vertical-ruler.png)

## Band Captions

In the Report Designer, each [report band param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  carries a caption, the tab title and color, which depends on the band kind. These captions are not printed in the resultant report document and are only visible at design time.

You can expand or collapse a band's content at design time by clicking the tab on the left side of the band.

![](..\/..\/images/eurd-web-designer-surface-band.png)

To access a band's properties, click the band's caption and switch to the [Properties Panel param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } .

## Context Menus

Context menus provide quick access to actions for the selected report element. Right-click a report element to invoke the context menu:

![Web Report Designer - Context Menu for Report Controls](..\/..\/images/web-report-designer-context-menu-control.png)

Context menus allow you to do the following:

* Add new bands, if you selected a report.
    
    ![Web Report Designer - Context Menu for Bands](..\/..\/images/web-report-designer-context-menu-bands.png)

* Manage cells, rows, and columns in a table.
    
    ![Web Report Designer - Context Menu for Table Cells](..\/..\/images/web-report-designer-context-menu-table-cells.png)

* Change element layout (for example, align elements to each other, snap to grid, change content alignment).
    
    ![Web Report Designer - Align and Position Elements](..\/..\/images/web-report-designer-context-menu-align.png)

Context menus are also available in [Field List param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  and [Report Explorer param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  windows.

## Smart Tags

When you select a report element (report, band, or report control), a smart tag and expression button are displayed next to the element on the Design Surface:

![Web Report Designer - Smart Tag and Expression Buttons](..\/..\/images/web-report-designer-smart-tags-expressions.png).

The expression button invokes the [Expression Editor param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } .

The smart tag opens a panel with the element's most commonly used properties:

![Web Report Designer - Smart Tag](..\/..\/images/web-report-designer-smart-tag.png)

The smart tag contains properties from the element's **Task** group of the Properties Panel. Note that complex properties (for example, `Symbology`  for a Barcode control) need to be configured in the **Properties Panel**. 

## Data Binding Indication

The Report Designer displays a database barrel icon above [data-bound param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  report controls.

You can click the [Validate Bindings param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  toolbar button to highlight report controls with invalid [expression/data bindings param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } . This allows you to determine if the specified expression has an incorrect syntax or uses non-existing data source fields.

![](..\/..\/images/eurd-web-validation-bindings.png)

## In-Place Editors

In-place editors allow you to edit the text-oriented controls' content ([Barcode param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } , [Character Comb param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } , [Check Box param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } , [Label param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } , [Table Cell param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } ) by double-clicking them.

![](..\/..\/images/eurd-web-designer-surface-in-place-editor.png)

You can switch between a report's **Design** and **Preview** mode using the corresponding buttons in the [Main Toolbar param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } .