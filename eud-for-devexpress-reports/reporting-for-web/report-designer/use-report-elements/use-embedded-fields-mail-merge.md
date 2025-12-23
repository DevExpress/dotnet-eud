---
title: Use Embedded Fields (Mail Merge)
author: Anna Vekhina
---
# Use Embedded Fields (Mail Merge)

This topic describes how to provide data to report controls using the advanced **Mail Merge** binding method. This feature allows you to create templates in which data source values populate specific fields while other text remains constant (that is, allows you to combine static and dynamic content within the same control).

## <a name="embedfields"></a>Embed Fields in a Control Text
You can apply mail merge to the control's **Text** property only. Double-click the required control on the design surface to invoke the in-place editor. Insert data field names with square brackets to create embedded fields and use any prefixes or postfixes.

![](..\/..\/images/eurd-web-mail-merge-insert-data-fields.png)

You can embed a [parameter param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } 's value into a control's content using the **?ParameterName** syntax.

![](..\/..\/images/eurd-web-mail-merge-insert-parameters.png)

Embedded fields are replaced with values obtained from an assigned data source when previewing or exporting a report:

![](..\/..\/images/eurd-web-mail-merge-preview-result.png)

Consider the following specifics and limitations when using embedded fields:

* Field names should not use spaces to be interpreted correctly.
* Mail Merge is not available for a table's nested fields in a master-detail hierarchy.
* Embedded fields cannot be exported to [XLS param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  and [XLSX param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  as values; they are always exported as plain text. We recommend using [text formats param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  instead if you need to accompany dynamic data with static text.

## <a name="formatfields"></a>Format Embedded Fields

You can add a format to the target data field by separating it from the field name with the **!** symbol and apply this format to field values when previewing a document.

![](..\/..\/images/eurd-web-mail-merge-format-string-result.png)

## <a name="supportedcontrols"></a>Supported Controls
You can apply the mail merge feature to the **Text** of the following report controls:

* [Barcode param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } 
* [Character Comb param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } 
* [Check Box param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } 
* [Label param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } 
* [Rich Text param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } 
* [Table Cell param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } 