---
title: Table Reports
author: Anna Vekhina
---
# Table Reports

This tutorial describes how to create a data-bound report displaying information in a tabular format. Table reports should not be confused with hierarchical [master-detail reports param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } , nor with [cross-tab reports param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } .

![](..\/..\/images/eurd-web-table-report-result.png)

1. [Create a new report param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  or [open an existing one param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } .

2. [Bind the report param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  to a required data source.

3. Add the [Page Header param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  band to the report to print the column headers at the top of every document page. To do this, from the report's context menu, select the **Insert Page Header Band** command.

    ![](..\/..\/images/eurd-web-table-report-insert-page-header.png)

4. Drop the [Table param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  control from the [Toolbox param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  onto the Page Header band and specify columns' text to create column headers.

    ![](..\/..\/images/eurd-web-table-report-add-static-captions.png)

5. To provide dynamic content to the report, switch to the [Field List param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } , select data fields and drop them onto the Detail band.

    ![](..\/..\/images/eurd-web-table-report-add-dynamic-content.png)

    This creates a table with the same number of cells as the number of fields selected with each cell bound to the appropriate data field.

6. Click an empty place on the report's surface and draw a rectangle around the table to select it. 

    ![](..\/..\/images/eurd-web-table-report-select-both-tables.png)

7. Expand the **Appearance** category and specify the **Font**, **Text Alignment** and **Borders** properties to customize the tables' appearance.

    ![](..\/..\/images/eurd-web-table-report-set-up-appearance.png)

8. Define a currency format for the **UnitPrice** cell. Select the cell and click the **Text Format String** property's ellipsis button. Select the appropriate format in the invoked **Format String Editor** editor and click **OK**.

    ![](..\/..\/images/eurd-web-table-report-format-string.png)

9.  To further improve the table readability, you can apply different visual styles to its odd and even rows. See [Report Visual Styles param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  to learn more. 

    ![](..\/..\/images/eurd-web-table-report-odd-even-styles.png)
	
	See the [Use Tables param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  section to learn how to add or remove the table's rows and cells, as well as convert the table's cells to separate label controls.

Switch to [Print Preview param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  to see the resulting report.

![](..\/..\/images/eurd-web-table-report-result.png)