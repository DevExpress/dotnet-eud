---
title: Count the Number of Groups in a Report
author: Anna Vekhina
---
# Count the Number of Groups in a Report

This document describes how to count the number of groups in a report.

1. Insert the [Group Header param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  band, select the **Group Fields** section in the **Group Header Tasks** category and add a new group field to group the report's data by the required field.
	
	![](..\/..\/..\/images/eurd-web-shaping-count-group-data.png)

2. Switch to the [Field List param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  and drop the group field onto the created Group Header.
	
	![](..\/..\/..\/images/eurd-web-shaping-count-drop-filed-onto-group-header.png)

3. Drop a label onto the Report Footer, expand the **Summary** section in the **Label Tasks** category and set the **Running** property to **Report**.
	
	![](..\/..\/..\/images/eurd-web-shaping-group-count-summary-running.png)

4. Click the **Text** property marker to invoke the menu. Select **Text Expression** to invoke the [Expression Editor param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } .

	![](..\/..\/..\/images/eurd-web-shaping-group-count-text-expression.png)


5. In the Expression Editor select the **sumDCount** summary function in the **Functions** | **Summary** section:

	`sumDCount([CategoryName])`
	
	![](..\/..\/..\/images/eurd-web-shaping-group-count-expression.png)

6. Use the **Text Format String** property to format the summary's value.
	
	![](..\/..\/..\/images/eurd-web-shaping-group-count-format-string.png)

7. Switch to [Print Preview param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  and see the group count in the report footer:

	![](..\/..\/..\/images/eurd-web-shaping-group-count-result.png)