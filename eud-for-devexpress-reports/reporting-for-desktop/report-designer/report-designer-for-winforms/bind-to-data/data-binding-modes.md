---
title: Data Binding Modes
author: Anna Gubareva
---
# Data Binding Modes

The Report Designer works in one of the following data binding modes:

* **Expressions** is the default binding mode.

    This mode enables you to specify complex [expressions param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  that include two or more data fields, [report parameters param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } , or [functions](../use-expressions/expression-language.md#functions). You can also use expressions to [calculate summaries param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  of any complexity or [conditionally shape your data param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } .

    Click a property's marker to see whether the invoked context menu has the **PropertyName Expression** item that invokes the **Expression Editor**.

    ![Property Marker](..\/..\/..\/images/eurd-win-binding-modes-property-marker.png)

    The **Expression Editor** allows you to use functions, access report bands and controls, and reference data source values in the constructed expression.

    ![Expression Editor](..\/..\/..\/images/eurd-win-binding-modes-expression-editor.png)

* **Expressions Advanced** is the advanced Expression mode.

    This mode enables you to specify an expression that is evaluated within a control's specific event.

	![property-grid-expression-advanced-tab](..\/..\/..\/images/eurd-win-binding-modes-expressions-advanced.png)

    The **Expression Editor** allows you to use event argument values in the constructed expressions. Event arguments are available in the [Variables param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  section.

    In the **BeforePrint** event, you can use data fields from all queries in the data source.

    ![Expression Editor for the BeforePrint event](..\/..\/..\/images/eurd-win-binding-modes-data-fields.png)

    In the **PrintOnPage** event, data source fields are not available because data was fetched when this event occurs. You can use the event arguments that are available in the [Variables param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  section.

    ![Expression Editor for the PrintOnPage event](..\/..\/..\/images/eurd-win-binding-modes-event-arguments.png)
