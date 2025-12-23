---
title: Draw Cross-Band Lines and Boxes
author: Anna Gubareva
---
# Draw Cross-Band Lines and Boxes

Cross-band controls allow you to draw lines and rectangles through several [report bands param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } .

The Report Designer provides the following two cross-band controls:

* The **Cross-Band Line** control draws vertical lines that can span multiple report bands. You can use this control to emphasize a report area that consists of different bands.   
* The  **Cross-Band Box** control draws rectangles through several report bands. You can use this control to encompass a report section that includes multiple band areas.

To add a cross-band control to a report, select the corresponding item in the [Toolbox param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  and draw a rectangle across required bands.

![](..\/..\/..\/..\/images/eurd-win-add-cross-band-control-to-report.png)

The following properties define a cross-band control's location in a report:

* **Start Band** - determines the band from which the control starts to draw;
* **Start Point** - specifies the exact coordinates (measured in [report units param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } ) within the start band where the control starts to draw;
* **End Band** -  determines the band where the cross-band control stops to draw;
* **End Point** - specifies the exact coordinates (measured in [report units param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } ) within the end band where the control finishes to draw.

![](..\/..\/..\/..\/images/eurd-win-cross-band-control-properties.png)

The following image illustrates how the [Report Explorer param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  reflects cross-band controls:

![](..\/..\/..\/..\/images/eurd-win-cross-band-controls-in-report-explorer.png)

