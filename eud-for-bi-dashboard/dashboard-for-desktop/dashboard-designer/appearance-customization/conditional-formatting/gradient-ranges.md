---
title: Gradient Ranges
author: Natalia Kazakova
legacyId: 114190
---
# Gradient Ranges
Gradient Ranges allow you to use predefined color gradients to apply conditional formatting to different ranges of values. You can also use specific colors to generate custom gradients.

To format values according the required condition, click the measure menu button, select **Add Format Rule | Color Ranges** and choose the required color gradient.

![GradientRanges_Menu](../../../images/img118675.png)

This invokes the **Gradient Ranges** dialog containing the set of value ranges and corresponding appearance settings. The Grid dashboard item on the right displays the default formatting applied using the predefined Red-Blue gradient.

![GradientRangeDialog](../../../images/img118676.png)

This dialog allows you to change the following options specific to Gradient Ranges.
* **Number of ranges** allows you to specify the number of ranges used to classify values. Click the **Generate Ranges** button to generate a new gradient scale according to the specified number of ranges.
* The **Use % ranges** check box specifies whether the percent or absolute scale is used to generate ranges.
	
	> [!NOTE]
	> Note that this option is not available for date-time dimensions.
* To change the specific color in the gradient, click the button next to the required color and select a new color or specify a custom background color. This allows you to create a color gradient based on more than two colors. In this case, the specified colors are marked with an empty square.
	
	![GradientRangeDialog_ChangeColor](../../../images/img118677.png)
	
	To learn how to specify a custom color, see the **Specify Appearance Settings** paragraph in the [Conditional Formatting](../conditional-formatting.md) topic.
* You can change range boundaries by specifying the required values.
	
	![GradientRangeDialog_ChangeRangeStop](../../../images/img118678.png)
	
	> [!NOTE]
	> Note that a new value should fall into a range between corresponding values of the previous and next range.
* To change the comparison logic for the required range, click the comparison sign and select the required option.
	
	![GradientRangeDialog_ChangeComparisonLogic](../../../images/img118679.png)
	
	The _greater or equal_ sign includes the smallest value in the current interval while the _greater_ sigh excludes the smallest value from the current interval and includes it in the next interval.