---
title: Sort Groups by a Summary Function's Result
author: Anna Gubareva
---
# Sort Groups by a Summary Function's Result

This tutorial explains how to sort groups by a summary function result, in particular, by the number of records groups contain.

1. Create a new or open an existing data-bound report.
	
	You cannot apply grouping unless your report is bound to a data source.
2. [Group the report param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  by the required data field, [calculate the record count param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  in each group and construct the required report layout.

    ![](..\/..\/..\/..\/images/eurd-win-group-by-summary-layout.png)

3. Click the Group Header band's smart tag, and click the **Sorting Summary** property's ellipsis button.
	
	In the invoked **Group Sorting Summary Editor**, turn on the **Enabled** option, set the **Field** option to the data field from the Detail band, and set the **Summary function** to **Count**.
	
	![](..\/..\/..\/..\/images/eurd-win-group-by-summary-settings.png)
	
	In this editor, you can also define the sorting direction for the group, as well as specify whether or not the **Null** values should be ignored.
	
	Click **OK** to apply the changes and close the dialog.

Switch to [Print Preview param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  to see the result.

![](..\/..\/..\/..\/images/eurd-win-group-by-summary-result.png)