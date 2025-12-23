---
title: Conditionally Change a Control's Appearance
author: Anna Gubareva
legacyId: 116338
---
# Conditionally Change a Control's Appearance
This tutorial describes how to conditionally change a control's appearance (e.g., make a [Label param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } 's text red if its value exceeds a certain threshold). Thanks to the _formatting rules_ feature, no [scripts param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  are required to complete this task, so you should not have to write any code.

To conditionally change a control's appearance, do the following.
1. [Create a new report param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  and [bind it to a data source param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } .
2. Right-click the report and select **Edit Formatting Rule Sheet...** in the invoked context menu.
	
	![EUD_WpfReportDesigner_CondFormatting_1](..\/..\/..\/..\/images/img123651.png)
3. In the invoked **Formatting Rule Sheet Editor**, create a new formatting rule using the plus button, and then, click the ellipsis button for its **Condition** property.
	
	![EUD_WpfReportDesigner_CondFormatting_2](..\/..\/..\/..\/images/img123652.png)
4. In the invoked **Expression Editor**, define the required Boolean condition (which means that its result is returned as either **true** or **false**). This tutorial demonstrates how to format fields if the **UnitPrice** value is greater than **30**.
	
	![EUD_WpfReportDesigner_CondFormatting_3](..\/..\/..\/..\/images/img123653.png)
	
	To save the condition and close the dialog, click **OK**.
5. Return to the **Formatting Rule Sheet Editor** and define the formatting to be applied, e.g., specify the desired foreground color.
	
	![EUD_WpfReportDesigner_CondFormatting_4](..\/..\/..\/..\/images/img123654.png)
	
	To save the changes and quit the dialog, click **OK**.
6. Finally, select the band or control to which the formatting rule should be applied (in this example, it is the [Detail band param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } ), and select **Edit Formatting Rules...** in the context menu.
	
	![EUD_WpfReportDesigner_CondFormatting_5](..\/..\/..\/..\/images/img123655.png)
7. In the invoked **Formatting Rules Editor**, move the rule from left to right using the right arrow button so that you can apply the rule for this band.
	
	![EUD_WpfReportDesigner_CondFormatting_6](..\/..\/..\/..\/images/img123656.png)
	
	If multiple rules are applied, it is possible to customize their precedence using the up and down arrow buttons. So, the rules are applied in the same order that they appear in the list, and the last rule in the list has the highest priority.

Switch your report to the [Print Preview param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  tab and view the result.

![EUD_WpfReportDesigner_CondFormatting_Result](..\/..\/..\/..\/images/img123657.png)