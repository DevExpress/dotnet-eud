---
title: Bind Table Cells to Data
author: Anna Gubareva
---
# Bind Table Cells to Data

You can create a table control with cells [bound param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  to data fields obtained from a report's data source using the [Field List param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } . Select data fields by clicking them while holding the CTRL or SHIFT key and drop them onto the Detail band.

![](..\/..\/..\/..\/images/eurd-win-table-control-drop-fields-from-field-list.png)

Drag and drop the same fields with the right mouse button to create column headers with the corresponding field names.

![](..\/..\/..\/..\/images/eurd-win-table-control-drop-captions-from-field-list.png)

You can bind individual table cells to data in the same ways as [Label param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  controls. Dropping a data field onto an existing cell binds this cell to a corresponding field.

![](..\/..\/..\/..\/images/eurd-win-bind-existing-table-cell-to-data.png)

Alternatively, click the cell's smart tag, expand the **Expression** drop-down list and select the required data field

![](..\/..\/..\/..\/images/eurd-win-table-cell-smart-tag-expression-binding.png)

Clicking the **Expression** option's ellipsis button invokes the Expression Editor. This allows you to construct a complex binding expression involving two or more data fields.

See the [Bind Report Controls to Data param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  topic to learn more about creating data-aware controls.

The **Process Duplicates Mode** and **Process Duplicates Target** options enable you to merge cells with identical values.

![](..\/..\/..\/..\/images/eurd-win-table-cell-process-duplicates-mode.png)