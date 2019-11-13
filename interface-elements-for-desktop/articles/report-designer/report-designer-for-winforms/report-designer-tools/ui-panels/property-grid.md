---
title: Property Grid
---
# Property Grid

The **Property Grid** allows you to access and customize report/report element settings.

![WinFormsPropertyGrid](../../../../../images/eurd-win-WinFormsPropertyGrid.png)

## Select a Report Element

Perform one of the following actions to select an element and show its properties in the Property Grid:

* Select an element in the drop-down list at the top of the Property Grid.

	![WinFormsPropertyGrid-SelectControl](../../../../../images/eurd-win-PropertyEditor-SelectControl.png)

* Click an element in the [design surface](../../first-look-at-the-report-designer.md).
* Select an element in the [Report Explorer](report-explorer.md).

## Property Grid Tabs

The Property Grid displays properties in tabs. The active tab is activated at the application's next start.

![WinFormsPropertyGrid-Tabs](../../../../../images/eurd-win-PropertyGrid-Tabs.png)

## Favorite Properties

The **Favorites** tab displays favorite or most frequently used properties.

![WinFormsPropertyGrid-Tabs](../../../../../images/eurd-win-PropertyGrid-Favorites.png)

Click the **Edit Favorite Properties** context menu item to set up the favorite properties. In the invoked **Favorite Properties Editor**, enable check boxes for the controls' properties to include these properties into the favorite list.

![](../../../../../images/eurd-win-favorite-properties-editor.png)

## Change Property Values

The Property Grid adds a green property marker to properties if their default value changes.

![WinFormsPropertyGrid-GreenMarks](../../../../../images/eurd-win-PropertyGrid-GreenMarks.png)

Right-click a property's editor to reset the value.

![WinFormsPropertyGrid-ResetValue](../../../../../images/eurd-win-FormsPropertyGrid-ResetValue.png)

## Set Color Properties

You can use the Magnifier to set color properties.

![](../../../../../images/eurd-win-magnifier-button.png)

Do the following to use the Magnifier:

- Click the Magnifier button.
- Move the invoked Magnifier on the screen to find the color you want to set.

	![](../../../../../images/eurd-win-magnifier-get-color.png)

	You can use the Magnifier to zoom out. Use one of the following options to do this:

	- Hold Ctrl and press + / -
	- Scroll the mouse wheel

- Click to set the color property to the selected color.

	![](../../../../../images/eurd-win-magnifier-set-color.png)

Right click to cancel the Magnifier mode.

## Specify Expressions

If [expression bindings](../../bind-to-data/data-binding-modes.md) are enabled, the Property Grid allows you to specify expressions that can include two or more data fields and various functions. Click a property's marker to see whether the invoked context menu has the **PropertyName Expression** item.

![WinFormsPropertyGrid-Expression](../../../../../images/eurd-win-PropertyGrid-Expression.png)

Click this item to specify an expression in the invoked Expression Editor.

![WinFormsPropertyGrid-ExpressionEditor](../../../../../images/eurd-win-PropertyGrid-ExpressionEditor.png)

The Property Grid highlights properties that have an assigned expression.

![WinFormsPropertyGrid-ExpressionMark](../../../../../images/eurd-win-PropertyGrid-ExpressionMark.png)

Click a property's marker and choose **Reset** to reset the property value.

![WinFormsPropertyGrid-ResetExpression](../../../../../images/eurd-win-PropertyGrid-ResetExpression.png)

> [!Note]
> The **Reset** command resets both the expression and the value you specified using the property editor.

## Search Properties

The Property Grid's search box allows you to search for a property. When you type within the search box, the Property Grid automatically creates a search criteria based on the entered text and filters the list of available properties.

![WinFormsPropertyGrid-Search](../../../../../images/eurd-win-PropertyGrid-Search.png)

If you type two substrings separated by a space character, these substrings are considered as individual conditions combined by the OR logical operator. To find properties that contain both substrings (to use the AND logical operator), enclose the entered string in quotation marks.

## Non-Tabbed View

![Property-Grid-NonTabbed-View](../../../../../images/eurd-win-property-grid-nontabbed-view.png)

The non-tabbed view allows users to switch between categorized and alphabetical modes.

  ![Categorized-Alphabetical-Mode-Switchers](../../../../../images/eurd-win-propertygrid-nontabbed-modeswitchers.png)

  - In the categorized mode, properties are listed in a tree-like form.

    ![Categorized-Mode](../../../../../images/eurd-win-propertygrid-nontabbed-categorized.png)

  - In the alphabetical mode, all properties are displayed in a single list and are sorted alphabetically by name.

    ![Alphabetical-Mode](../../../../../images/eurd-win-propertygrid-nontabbed-alphabetical.png)