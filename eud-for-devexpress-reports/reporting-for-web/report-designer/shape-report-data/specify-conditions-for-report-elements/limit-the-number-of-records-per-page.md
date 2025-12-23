---
title: Limit the Number of Records per Page
author: Anna Vekhina
---
# Limit the Number of Records per Page

This document describes how to specify the number of data source records displayed on report pages.

After you [bound your report to data param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  and provided content to the report's [Detail band param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } , you can limit the number of records each report page displays. This example demonstrates how to pass the required record count as a parameter value.

1. Switch to the [Field List param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  panel, select the **Parameters** node and click **Add parameter** to add a new report parameter.
	
	![](..\/..\/..\/images/eurd-web-shaping-filter-add-parameter.png)

2. Specify the parameter's description displayed in Print Preview and set its type to **Number (Integer)**.
	
	![](..\/..\/..\/images/eurd-web-shaping-limit-parameter-settings.png)

3. Drop a [Page Break param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  control onto the report's detail band.
	
	![](..\/..\/..\/images/eurd-web-shaping-page-break.png)

4. Switch to the [Expressions param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  panel and click the **Visible** property's ellipsis button. In the invoked [Expression Editor param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } , specify the required [expression param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } .
	
	![](..\/..\/..\/images/eurd-web-shaping-page-break-visible-expression.png)
	
	For example:
	
	**([DataSource.CurrentRowebdex] % [Parameters.parameter1] == 0) And ([DataSource.CurrentRowebdex] !=0)**

When switching to [Print Preview param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } , you can specify how many rows each report page should display by entering the corresponding parameter value:

![](..\/..\/..\/images/eurd-web-shaping-limit-rows-result.png)