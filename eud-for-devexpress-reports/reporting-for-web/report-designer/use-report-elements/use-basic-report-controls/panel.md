---
title: Panel
author: Anna Vekhina
---
# Panel

The **Panel** control is a container that frames separate report controls and allows you to move, copy and paste them. The panel also visually unites report controls in Print Preview (for instance, with borders or a uniform color background).

To add a panel to a report, drag the **Panel** item from the [Toolbox param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  and drop it onto the required report band.

![](..\/..\/..\/images/eurd-web-add-panel-control-to-report.png)

Drop the desired report controls onto the panel to combine them to a group.

![](..\/..\/..\/images/eurd-web-add-report-controls-to-panel.png)

You can use this panel to move, copy, change appearance settings, etc. instead of adjusting individual controls.

![](..\/..\/..\/images/eurd-web-panel-control-moving.png)

The [Report Explorer param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  displays controls placed onto a panel as its subordinate nodes.

![](..\/..\/..\/images/eurd-web-panel-structure-in-report-explorer.png)

The panel cannot contain the following report controls:
* [Cross Tab param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } 
* [Subreport param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } 
* [Page Break param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } 
* [Table of Contents param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } 
* [Cross-Band Line and Box param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } 

If a panel includes only one control, you can use the **Fit Bounds to Container** from the panel's context menu. This command resizes the control so that it occupies all the available container space (excluding borders).

![](..\/..\/..\/images/eurd-web-panel-fit-bounds-to-container.png)

You can also enable the panel's **Can Shrink** property to automatically adjusts the panel's size to fit all the inner controls. For instance, this allows preventing blank areas when you [conditionally hide specific controls param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } .

![](..\/..\/..\/images/eurd-web-panel-can-shrink-property.png)

> [!NOTE]
> The Panel control cannot span several [report bands param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  as [cross-band controls param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  can.