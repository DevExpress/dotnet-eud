---
title: Table Overview
author: Anna Vekhina
---
# Table Overview

The **Table** control displays information in a tabular format and allows you to create [table reports param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } .

You can add a table control by dragging the **Table** item from the [Toolbox param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  onto the report's area.

![](..\/..\/..\/images/eurd-web-drop-table-from-toolbox.png)

The table control contains one or more rows. Each row contains one or more cells. See the [Report Explorer param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  for a table structure example.

![](..\/..\/..\/images/eurd-web-table-structure-in-report-explorer.png)

You can double-click the cell to invoke its in-place editor and type the desired static text.

![](..\/..\/..\/images/eurd-web-table-cell-static-text.png)

You can adjust the font size of a cell's static text to fit into the cell's boundaries. Use the **Fit Text to Bounds** command from the cell's context menu.

![](..\/..\/..\/images/eurd-web-table-cell-fit-text-to-bounds.png)

Refer to [Bind Table Cells to Data param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  to learn about providing dynamic content to table cells.

A table cell is like an [Label param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  control - it provides the same options for text formatting, alignment, appearance, interactivity, etc. 

You can also make a table cell act as a container for other report controls by dropping the required control from the toolbox on this cell.

![](..\/..\/..\/images/eurd-web-drop-check-box-onto-table-cell.png)

If a table cell includes only one control, you can right-click this control and use the **Fit Bounds to Container** command in the context menu. This command resizes the control so that it occupies all the available cell space (excluding borders).

![](..\/..\/..\/images/eurd-web-fit-bounds-to-container.png)

You can assign different [visual styles param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  for even and odd table rows to improve readability.