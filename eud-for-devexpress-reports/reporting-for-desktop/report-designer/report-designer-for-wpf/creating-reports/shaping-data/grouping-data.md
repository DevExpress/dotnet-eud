---
title: Grouping Data
author: Anna Gubareva
legacyId: 116280
---
# Grouping Data
This document demonstrates how to group report data. Grouping allows you to split data into groups based on identical values in a field or fields. Note that data grouping can be performed only if a report is [bound to a data source param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } .

To group records in a report, do the following.
1. [Create a new report param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  and [bind it to a data source param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } . This tutorial starts with the following report.
	
	![EUD_WpfReportDersigner_Grouping_InitialReport](..\/..\/..\/..\/images/img123495.png)
2. Next, switch to the [Group and Sort Panel param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } , and click **Add a Group**. In the invoked drop-down list, select a data member across which the report is to be grouped.
	
	![EUD_WpfReportDersigner_Grouping_1](..\/..\/..\/..\/images/img123496.png)
3. After this, the [Group Header param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  band is added to the report with the specified data member set as its grouping criterion.
	
	Drop the data field, which is specified as the grouping criterion, from the [Field List param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  panel onto the Group Header band. This data field will be displayed as a header for each group.
	
	![EUD_WpfReportDersigner_Grouping_2](..\/..\/..\/..\/images/img123497.png)
4. In addition, you can enable the corresponding Group Footer band by enabling the **Show Footer** option in the Group and Sort Panel.
	
	![EUD_WpfReportDersigner_Grouping_3](..\/..\/..\/..\/images/img123498.png)
	
	Use the **Sort Order** drop-down list to manage the sorting order of the group's items (ascending or descending) or to disable sorting in grouped data. If multiple groups are created, you can specify the priority for each group by selecting it in the Group and Sort Panel and using the **Move Up** and **Move Down** buttons.
5. Then, you can [calculate a total param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  across the group by placing a [Label param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  onto the Group Footer band and specifying its **Summary** properties in the following way.
	
	![EUD_WpfReportDersigner_Grouping_4](..\/..\/..\/..\/images/img123499.png)
	
	Note also that value formatting is applied to a summary independently of the [general formatting param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } , and has a greater priority.

The report is now ready. Switch to the [Print Preview param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  tab and view the result.

![EUD_WpfReportDersigner_Grouping_Result](..\/..\/..\/..\/images/img123500.png)