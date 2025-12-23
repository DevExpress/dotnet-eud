---
title: Calculate an Advanced Summary
author: Anna Gubareva
---
# Calculate an Advanced Summary

This document describes how to calculate an advanced summary for report groups using a built-in summary function and arithmetical or logical functions.

1. [Create a new report param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  or open an existing one and [bind it to a data source param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } .

2. Switch to the [Group and Sort param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  panel and group the report's data by the required field. Display the footer for the created group.

    ![](..\/..\/..\/..\/images/eurd-win-label-summary-group-data.png)

3. Drop a [Label param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  onto the group footer to display the summary result.

    Click the label's smart tag and set its **Summary** property to **Group**.

    ![](..\/..\/..\/..\/images/eurd-win-label-advanced-summary-running.png)

4. Click the **Expression** property's ellipsis button.

    ![](..\/..\/..\/..\/images/eurd-win-label-advanced-summary-expression-property.png)

5. This invokes the **Summary Expression Editor** where you can specify a custom expression with the required summary functions and other logical or arithmetical functions. For example:

    ![](..\/..\/..\/..\/images/eurd-win-label-advanced-summary-expression.png)

	> [!TIP]
	> See the [Functions in Expressions param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  topic for a complete list of supported summary functions.

6. You can use the **Format String** property to format the summary's value.
	
	![](..\/..\/..\/..\/images/eurd-win-label-advanced-summary-format-string.png)

Switch to [Print Preview param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  to see the result.

![](..\/..\/..\/..\/images/eurd-win-label-advanced-summary-result.png)