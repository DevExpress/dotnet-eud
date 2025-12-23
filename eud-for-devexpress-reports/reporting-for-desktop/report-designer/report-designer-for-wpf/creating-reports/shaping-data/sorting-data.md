---
title: Sorting Data
author: Anna Gubareva
legacyId: 116281
---
# Sorting Data
This document demonstrates how to sort report data. Note that as with data grouping, sorting can be performed only if a report is [bound to a data source param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } . This example uses the report created in the following tutorial: [Grouping Data param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } .

To sort records in a data-aware report, do the following.
1. Switch to the [Group and Sort Panel param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } , and click **Add a Sort**. In the invoked drop-down list, choose a data field across which the report is to be sorted.
	
	![EUD_WpfReportDersigner_Sorting_1](..\/..\/..\/..\/images/img123501.png)
2. To manage the sorting order, use the **Sort Order** drop-down list.
	
	If multiple sorting criteria are specified, you can define the priority for each one by selecting it in the Group and Sort Panel and using the **Move Up** and **Move Down** buttons.

The report is now ready. Switch to the [Print Preview param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  tab and view the result.

![EUD_WpfReportDersigner_Sorting_Result](..\/..\/..\/..\/images/img123502.png)