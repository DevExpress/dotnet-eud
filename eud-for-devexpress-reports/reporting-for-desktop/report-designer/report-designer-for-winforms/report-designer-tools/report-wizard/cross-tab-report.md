---
title: Cross-Tab Report
---
# Cross-Tab Report

Select **Cross-Tab Report** on the wizard's [start page param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  to create a [cross-tab report param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  that displays multi-dimensional data.

![](..\/..\/..\/..\/images/eurd-win-cross-tab-report-wizard-select-report-type.png)

Click **Next** and use the [Data Source Wizard param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  to set up a report's data source.

Once the data source is configured, you can define the report's layout on the next page. Drop data fields onto the following cross-tab area:

* **Rows** - defines row headers;
* **Columns** - defines column headers;
* **Data** - defines fields against which to calculate summaries.

![](..\/..\/..\/..\/images/eurd-win-cross-tab-report-wizard-drop-fields.png)

You can also select a field from the corresponding drop-down list.

![](..\/..\/..\/..\/images/eurd-win-cross-tab-report-wizard-drop-down-list.png)

> [!Note]
> The field order defines the hierarchy in the resulting cross-tab report. The higher the field on the list, the higher the level in the field hierarchy.

You can click **Finish** to stop the Report Wizard. If you want to customize the report further, click **Next** and proceed to the next pages:

* [Specify Report Page Settings param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } 
* [Choose a Report Color Scheme param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } 
* [Set the Report Title param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } 

The generated report contains the [Cross Tab param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  control that is configured based on the specified settings. The XRCrossTab control calculates automatic totals and grand totals across row and column fields.

![](..\/..\/..\/..\/images/eurd-win-report-wizard-cross-tab-result.png)