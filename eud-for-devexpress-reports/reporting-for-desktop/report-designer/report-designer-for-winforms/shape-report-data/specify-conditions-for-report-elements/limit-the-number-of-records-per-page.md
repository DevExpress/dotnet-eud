---
title: Limit the Number of Records per Page
author: Anna Gubareva
---
# Limit the Number of Records per Page

This document describes how to specify the number of data source records displayed on report pages.

After you [bound your report to data param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  and provided content to the report's [Detail band param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } , you can limit the number of records each report page displays. This example demonstrates how to pass the required record count as a parameter value.

1. Switch to the [Field List param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } , right-click the **Parameters** section and add a new report parameter.
	
	![](..\/..\/..\/..\/images/eurd-win-shaping-filter-add-parameter.png)

2. Specify the parameter's description displayed in Print Preview and set its type to **Number (Integer)**.
	
	![](..\/..\/..\/..\/images/eurd-win-shaping-limit-parameter-settings.png)

3. Drop a [Page Break param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  control onto the report's detail band and switch to the [Property Grid param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } . Open the **Behavior** tab, click the **Visible** property's marker and select **Visible Expression** in the context menu.
	
	![](..\/..\/..\/..\/images/eurd-win-shaping-page-break-visible-property.png)

4. In the invoked **Expression Editor**, specify the required [expression param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } .
	
	![](..\/..\/..\/..\/images/eurd-win-shaping-page-break-visible-expression.png)
	
	For example:
	
	**([DataSource.CurrentRowIndex] % ?parameter1 == 0) And ([DataSource.CurrentRowIndex] !=0)**

When switching to [Print Preview param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } , you can specify how many rows each report page should display by entering the corresponding parameter value:

![](..\/..\/..\/..\/images/eurd-win-shaping-limit-rows-result.png)