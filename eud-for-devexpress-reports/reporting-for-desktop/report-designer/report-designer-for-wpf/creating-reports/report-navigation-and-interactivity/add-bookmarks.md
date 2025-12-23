---
title: Add Bookmarks
author: Anna Gubareva
legacyId: 116342
---
# Add Bookmarks
This tutorial describes the steps to create a report with _bookmarks_ (a so-called _Document Map_). This feature allows you to easily navigate through the report during [print preview param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } .

To demonstrate the Document Map feature, use a report with grouping, similar to the one created in the following tutorial: [Grouping Data param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } .

To create a report with bookmarks, do the following.
1. Select the label placed in the [Group Header band param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } , and in the [Properties Panel param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } , expand the **Data Bindings** property. As this control is bound to data, bind its **Bookmark** property to the same data field (in this example, **CategoryID**).
	
	![EUD_WpfReportDesigner_Bookmarks_1](..\/..\/..\/..\/images/img123675.png)
	
	Note that as with other bindable properties, you can also apply [value formatting param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  to the **Bookmark** property (e.g., **Category: {0}**).
2. In the same way, select the label in the Detail band and set its **Bookmark** property to the **ProductName** data field.
	
	![EUD_WpfReportDesigner_Bookmarks_2](..\/..\/..\/..\/images/img123676.png)
3. Then, for the same label, set the **Parent Bookmark** property to the Group Header's label to define the Document Map's hierarchy.
	
	![EUD_WpfReportDesigner_Bookmarks_3](..\/..\/..\/..\/images/img123677.png)
4. Finally, select the report itself and assign text to its **Bookmark** property, which determines the caption of the root node of the Document Map.
	
	![EUD_WpfReportDesigner_Bookmarks_4](..\/..\/..\/..\/images/img123678.png)

The report with bookmarks is now ready. Switch to the [Print Preview param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  tab and use the [Document Map Panel param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  to navigate through the report.

![EUD_WpfReportDesigner_Bookmarks_Result](..\/..\/..\/..\/images/img123679.png)