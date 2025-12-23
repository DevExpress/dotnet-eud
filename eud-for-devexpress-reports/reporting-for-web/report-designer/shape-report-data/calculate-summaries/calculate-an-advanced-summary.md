---
title: Calculate an Advanced Summary
author: Anna Vekhina
---
# Calculate an Advanced Summary

This document describes how to calculate an advanced summary for report groups using a built-in summary function and arithmetical or logical functions.

1. [Create a new report param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  or open an existing one and [bind it to a data source param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } .

2. Insert the [Group Header param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  band, select the **Group Fields** section in the **Group Header Tasks** category and add a new group field to group the report's data by the required field. 

    ![](..\/..\/..\/images/eurd-web-label-advanced-summary-group-data.png)

3. Insert the Group Footer band and drop a [Label param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  onto it to display the summary result. Expand the **Summary** section in the **Label Tasks** category and set the **Running** property to **Group**.

    ![](..\/..\/..\/images/eurd-web-label-advanced-summary-running.png)

4. Click the ellipsis button for the label's **Expression** property.

    ![](..\/..\/..\/images/eurd-web-label-advanced-summary-expression-property.png)

5. This invokes the [Expression Editor param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  where you can specify a custom expression with the required summary functions and other logical or arithmetical functions. For example:

    ![](..\/..\/..\/images/eurd-web-label-advanced-summary-expression-editor.png)

	> [!TIP]
	> See the [Functions in Expressions param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  topic for a complete list of supported summary functions.

6. You can use the **Text Format String** property to format the summary's value.
	
	![](..\/..\/..\/images/eurd-web-label-advanced-summary-format-string.png)

Switch to [Print Preview param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  to see the result.

![](..\/..\/..\/images/eurd-web-label-advanced-summary-result.png)