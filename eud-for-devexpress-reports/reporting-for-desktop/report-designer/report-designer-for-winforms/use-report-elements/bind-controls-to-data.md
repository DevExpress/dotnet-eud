---
title: Bind Report Controls to Data (Expression Bindings)
author: Anna Gubareva
---
# Bind Report Controls to Data (Expression Bindings)

You can use the following approaches to include a data source's information in your report:

* [Use the Field List](#use-the-field-list)
* [Use the Smart Tag](#use-the-smart-tag)
* [Use the Property Grid](#use-the-property-grid)

## Use the Field List

After you [bind your report to data param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } , the [Field List param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  panel displays the data source's hierarchy and provides access to the available data fields. 

Drop a data field from this panel onto a report's surface to create a new report control bound to the corresponding field.

![eurd-win-field-list-drop-fields](..\/..\/..\/images/eurd-win-field-list-drop-fields.png)

Drop a data field onto an existing control to bind this control to the corresponding field.

![eurd-win-field-list-drop-field-to-control](..\/..\/..\/images/eurd-win-field-list-drop-field-to-control.png)

You can do one of the following to create a data-bound control of a specific type:

* Hold down the SHIFT key and drop a data field onto a report's surface.
* Right-click a corresponding data field and drop it onto a report's surface.

This invokes a context menu that enables you to select which control to create.

![eurd-win-fieldlist-create-specific-contols](..\/..\/..\/images/eurd-win-fieldlist-create-specific-contols.png)

You can also drop an entire data table onto a report to create a [Table param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  control with its cells bound to the corresponding data table fields. 

![eurd-win-field-list-drop-table](..\/..\/..\/images/eurd-win-field-list-drop-table.png)

To select multiple fields in the Field List, hold CTRL or SHIFT and click the fields. Drop these fields onto a report to create a new table.

![design-time-field-list-drop-multiple-fields](..\/..\/..\/images/eurd-win-list-drop-multiple-fields.png)

## Use the Smart Tag

Click a control's smart tag, expand the **Expression** drop-down list and select a data field.

![](..\/..\/..\/images/eurd-win-label-bind-to-data-field.png)

You can also click the **Expression** option's ellipsis button to invoke the **Expression Editor**. This editor allows you to construct a complex binding expression with two or more data fields and various functions. See [Expression Language param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  for more information.
 
![](..\/..\/..\/images/eurd-win-label-expression-binding.png)


## Use the Property Grid

Click a property marker to see whether the invoked context menu has the **PropertyName Expression** item.

![](..\/..\/..\/images/eurd-win-property-grid-data-binding.png)

Click this item to specify an expression in the invoked Expression Editor.

![WinFormsPropertyGrid-ExpressionEditor](..\/..\/..\/images/eurd-win-PropertyGrid-ExpressionEditor.png)

You can use the same approach to specify expressions for all the control properties. See [Shape Report Data param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  for more tutorials.

