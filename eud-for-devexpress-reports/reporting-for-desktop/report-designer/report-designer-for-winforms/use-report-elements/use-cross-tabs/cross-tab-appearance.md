---
title: Cross Tab Appearance
author: Sergey Andreev
---
# Cross Tab Appearance

## Customize Appearance

After you drop the Cross Tab from the Toolbox onto a report or finish the Cross-Tab Report Wizard, 4 predefined [report styles param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  are created and assigned to the Cross Tab's **Styles**.

![](..\/..\/..\/..\/images/eurd-win-cross-tab-crosstabstyles-property.png)

Use the **General Style** property to specify common appearance settings that apply to all Cross Tab cells.

Use the **Header Area Style**, **Data Area Style** and **Total Area Style** properties to customize appearance settings of specific areas shown below.

![](..\/..\/..\/..\/images/eurd-win-cross-tab-styles-areas.png)

If an area's appearance option is not set, its value is inherited from the general style.

You can also override appearance settings of each Cross Tab cell. These settings have a higher priority over style settings.

![](..\/..\/..\/..\/images/eurd-win-cross-tab-cells-appearance-properties.png)

## Customize Appearance Conditionally

Specify [expression bindings param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  to change a cell's appearance based on a specific condition. You can use the **GroupRowIndex** and **GroupColumnIndex** arguments to identify group indexes (for instance, to define the background color for odd and even rows).

![](..\/..\/..\/..\/images/eurd-win-cross-tab-cell-back-color-expression.png)

Expressions are evaluated when a report is previewed. The calculated appearance settings have the highest priority. They override a cell's appearance settings and style settings.

![](..\/..\/..\/..\/images/eurd-win-cross-tab-cell-back-color-expression-result.png)
