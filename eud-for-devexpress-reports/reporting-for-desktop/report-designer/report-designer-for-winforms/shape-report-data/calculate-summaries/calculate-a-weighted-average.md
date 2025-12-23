---
title: Calculate a Weighted Average
author: Anna Gubareva
---
# Calculate a Weighted Average

![](..\/..\/..\/..\/images/eurd-win-weighted-average-result.png)

Follow the steps below to calculate a weighted average:

1. [Open an existing report param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  or [create a new one from scratch param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } .
2. [Bind a report param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  to a required data source.
3. [Group the report's data param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  using the [Group and Sort Panel param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  and construct a layout like the following:
	
	![](..\/..\/..\/..\/images/eurd-win-weighted-average-group-data.png)

4. Add the [Group Footer param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  band to the report and drop a [Label param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  control on this band to display the summary result.	Click the label's smart tag, then click the Summary field's ellipsis button.
	
	![](..\/..\/..\/..\/images/eurd-win-weighted-average-summary-running.png)

5. In the invoked **Summary Editor** window:
    * Set the **Summary Running** property to **Group**.
    * Set the **Summary Function** property to **Weighed average**.
    * Set the **Argument Expression** property to the field to count the weighted average on, and the **Weight** property to the field that provides weights.
	
	![](..\/..\/..\/..\/images/eurd-win-weighted-average-summary-expression.png)

6. You can also use the control's **Format String** property to format the summary value. For instance, set this property to **Weighted Average Price: {0:c2}**.
