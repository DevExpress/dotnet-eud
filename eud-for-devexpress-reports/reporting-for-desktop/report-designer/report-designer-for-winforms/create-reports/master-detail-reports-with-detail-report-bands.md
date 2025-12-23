---
title: Master-Detail Reports with Detail Report Bands
author: Anna Gubareva
---
# Master-Detail Reports with Detail Report Bands

This tutorial illustrates how to display hierarchical data in a master-detail report using nested [Detail Report bands param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } . This approach is effective if your data source contains master-detail relationship. Another way is described at [Master-Detail Reports with Subreports param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } .

1. [Create a new report param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  or [open an existing one param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } .

2. [Bind the report param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  to a required data source and provide it with a master-detail relationship as described in the [Bind a Report to a Database param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  topic.

3. Drop the required data fields from the [Field List param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  onto the [Detail param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  band.

    ![](..\/..\/..\/images/eurd-win-master-detail-drop-fields-for-master-layout.png)

4. Create a [Detail Report Band param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  by right-clicking the report's surface. In the invoked context menu, select **Insert Detail Report**, and then, select the master-detail relationship's name.

    ![](..\/..\/..\/images/eurd-win-master-detail-insert-detail-report-band.png)

    This sets the detail report's **Data Source** and **Data Member** properties automatically.

    ![](..\/..\/..\/images/eurd-win-master-detail-data-member-property.png)

5. Switch to the **Field List**, select the data fields while holding down CTRL or SHIFT and drag-and-drop them onto the Detail band.

    ![](..\/..\/..\/images/eurd-win-master-detail-drop-fields-for-detail-layout.png)

    > [!NOTE]
    > You should drag-and-drop fields from the category corresponding to the master-detail relationship to correctly generate the detail report's data. Otherwise, the report will display only the first record of the detail table as many times as there are records in this table.

6. If required, customize the report's [appearance param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  and [format values param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } .

Switch to [Print Preview param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  to see the resulting report.

![](..\/..\/..\/images/eurd-win-master-detail-result.png)