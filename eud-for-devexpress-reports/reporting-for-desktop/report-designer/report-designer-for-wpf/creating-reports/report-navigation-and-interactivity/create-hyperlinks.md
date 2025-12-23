---
title: Create Hyperlinks
author: Anna Gubareva
legacyId: 116344
---
# Create Hyperlinks
This tutorial demonstrates how to embed a _hyperlink_ into your report. In this case, a label behaves as a hyperlink in a report's [Print Preview param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } ,  and when the report is exported to PDF, HTML, MHT, RTF, XLS and XLSX formats.

To insert a hyperlink into your report, do the following.
1. [Create a new report param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } .
2. Drop a [Label param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  onto the report, and in the [Properties Panel param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } , change its **Text** to the one required for the link.
	
	![EUD_WpfReportDesigner_Hyperlink_1](..\/..\/..\/..\/images/img123683.png)
3. Then, set the **Navigation Target** to the required value (__blank_, __parent_, __search_, __self_, or __top_), and define the required **Navigation URL**.
	
	![EUD_WpfReportDesigner_Hyperlink_2](..\/..\/..\/..\/images/img123684.png)
4. In addition, to make the label look like a typical link, you can change its appearance appropriately (e.g., make it blue and underlined).

The hyperlink is now ready. Switch to the [Print Preview param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  tab and view the result.

![EUD_WpfReportDesigner_Hyperlink_Result](..\/..\/..\/..\/images/img123685.png)