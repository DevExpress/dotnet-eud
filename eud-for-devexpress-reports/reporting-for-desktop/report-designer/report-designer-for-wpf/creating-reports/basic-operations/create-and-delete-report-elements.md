---
title: Create and Delete Report Elements
author: Anna Gubareva
legacyId: 116287
---
# Create and Delete Report Elements
This document describes how to add and delete [report controls param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  and [bands param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  in the Report Designer.

The topic consists of the following sections.
* [Creating Report Controls](#createcontrols)
* [Creating Report Bands](#createbands)
* [Deleting Controls and Bands](#delete)

<a name="createcontrols"/>

## Creating Report Controls
All available controls are listed in the [Control Toolbox param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } . To add a control to the currently opened report, you can drag and drop it onto an appropriate [report band param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } .

![WPFDesigner_DragAndDropItemFromToolbox](..\/..\/..\/..\/images/img120304.png)

Report controls of appropriate types are created automatically, after you drag items from the [Field List param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  and drop them onto the [report surface param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } .

![EUD_WpfReportDesigner_BindControls_2](..\/..\/..\/..\/images/img123705.png)

<a name="createbands"/>

## Creating Report Bands
To add a new band of a particular type, use the context menu of the report or bands. Right-click a report on the [design surface param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  or in the [Report Explorer param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } , and select a band to be inserted in the report.

![EUD_WpfReportDesigner_CreateBand](..\/..\/..\/..\/images/img123817.png)

<a name="delete"/>

## Deleting Controls and Bands
To delete a report control or band, select it on the [design surface param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  or [Report Explorer param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } , and then do one of the following.
* Press the DELETE key.
* Right-click the report element, and in the invoked context menu, select **Delete**.
	
	![EUD_WpfReportDesigner_DeleteControl](..\/..\/..\/..\/images/img123818.png)
* Click the **Delete** ![WPFDesigner_Toolbar_DeleteIcon](..\/..\/..\/..\/images/img120139.png) button on the [Toolbar param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } .

Note that certain elements cannot be deleted (such as the Detail band).