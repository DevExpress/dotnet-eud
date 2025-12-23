---
title: Conditionally Suppress Controls
author: Anna Gubareva
---
# Conditionally Suppress Controls

This document describes how to display or hide a report control in a published document based on a specified logical condition.

1. [Create a new report param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  or open an existing one and prepare the report layout.

    ![](..\/..\/..\/..\/images/eurd-win-shaping-suppress-initial-layout.png)

2. Select the required control and switch to the [Property Grid param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } . Open the **Behavior** tab, click the **Visible** property's marker and select **Visible Expression** in the context menu.

    ![](..\/..\/..\/..\/images/eurd-win-shaping-suppress-visible-property.png)

3. In the invoked **Expression Editor**, specify the required [expression param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } .
	
	![](..\/..\/..\/..\/images/eurd-win-shaping-suppress-expression.png)
	
	Use the **Iif** function to define the required condition. For example:
	
	**Iif([Discontinued] == False, False, [Discontinued])**
	
	This expression means that if the data field's value is **False**, the control's **Visible** property is disabled.

When switching to [Print Preview param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } , you can view the report control's visibility changes according to the assigned condition.

![](..\/..\/..\/..\/images/eurd-win-shaping-suppress-result.png)

> [!Note]
> See [Hide Table Cells param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  to learn how to conditionally suppress table cells and define the mode for processing them.