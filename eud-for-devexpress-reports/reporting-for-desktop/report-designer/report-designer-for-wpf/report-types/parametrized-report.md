---
title: Parametrized Report
author: Anna Gubareva
legacyId: 116210
---
# Parametrized Report
This tutorial describes the steps needed to create a report with parameters. In this example, two date-time parameters are created to filter out orders that don't fall in the specified range from the report.

To create report parameters, follow the steps below.
1. [Create a new report param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  and bind it to a data source.
2. In the [Field List param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  panel, right-click the **Parameters** section and in the invoked menu, click **Add Parameter**.
	
	![EUD_WpfReportDesigner_Parametrized_1](..\/..\/..\/images/img123797.png)
3. In the invoked **Add New Parameter** dialog, set the created parameter's **Name** and **Description** properties and make sure to set its **Type** to an appropriate value. To display this parameter in the [Print Preview param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } , enable the **Show in the parameters panel** option.
	
	![EUD_WpfReportDesigner_Parametrized_2](..\/..\/..\/images/img123798.png)
4. To assign a list of values to this report parameter, enable the **Supports the collection of standard values** option.
	
	In the **Dynamic values** tab, you can specify a parameter's data source, data member, value member and display member. The value member defines a data field that provides values to the parameter. The display member defines a data field that provides display names for parameter values, i.e., how these values appear in the user interface available in a [Print Preview param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } .
	
	In the **Static values** tab, you can manually fill the list of parameter values. Each parameter value has an individual description specifying how this value appears in the [Parameters Panel param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } .
	
	![EUD_WpfReportDesigner_Parametrized_3](..\/..\/..\/images/img123800.png)
5. Then, repeat the previous steps to create the second parameter, so that every time your report is previewed, you will be asked to specify two dates.
6. Next, use parameters to filter your report's data. Select report, and in the [Properties Panel param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } , click the ellipsis button for the **Filter String** property. Then, in the invoked **Filter String Editor**, construct an expression where a data field is compared with the created parameters. To access parameters, click the icon on the right until it turns into a question mark.
	
	![EUD_WpfReportDesigner_Parametrized_4](..\/..\/..\/images/img123801.png)

The Parametrized report is now ready. Switch to the [Print Preview param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  tab, define the required values in the **Parameters** panel and click **Submit**.

![EUD_WpfReportDesigner_Parametrized_Result](..\/..\/..\/images/img123802.png)