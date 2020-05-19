---
title: Conditional Formatting
author: Natalia Kazakova
legacyId: 117564
---
# Conditional Formatting
The Web Dashboard supports conditional formatting. You can apply a custom style to data elements that satisfy a certain condition. 

For more information about conditional formatting for different dashboard items, see the following topics:

* [Conditional Formatting - Grid](../designing-dashboard-items/grid/conditional-formatting.md)
* [Conditional Formatting - Pivot](../designing-dashboard-items/pivot/conditional-formatting.md)
* [Conditional Formatting - Card](../designing-dashboard-items/cards/conditional-formatting.md)

![wdd-cf-main](../../../images/img126130.png)

Format rules used in conditional formatting can be divided into the following groups:
* **Value** - Allows you to compare static values (such as Greater Than, Less Than, Between, etc.).
* **Top-Bottom** - Highlights a specific number of topmost/bottommost values.
* **Average** - Highlights values above the average value or below the average value.
* **A Date Occurring** - Allows you to highlight date-time values that fall into a specified interval.
* **Expression** - Allows you to use complex conditions to apply formatting. You can also pass dashboard parameters to expressions.
* **Icon and Color Ranges** - Allows you to apply formatting by displaying specific icons for different ranges of values. You can select a predefined set of icons or use a specific icon for each range.
* **Color Ranges** - Allows you to apply formatting using specific colors for different ranges of values. You can select a predefined set of colors or use custom appearance settings to highlight values within specified ranges.
* **Gradient Ranges** - Allows you to apply formatting using gradient color scales.
* **Bar** - Allows you to visualize numeric values using bars. You can also color bars corresponding to positive and negative values using different colors.
* **Bar Color Ranges** - Allows you to visualize numeric values using bars whose colors are contained in the specified color set.
* **Bar Gradient Ranges** - Allows you to visualize numeric values using bars whose colors are contained in the specified color gradient.

You can calculate a format rule using [measure or dimension](../binding-dashboard-items-to-data/binding-dashboard-items-to-data-in-the-web-dashboard.md) values. For the Card dashboard item, format rules also can be calculated by [delta](../designing-dashboard-items/cards/delta.md) values.

The table below lists format conditions that can be applied to different types of data items.
* numeric 
	* **Value**
	* **Top-Bottom**
	* **Average**
	* **Expression**
	* **Icon Ranges**
	* **Color Ranges**
	* **Gradient Ranges**
	* **Bar** <sup>1</sup>
	* **Bar Color Ranges** <sup>1</sup>
	* **Bar Gradient Ranges** <sup>1</sup>
* string 
	* **Value** with the condition type set to _Equal To_, _Not Equal To_ or _Text that Contains_
	* **Expression**
* date-time 
	* **Value**
	* A **Date Occurring** for dimensions with the continuous date-time group interval
	* **Expression**
	* **Icon and Color Ranges**
	* **Color Ranges**
	* **Gradient Ranges**
	* **Bar** <sup>1</sup>
	* **Bar Color Ranges** <sup>1</sup>
	* **Bar Gradient Ranges** <sup>1</sup>

	<sup>1</sup>  The Card dashboard item does not support these rules.

## Create a Format Rule

 To create a format rule, open the **Conditional Formatting** section in the dashboard item's [Options](../ui-elements/dashboard-item-menu.md) menu or in the [data item menu](../ui-elements/data-item-menu.md). Click "+" to add a new format rule:
	
![wed-dashboard-cf-add-rule](../../../images/wed-dashboard-cf-add-rule.png)

Specify the data item/card used to calculate a condition in the **Common** section. You can also create a format rule for one data item and apply different settings to the other data item. 

Select a format rule type from the list to open its settings.
	
![wdd-grid-cf-select-rule-type](../../../images/img126024.png)

Select a condition from the list and [specify its settings](#appearance-settings) in the **Condition** section. Available settings depend on the selected format rule.
	
![wdd-grid-cf-value-menu](../../../images/img126023.png)
	
Specify additional settings in the **Miscellaneous** section. For example, you can specify the intersection level for the Pivot or apply the current rule to a row in the Grid.

See the following topics for more information about specific formatting settings of the dashboard items:

* [Conditional Formatting - Grid](../designing-dashboard-items/grid/conditional-formatting.md)
* [Conditional Formatting - Pivot](../designing-dashboard-items/pivot/conditional-formatting.md)
* [Conditional Formatting - Card](../designing-dashboard-items/cards/conditional-formatting.md)

## Edit a Format Rule

You can see existing format rules for the entire dashboard item. To do this, open the dashboard item's [Options](../ui-elements/dashboard-item-menu.md) menu and go to the **Conditional Formatting** section.

![wdd-cf-all-rules](../../../images/img126046.png)

To edit a format rule, select the rule and click **Edit** (the ![wdd-icon-edit-collection-value-item](../../../images/img126050.png) icon).

Click **Delete** (the ![wdd-icon-delete-big](../../../images/img126104.png) icon) to delete the selected format rule.

When you edit a format rule, you can enable or disable the rule in the **Miscellaneous** section.

![](../../../images/web-conditional-formatting-edit-rule-miscellaneous-section.png)


## Appearance Settings

The format rule's menu **Condition** section contains appearance settings. You can configure and customize current format condition appearance settings:

* Choose a predefined background color or font in the **Appearance** tab.
	
	![wdd-cf-appearance-gallery](../../../images/img126044.png)
* Add a predefined icon in the **Icons** tab.
	
	![wdd-cf-icons-gallery](../../../images/img126045.png)

You can also customize predefined colors and values for each Range format rule.

![wdd-cf-range-gallery](../../../images/img126043.png)
