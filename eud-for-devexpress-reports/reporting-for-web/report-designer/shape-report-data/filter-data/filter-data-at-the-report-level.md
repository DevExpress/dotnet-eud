---
title: Filter Data at the Report Level
author: Anna Vekhina
---
# Filter Data at the Report Level

This tutorial illustrates how to filter data at the report level, as opposed to the [data source level param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } . This approach is useful when dealing with relatively small data sources, when data load times are acceptable.

1. [Create a new report param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  or open an existing one.

2. Bind you report to a required data source. See the [Bind to Data param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  section to learn more about providing data to reports.

3. Switch to the [Field List param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  panel and drop the required fields onto the report's [Detail param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  band.

    ![](..\/..\/..\/images/eurd-web-filter-data-drop-fields.png)

4. Expand the **Tasks** category and click the **Filter String** property's ellipsis button.

    In the invoked [Filter Editor param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } , construct an expression in which the data fields are compared with the required values.

    ![](..\/..\/..\/images/eurd-web-filter-data-report-level-filter-string.png)

    Every filter condition consists of three parts:
    * A field of a data source to which a report is bound or the name of the [calculated field param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } , which exists in this data source at the same level.
    * Criteria operator, such as **Equals**, **Is less than**, **Is between**, etc.
    * A static operand value, another data field or a [report parameter param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } . To access parameters, click the icon on the right until it turns into a question mark.

    You can arrange specific conditions into groups with **And**, **Or**, **Not And**, and **Not Or** operators.

Your report is now ready to be generated. Switch to [Print Preview param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  to see the result.

![](..\/..\/..\/images/eurd-web-filter-data-report-level-result.png)