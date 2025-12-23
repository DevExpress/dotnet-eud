---
title: Conditionally Change a Label's Text
author: Anna Vekhina
---
# Conditionally Change a Label's Text

This document describes how to display different values in a report control based on a specified logical condition.

After you [bound your report to data param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  and specified a bound data field in a report control's **Expression** property, you can make this control display different values based on a specified logical condition:

1. Expand the **Label Tasks** category and click the **Expression** property's ellipsis button.
	
	![](..\/..\/..\/images/eurd-web-shaping-label-expression-property-for-custom-text.png)

2. In the invoked [Expression Editor param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } , specify the required [expression param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } .
	
	![](..\/..\/..\/images/eurd-web-shaping-label-expression-for-custom-text.png)
	
	Use the **Iif** function to define the condition. For example:
	
	**Iif([UnitsOnOrder] == 0, 'None', [UnitsOnOrder])**
	
	This expression means that if the data field's value is zero, the control's text is set to '**None**'; otherwise, it displays the actual field value.

When switching to [Print Preview param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } , you can see the report control displaying the assigned values.

![](..\/..\/..\/images/eurd-web-shaping-label-custom-text-result.png)