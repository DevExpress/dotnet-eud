---
title: Display the Current Date and Time in a Report
author: Anna Vekhina
---
# Display the Current Date and Time in a Report

This tutorial demonstrates how to insert the current system date and time into a report using the [PageInfo param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  control.

![](..\/..\/images/eurd-web-insert-datetime-result.png)

Do the following to include information about the current date and time into a report:

1. The current date and time are usually displayed in the [Report Header param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  band. To add it to the report,  click **Insert Report Header Band** in the context menu.
	
	![](..\/..\/images/eurd-web-shaping-insert-report-header.png)
2. Drop the [PageInfo param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  control from the [Toolbox param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  onto the **Report Header** band.
	
	![](..\/..\/images/eurd-web-insert-date-time-add-pageinfo.png)
3. Set the control's **Page Information** property to *Current Date and Time*.
	
	![](..\/..\/images/eurd-web-insert-datetime-set-pageinfo.png)
4. To apply a format string to the control's contents, type **Created at {0:h:mm tt dd MMMM yyyy}** into its **Text Format String** property.
	
	![](..\/..\/images/eurd-web-insert-datetime-set-formatstring.png)