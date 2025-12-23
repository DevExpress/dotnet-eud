---
title: Enable the Right-To-Left Layout
author: Anna Vekhina
---
# Enable the Right-To-Left Layout

The report and most of the report controls provide the **Right to Left** and **Right to Left Layout** property. 

![](..\/..\/images/eurd-web-right-to-left-yes-property.png)

## Right to Left

The  property specifies content layout within a control (for most controls, this property affects the direction of their text, and for the [Check Box param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } , this property also affects the check box position within the control).

* **Disabled**

    ![](..\/..\/images/eurd-web-right-to-left-no.png)

* **Enabled**

    ![](..\/..\/images/eurd-web-right-to-left-yes.png)

Initially all report controls have this property set to **Inherit**, and when you enable it for a report, the setting is enabled for all report controls.

The following controls support this feature:

* [Label param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } 
* [Check Box param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } 
* [Page Info param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } 
* [Panel param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } 
* [Cross Tab param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } 
* Pivot Grid (deprecated)
* [Table param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } 
* [Table of Contents param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } 

For the **Panel** and **Table** controls, this option affects contained controls.

## Right to Left Layout

When the **Right To Left** property of a report is set to **Yes**, you can also enable the **Right To Left Layout** property that specifies the position of controls within [report bands param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } . Enabling the right-to-left layout will also swap the page margins of a document (you are not allowed to place controls outside the right page margin).

![](..\/..\/images/eurd-web-right-to-left-layout.png)

The coordinates of report controls remain unchanged, only the point and direction of reference change (the X coordinate is calculated based on the top right corner).

The right-to-left layout is preserved when exporting a report to any [supported format param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } .        