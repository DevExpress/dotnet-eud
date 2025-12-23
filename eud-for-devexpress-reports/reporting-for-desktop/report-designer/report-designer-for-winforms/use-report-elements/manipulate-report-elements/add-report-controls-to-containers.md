---
title: Add Report Controls to Containers
author: Anna Gubareva
---
# Add Report Controls to Containers

The [Panel param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  control allows you to place various report controls on it to combine them into a group.

![](..\/..\/..\/..\/images/eurd-win-add-report-controls-to-panel.png)

You can use this panel to move, copy, change appearance settings, etc. instead of adjusting individual controls.

![](..\/..\/..\/..\/images/eurd-win-panel-control-moving.png)

A [table cell param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  can also act as a container for other controls.

![](..\/..\/..\/..\/images/eurd-win-add-control-to-table-cell.png)

Both panel and table cells cannot contain the following report controls:
* [Pivot Grid param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } 
* [Subreport param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } 
* [Page Break param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } 
* [Table of Contents param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } 
* [Cross-Band Line and Box param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } 

If a panel or table cell includes only one control, you can use the **Fit Bounds to Container** command in the context menu to position the control within the container. This command resizes the control so that it occupies all the available space (except borders).

![](..\/..\/..\/..\/images/eurd-win-fit-bounds-to-container.png)
