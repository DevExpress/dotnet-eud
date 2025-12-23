---
title: Use Report Parameters
author: Sergey Andreev
---

# Use Report Parameters

Report parameters allow you to filter report data dynamically.

![Report parameters example](..\/..\/images/report-parameters-example.gif)

## Supported Features/Capabilities

* Built-in parameter types (String, Date, Number, Boolean, and GUID)

    ![Built-in parameter types](..\/..\/images/built-in-parameter-types.png)

* [Multi-value parameters param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  (filter report data against multiple criteria)

    ![Multi-value report parameters](..\/..\/images/parameter-editor-multiple-values.png)

* [Cascading parameters param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  (filter a parameter’s value list against selections made in a different parameter)

    ![Cascading report parameters](..\/..\/images/cascadingparametersresult124540.png)

* [Date-range parameters param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  (filter report data against a specified time period)

    ![Date-range report parameters](..\/..\/images/date-range-report-parameters.png)

* [Static parameter values param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  (create pre-defined (static) parameter value lists)

    ![Static parameter values](..\/..\/images/static-parameter-values.png)

* [Dynamic parameter values param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  (load parameter values from a data source dynamically)

    ![Dynamic parameter values](..\/..\/images/dynamic-parameter-values.png)

Refer to the following documentation section for more details: [Create a Report Parameter param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } .

## Reference Report Parameters

Once you [create param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  a parameter, you can reference it in your report’s [filter string param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  to filter underlying report data.

![Reference parameter in report filter string](..\/..\/images/reference-parameter-in-report-filter-string.png)

You can also reference the parameter in a report control’s [expression param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  or its **Text** property.

![Reference report parameter in a control's expression](..\/..\/images/report-parameters-reference-in-expression.png)

When used in this manner, you can filter data displayed within an individual report control (such as [Label param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } ) conditionally.

You can also bind data source parameters to report parameters and filter data at the data source level. Refer to the following help topic for more information: [Reference Report Parameters param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } .

## Specify Parameter Values

Available report parameters appear within a report’s **Print Preview** window (inside the [Parameters panel param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } ). Use this panel to specify desired parameter values:

![Specify parameter values in the Parameters Panel](..\/..\/images/parameters-panel.png)
