---
title: Page Break
author: Anna Vekhina
---
# Page Break

The **Page Break** control's sole purpose is to insert a page delimiter at any point within a report.

You can add this control by dragging the **Page Break** item from the [Toolbox param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  onto the report's area.

![](..\/..\/..\/images/eurd-web-add-page-break-to-report.png)

This control is visually represented by a short line attached to the report's left margin.

The Page Break control is useful when you need to insert a page break between controls within a [report band param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  (for example, to divide subreports so that the second subreport starts printing on a new page).

![](..\/..\/..\/images/eurd-web-page-break-between-subreports.png)

You can also insert a page break before or after a specific report band using the band's **Page Break** property.

![](..\/..\/..\/images/eurd-web-band-page-break-property.png)