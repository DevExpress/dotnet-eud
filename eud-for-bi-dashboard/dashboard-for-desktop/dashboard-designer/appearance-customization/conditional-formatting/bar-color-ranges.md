---
title: Bar Color Ranges
author: Natalia Kazakova
legacyId: 115243
---
# Bar Color Ranges
Bar Color Ranges allow you to visualize numeric values using bars whose colors are contained in the specified color set.

To format values according the required condition, click the data item menu button, select **Add Format Rule | Bar Color Ranges** and choose the required color set.

![BarColorRanges_Menu](../../../images/img120036.png)

This invokes the **Color Range Bar** dialog containing the set of value ranges and corresponding colors. The Grid dashboard item on the right displays the default formatting applied using the predefined set of 3 colors.

![ConditionalFormatting_ColorRangeBarDialog](../../../images/img120018.png)

This dialog allows you to change the following options specific to Bar Color Ranges.
* The **Format Style** combo box allows you to change the color set used to apply formatting.
* The **Use % ranges** check box specifies whether the percent or absolute scale is used to generate ranges.
	
	> [!NOTE]
	> Note that this option is not available for numeric dimensions.
* To change the appearance settings applied to values corresponding to the specified range, click the button next to the required color and select a new color or specify custom appearance settings. To learn how to specify custom settings, see the **Specify Appearance Settings** paragraph in the [Conditional Formatting](../conditional-formatting.md) topic.
	
	![BarColorRangeDialog_ChangeAppearance](../../../images/img120019.png)
	
	Select **No Style** to disable the indication for the required range.
* You can change range boundaries by specifying the required values.
	
	![ColorRangeSetDialog_ChangeRangeStop](../../../images/img118669.png)
	
	> [!NOTE]
	> Note that a new value should fall into a range between corresponding values of the previous and next range.
* To change the comparison logic for the required range, click the comparison sign and select the required option.
	
	![ColorRangeSetDialog_ChangeComparisonLogic](../../../images/img118670.png)
	
	The _greater or equal_ sign includes the smallest value for the current interval, while the _greater_ sign excludes the smallest value from the current interval and includes it in the next interval.
* Use the **Add** and **Delete** buttons to add new ranges or delete the selected range respectively.