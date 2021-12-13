---
title: Properties Window
author: Anna Gubareva
legacyId: 116219
---
# Properties Window

Use the Properties window to view, discover, and change the properties of selected report [elements](../report-elements.md).

![Properties Window](../../../../images/eurd-wpf-properties-window.png)

Switch to the **View** ribbon tab, expand the **Windows** group, and click **Properties** to show or hide the Properties window.

![Invoke the Properties Window](../../../../images/eurd-wpf-invoke-properties-window.png)

## Select a Report Element

Do one of the following to select a report element and show its properties in the Properties window:

* Select a report element from the drop-down list at the top of the Properties window.

	![Select a Report Element from the Drop-Down List](../../../../images/eurd-wpf-properties-window-select-report-element.png)

* Click a report element on the [design surface](design-surface.md).

	![Click a Report Element on the Design Surface](../../../../images/eurd-wpf-properties-window-select-report-element-on-surface.png)

* Select a report element in the [Report Explorer](report-explorer.md).

	![Select a Report Element in the Report Explorer](../../../../images/eurd-wpf-properties-window-select-report-element-in-report-explorer.png)

## Category Tabs

The Properties window splits properties into category tabs and sorts them alphabetically.

![Category Tabs](../../../../images/eurd-wpf-properties-window-category-tabs.png)

## Favorite Properties

The Favorites tab contains the most used (or “favorite”) properties.

![The Favorites Tab](../../../../images/eurd-wpf-properties-window-favorite-tab.png)

Use the **Favorite Properties Editor** to add properties to the Favorites tab. Click the **Edit Favorite Properties...** menu item to open the **Favorite Properties Editor** that lists the report controls. Check/uncheck properties to modify these controls’ favorite property lists.

![The Favorite Properties Editor](../../../../images/eurd-wpf-favorite-properties-editor.png)

## Change Property Values

A marker near each property indicates whether a property value differs from its default value.

![Modified Properties](../../../../images/eurd-wpf-properties-window-modified-values.png)

Right-click a property’s editor to reset the value.

![Reset a Property Value](../../../../images/eurd-wpf-properties-window-value-reset.png)

## Specify Expressions

The Properties window allows you to set expressions that specify property values. Click the `f` button to specify an expression in the invoked Expression Editor.

![The f Buttons](../../../../images/eurd-wpf-properties-window-value-expression.png)

![The Expression Editor](../../../../images/eurd-wpf-expression-editor.png)

## Search for Properties

The integrated search box allows you to find properties. When you type within the search box, the Properties window filters the list and displays properties that match the entered text.

![The Search Box](../../../../images/eurd-wpf-properties-window-property-search.png)

If you type two substrings separated by a space character, these substrings are considered as individual search criteria. The Properties window shows the properties that match either of these substrings. To find properties that contain both substrings, enclose the typed string in quotation marks or type "+" before the second substring (for instance, **foreground +color**).

Type "-" to exclude properties that contain a specific substring (for instance, **border -color**).
