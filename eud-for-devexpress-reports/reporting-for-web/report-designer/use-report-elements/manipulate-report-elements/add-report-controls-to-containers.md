---
title: Add Report Controls to Containers
author: Anna Vekhina
---
# Add Report Controls to Containers

The [Panel param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  control allows you to place various report controls on it to combine them into a group. 

![](..\/..\/..\/images/eurd-web-add-label-to-panel.png)

You can use this panel to move, copy, change appearance settings, etc. instead of adjusting individual controls.

![](..\/..\/..\/images/eurd-web-move-panel.png)

A [table cell param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  can also act as a container for other controls.

![](..\/..\/..\/images/eurd-web-add-checkbox-to-tablecell.png)

Both panel and table cell cannot contain the following report controls:
* [Cross Tab param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } 
* [Subreport param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } 
* [Page Break param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } 
* [Table of Contents param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } 
* [Cross-Band Line and Box param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } 

If a panel or table cell includes only one control, you can position it within the container using the **Fit Bounds to Container** command. This command resizes the control so that it occupies all the available space (excluding borders).

![](..\/..\/..\/images/eurd-web-fit-bounds-to-container.png)
