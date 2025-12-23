---
title: Filter Data at the Data Source Level
author: Anna Gubareva
---
# Filter Data at the Data Source Level

This tutorial illustrates how to filter data at the report data source level, as opposed to the [report level param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } . This approach is recommended when dealing with comparatively large data sources when the retrieval process is slow.

1. [Create a new report param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  or open an existing one.

2. Bind you report to a required data source. See the [Bind to Data param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  section to learn more about providing data to reports.

3. Switch to the [Field List param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  and drop the required fields onto the report's [Detail param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  band.

    ![](..\/..\/..\/..\/images/eurd-win-filter-data-drop-fields.png)



4. Select the data source in the [Report Explorer param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } , expand its **Queries** collection property in the [Property Grid param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  and click the ellipsis for the **Filter String** property of the required query.

    ![](..\/..\/..\/..\/images/eurd-win-filer-data-source-filter-string-property.png)

5. <!-- In the invoked [Filter Editor param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } , --> Construct an expression where the data fields are compared with the required values as shown below.

    ![](..\/..\/..\/..\/images/eurd-win-filer-data-source-filter-string.png)

    Every filter condition consists of three parts:
    * A data field name.
    * Criteria operator, such as **Equals**, **Is less than**, **Is between**, etc.
    * A static operand value, another data field or a query parameter. See the [Specify Query Parameters param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  topic to learn about embedding these parameters into filter conditions.

    You can arrange specific conditions into groups with **And**, **Or**, **Not And**, and **Not Or** operators.

    Alternatively, you can specify a filter expression when creating a query using the [Query Builder param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } . To invoke the **Filter Editor** at this stage, click the **Filter...** button.

Switch to [Print Preview param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  to see the result.

![](..\/..\/..\/..\/images/eurd-win-filer-data-source-result.png)
