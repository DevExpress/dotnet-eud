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

Format rules used in conditional formatting can be categorized as follows:
* **Value** - Compares static values (Greater Than, Less Than, Between, etc.).
* **Top-Bottom** - Highlights a specific number of top/bottom values (Top N, Bottom N).
* **Average** - Highlights values above or below the average value.
* **A Date Occurring** - Highlights date-time values that are within a specified interval.
* **Expression** - Uses complex conditions to apply formatting. You can also pass dashboard parameters to expressions.
* **Icon and Color Ranges** - Display a specific icon based on a value range. You can select a predefined set of icons or apply a specific icon to each range.
* **Color Ranges** - Apply specific colors to different value ranges. You can select a predefined set of colors or use custom appearance settings to highlight values within specified ranges.
* **Gradient Ranges** - Allows you to apply formatting using gradient color scales.
* **Bar** - Allows you to visualize numeric values using bars. You can also color bars corresponding to positive and negative values using different colors.
* **Bar Color Ranges** - Allows you to visualize numeric values using bars whose colors are contained in the specified color set.
* **Bar Gradient Ranges** - Allows you to visualize numeric values using bars whose colors are contained in the specified color gradient.

You can use [measure or dimension](../binding-dashboard-items-to-data/binding-dashboard-items-to-data-in-the-web-dashboard.md) values to calculate a format rule. For a Card dashboard item, you can also calculate format rules by [delta](../designing-dashboard-items/cards/delta.md) values.

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
	* **Value** (with the condition type set to _Equal To_, _Not Equal To_ or _Text that Contains_)
	* **Expression**
* date-time 
	* **Value**
	* A **Date Occurring** (for dimensions with a continuous date-time group interval)
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

See the following topics for more information about specific format settings for dashboard items:

* [Conditional Formatting - Grid](../designing-dashboard-items/grid/conditional-formatting.md)
* [Conditional Formatting - Pivot](../designing-dashboard-items/pivot/conditional-formatting.md)
* [Conditional Formatting - Card](../designing-dashboard-items/cards/conditional-formatting.md)

## Edit a Format Rule

You can see existing format rules for an entire dashboard item. To do this, open the dashboard item's [Options](../ui-elements/dashboard-item-menu.md) menu and go to the **Conditional Formatting** section.

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
