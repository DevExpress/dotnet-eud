---
title: Sort a Report in Print Preview
---
# Sort a Report in Print Preview

This tutorial illustrates how to enable sorting report data in Print Preview.

In this tutorial, we will start with the following report displaying products [grouped param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  by category names.

![eurd-win-interactive-sorting-starting](..\/..\/..\/images/eurd-win-interactive-sorting-starting.png)

You can implement interactive sorting for both the detail data and report groups.

## <a name="sortreportgroups"></a>Sort Report Groups
To enable sorting report groups in Print Preview, select the label displaying product category names located in the **Group Header** band and switch to the [Property Grid param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } .

![eurd-win-interactive-sorting-for-groupsr](..\/..\/..\/images/eurd-win-interactive-sorting-for-groups.png)

Expand the label's **InteractiveSorting** property, and set the **TargetBand** property to *GroupHeader1* and **FieldName** to *CategoryName*.

Switch to the **Preview** tab to sort report groups by the **CategoryName** field. When a mouse pointer hovers over the category name, it changes to a hand indicating the sorting capability. The arrow displayed at the element's right edge indicates the sorting order.

![ieurd-win-interactive-sorting-groups-result](..\/..\/..\/images/ieurd-win-interactive-sorting-groups-result.png)

## <a name="sortdetaildata"></a>Sort Detail Data
To enable sorting data in the Detail band, select the table cell displaying the **Product Name** title and switch to the [Property Grid param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } .

![eurd-win-interactive-sorting-detail](..\/..\/..\/images/eurd-win-interactive-sorting-detail.png)

Set the **TargetBand** property to *Detail* and access the **SortField** property.

In the invoked collection editor, add a new group field and set its **FieldName** to **ProductName**.

Set the table cell's **FieldName** property to the **ProductName** field.

![eurd-win-interactive-sorting-detail-field-name](..\/..\/..\/images/eurd-win-interactive-sorting-detail-field-name.png)

On switching to the Preview tab, you can now sort data in the Detail band by the **ProductName** field.

![eurd-win-interactive-sorting-detail-result](..\/..\/..\/images/eurd-win-interactive-sorting-detail-result.png)

If you provide interactive sorting to multiple fields, clicking another field clears all the previously applied data sorting. Hold the SHIFT key while clicking to preserve the existing sorting settings and thus sort against multiple fields.

To disable data sorting against a specific field, hold the CTRL key on its caption click.

> [!NOTE]
> Reports embedded into the current report using the [Subreport param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  control do not support interactive data sorting.