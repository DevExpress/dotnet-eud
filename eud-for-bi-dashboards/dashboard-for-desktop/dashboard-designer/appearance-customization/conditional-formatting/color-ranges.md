---
title: Color Ranges
author: Natalia Kazakova
legacyId: 114209
---
# Color Ranges
Color Ranges allow you to use predefined sets of colors to apply conditional formatting to different ranges of values. You can also use custom appearance settings for specific ranges.

To format values according the required condition, click the data item menu button, select **Add Format Rule | Color Ranges** and choose the required icon set.

![ColorRanges_Menu](../../../images/img118665.png)

This invokes the **Range Set** dialog containing the set of value ranges and corresponding appearance settings. The Grid dashboard item on the right displays the default formatting applied using the predefined set of 3 colors.

![ColorRangeSetDialog](../../../images/img118666.png)

This dialog allows you to change the following options specific to Icon Ranges.
* The **Format Style** combo box allows you to change the color set used to apply formatting.
* The **Use % ranges** check box specifies whether the percent or absolute scale is used to generate ranges.
	
	> [!NOTE]
	> Note that this option is not available for date-time dimensions.
* To change the appearance settings applied to values corresponding to the specified range, click the button next to the required color and select a new color or specify custom appearance settings. To learn how to specify custom settings, see the **Specify Appearance Settings** paragraph in the [Conditional Formatting](../conditional-formatting.md) topic.
	
	![ColorRangeSetDialog_ChangeAppearance](../../../images/img118667.png)
	
	Select **No Style** to disable the indication for the required range.
* You can change range boundaries by specifying the required values.
	
	![ColorRangeSetDialog_ChangeRangeStop](../../../images/img118669.png)
	
	> [!NOTE]
	> Note that a new value should fall into a range between corresponding values of the previous and next range.
* To change the comparison logic for the required range, click the comparison sign and select the required option.
	
	![ColorRangeSetDialog_ChangeComparisonLogic](../../../images/img118670.png)
	
	The _greater or equal_ sign includes the smallest value for the current interval while the _greater_ sigh excludes the smallest value from the current interval and includes it in the next interval.
* Use the **Add** and **Delete** buttons to add new ranges or delete the selected range respectively.