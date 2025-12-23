---
title: Multi-Column Report
author: Anna Gubareva
legacyId: 116204
---
# Multi-Column Report
This tutorial describes the steps to create a _multi-column report_, meaning that each page of the report document is laid out in a specified number of columns.

To demonstrate the multi-column feature, use a report with grouping, similar to the one created in the following tutorial: [Grouping Data param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } .
1. Select the [Detail band param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } , and in the [Properties Panel param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } , expand the **Multi-Column Options** section.
	
	Set the required **Mode**, which determines whether the number of columns is manually specified or if it depends on the fixed column width.
	
	![EUD_WpfReportDersigner_MultiColumn_1](..\/..\/..\/images/img123506.png)
2. Then, if you've chosen to **Use Column Count**, set the **Column Count** to **2**, and **Column Spacing** to **10**.
	
	The **Layout** property determines the order in which records of the same group are processed.
	
	![EUD_WpfReportDersigner_MultiColumn_2](..\/..\/..\/images/img123507.png)
3. Now, on the Detail band's surface, a gray area appears, delimiting the available column's width. Adjust the control width, so that they fit within the effective borders.
	
	![EUD_WpfReportDersigner_MultiColumn_3](..\/..\/..\/images/img123508.png)

The multi-column report is now ready. Switch to the [Print Preview param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  tab and view the result.

![EUD_WpfReportDersigner_MultiColumn_Result](..\/..\/..\/images/img123509.png)