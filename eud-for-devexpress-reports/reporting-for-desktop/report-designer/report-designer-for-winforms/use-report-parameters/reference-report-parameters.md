---
title: Reference Report Parameters
author: Eugene Polevikov
---

# Reference Report Parameters

After you [create a report parameter param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } , you can reference this parameter in the [report's filter string](#reference-in-a-reports-filter-string), [in expressions](#reference-in-expressions), and [in a control's Text property](#reference-in-a-controls-text-property). You can also bind control and data source parameters to report parameters. Refer to the sections below for more details.

## Reference in a Report's Filter String

You can reference a report parameter in the report's filter string. This allows you to conditionally filter the report's data loaded from a data source.

![reference parameter in report filter string](..\/..\/..\/images/reference-parameter-in-report-filter-string.png)

> [!TIP]
> When you use a report's filter string to filter data, all the data is loaded from a data source before the filter is applied. If you use a large dataset, filter data at the data source level. Refer to the following topic for more information: [Filter Data at the Data Source Level param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } . 

## Reference in Expressions

You can reference a report parameter in [expressions param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  of [controls param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  and [calculated fields param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } .

![Reference report parameters in expressions](..\/..\/..\/images/report-parameters-reference-in-expression.png)

This allows you to conditionally change the data a control or calculated field displays.

You can use the [Field List param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  to create an [Label param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  control that displays only a parameter value. To do this, drag the parameter from the **Field List** and drop it onto the report's band.
 
![Drag and drop a report parameter](..\/..\/..\/images/reference-parameter-drag-and-drop.png)

You can also use parameters in expressions to specify the visibility of a report's bands or conditionally change a control's appearance.

![Reference parameters in the Expression Editor](..\/..\/..\/images/parameters-expression-editor.png)

Refer to the following topics for more information:

* [Conditionally Change a Band's Visibility param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } 
* [Conditionally Change a Control's Appearance param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } 

## Reference in a Control's Text Property

You can use a report parameter in a control's **Text** property.

![Reference a parameter in a control's Text property (Designer)](..\/..\/..\/images/report-parameters-reference-in-text-property.png)

This allows you to create a placeholder (embedded field) that is substituted by a parameter value. 

![Reference a parameter in a control's Text property (Preview)](..\/..\/..\/images/report-parameters-reference-in-text-preview.png)

Refer to the following topic for information on embedded fields: [Use Embedded Fields (Mail Merge) param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } .

## Bind Control Parameters to Report Parameters

You can create parameters for the [CrossTab param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  and [Chart param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  controls and bind these parameters to report parameters. This allows you to conditionally filter data at the control level. Refer to the following topic for details on how to filter data for the **Сhart** control: [Use Charts to Visualize Grouped Data param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } .

You can also specify a parameter for the [Subreport param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  control and bind this parameter to report parameters. This allows you to pass parameter values from the main report to the subreport and conditionally change the subreport's data and appearance.
 
## Bind Data Source Parameters to Report Parameters

You can create parameters for data sources and bind them to report parameters. The table below contains information about which tasks this allows you to solve, a data source for which the task can be solved, and links to documentation sections you can reference for details.

| Task | Data Source | Documentation |
| --- | --- | --- |
| **Filter data at the data source level** | SQL Data Source <br> Entity Framework Data Source <br> MongoDB Data Source | [Bind a Report to a Database param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  <br> [Bind a Report to an Entity Framework Data Source param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  <br> [Bind a Report to a MongoDB Instance param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  |
| **Pass report parameters to a stored procedure** | SQL Data Source <br> Entity Framework Data Source | [Specify Query Parameters param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  <br> [Bind a Report to an Entity Framework Data Source param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  |
| **Pass report parameters to a method that loads data** | Object Data Source | [Bind a Report to an Object Data Source param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  |

When you bind a report to the JSON Data Source, you can specify a URI from which a JSON file should be loaded. You can bind path parameters, query parameters, and header parameters to report parameters to conditionally configure HTTP requests to the web service endpoint. Refer to the following topic for details: [Bind a Report to JSON Data param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } .