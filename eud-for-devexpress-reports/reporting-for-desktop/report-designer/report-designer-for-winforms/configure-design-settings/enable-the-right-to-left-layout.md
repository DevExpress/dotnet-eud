---
title: Enable the Right-To-Left Layout
author: Anna Gubareva
---
# Enable the Right-To-Left Layout

The report and most of the report controls provide the **Right to Left** property. 

![](..\/..\/..\/images/eurd-win-right-to-left-property.png)

This property specifies content layout within a control (for most controls, this property affects the direction of their text, and for the [Check Box param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } , this property also affects the check box position within the control).

* **Left-To-Right**

    ![](..\/..\/..\/images/eurd-win-right-to-left-no.png)

* **Right-To-Left**

    ![](..\/..\/..\/images/eurd-win-right-to-left-yes.png)

By default, all report controls have this property set to **Inherit**, so enabling it for a report will apply this setting to all its controls.

The following controls support this feature:

* [Label param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } 
* [Check Box param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } 
* [Page Info param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } 
* [Panel param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } 
* [Pivot Grid param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } 
* [Table param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } 
* [Table of Contents param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } 

For the **Panel** and **Table**, this option only affects the controls contained in them.

When the **Right to Left** property of a report is set to **Yes**, you can also enable the **Right To Left Layout** property that specifies the position of controls within [report bands param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } . Enabling the right-to-left layout will also swap the page margins of a document (it will become impossible to place controls outside the right page margin).

![](..\/..\/..\/images/eurd-win-right-to-left-layout.png)

The controls' coordinates will remain unchanged and only the point and direction of reference will change (the X coordinate will be calculated starting with the top right corner).

The right-to-left layout is preserved when exporting a report to any of the [supported formats param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  (e.g., PDF, Excel, or RTF).