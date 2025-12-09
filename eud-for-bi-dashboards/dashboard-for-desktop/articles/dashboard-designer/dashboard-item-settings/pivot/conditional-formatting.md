---
title: Conditional Formatting
author: Natalia Kazakova
legacyId: 114225
---
# Conditional Formatting

A Pivot dashboard item applies conditional formatting to cell values. You can calculate a format rule by measures placed in the **Values** section and dimensions placed in the **Columns** or **Rows** section.

> [!NOTE]
> Note that you can use [hidden measures](../../bind-dashboard-items-to-data/hidden-data-items.md) to specify a condition used to apply formatting to visible values.

![pivot-with-applied-format-rules](../../../../images/pivot-with-applied-format-rules.png)

## Supported Format Rules

The following list contains available format rules and corresponding data types:
* numeric
	* [Value](../../appearance-customization/conditional-formatting/value.md)
	* [Top-Bottom](../../appearance-customization/conditional-formatting/top-bottom.md)
	* [Average](../../appearance-customization/conditional-formatting/average.md)
	* [Expression](../../appearance-customization/conditional-formatting/expression.md)
	* [Icon Ranges](../../appearance-customization/conditional-formatting/icon-ranges.md)
	* [Color Ranges](../../appearance-customization/conditional-formatting/color-ranges.md)
	* [Gradient Ranges](../../appearance-customization/conditional-formatting/gradient-ranges.md)
	* [Bar](../../appearance-customization/conditional-formatting/bar.md) 
	* [Bar Color Ranges](../../appearance-customization/conditional-formatting/bar-color-ranges.md) 
	* [Bar Gradient Ranges](../../appearance-customization/conditional-formatting/bar-gradient-ranges.md) 
* string 
	* [Value](../../appearance-customization/conditional-formatting/value.md) (with a condition type set to _Equal To_, _Not Equal To_ or _Text that Contains_)
	* [Expression](../../appearance-customization/conditional-formatting/expression.md)
* date-time
	* [Value](../../appearance-customization/conditional-formatting/value.md)
	* [A Date Occurring](../../appearance-customization/conditional-formatting/value.md) (for dimensions with a continuous date-time group interval)
	* [Expression](../../appearance-customization/conditional-formatting/expression.md)
	* [Icon Ranges](../../appearance-customization/conditional-formatting/icon-ranges.md)
	* [Color Ranges](../../appearance-customization/conditional-formatting/color-ranges.md)
	* [Gradient Ranges](../../appearance-customization/conditional-formatting/gradient-ranges.md)
	* [Bar](../../appearance-customization/conditional-formatting/bar.md) 
	* [Bar Color Ranges](../../appearance-customization/conditional-formatting/bar-color-ranges.md) 
	* [Bar Gradient Ranges](../../appearance-customization/conditional-formatting/bar-gradient-ranges.md) 

## Create and Edit a Format Rule

You can create and edit format rules in the following ways:

* Click the **Edit Rules** button on the **Home** ribbon tab. 

* Click the measure/dimension menu button in the Data Item's pane and select **Add Format Rule**/**Edit Rules**. 

Refer to the following topic for information on how to create and edit format rules: [Conditional Formatting Common](../../appearance-customization/conditional-formatting.md).

## Pivot-Specific Format Condition Settings

You can configure and customize current format condition appearance settings.

* Choose a predefined background color/font or click an empty square to add a new preset in the **Appearance** tab.

	![NewRuleDialog_AppearanceTab](../../../../images/img118585.png)

* Add a predefined icon in the **Icons** tab.	 

The **Appearance** tab contains the following Pivot-specific settings:

| Option | Description |
| --|--|
| **Enabled** | Enables/disables the current format rule. |
| **Intersection Mode** | Specifies the level at which to apply conditional formatting to pivot cells. |  
| **Intersection Row/Column Dimension**  | Applies the format rule to the specified row/column dimension, if you select the _Specific Level_ as the intersection mode.|
| **Apply to Row/Column** | Specifies whether to apply the formatting to the Pivot item's entire row/column.

A Pivot item allows you to specify the field intersection to which a format rule is applied.

| Intersection Level Mode| Description |
| --|--|
| _Auto_ | Identifies the default level. For the Pivot dashboard item, _Auto_ identifies the First Level. |
| _First Level_ |The first level values are used to apply conditional formatting. |
| _Last Level_ | The last level values are used to apply conditional formatting. |
| _All Levels_ | All pivot data cells are used to apply conditional formatting. |
| _Specific Level_ | The specified measures/dimensions are used to apply conditional formatting. |


The image below displays different intersection levels with the applied conditional format rule:

![winforms_pivot_intersection_level_mode](../../../../images/winforms_pivot_intersection_level_mode.png)

To apply a format rule to the row or column Grand Total, change the **Intersection Level Mode** to _Specific level_ and set the _[Grand Total]_ value as the intersection row/column dimension.  

Note the following limitations:

1. The dashboard cannot calculate conditional formatting in a Pivot item for multiple range levels with _percentage_ values. In this case, the "All Levels" intersection mode is not available for a conditional formatting rule.
2. The format condition dialog does not contain any Pivot-specific settings for a dimension from **Columns** and **Rows**.
