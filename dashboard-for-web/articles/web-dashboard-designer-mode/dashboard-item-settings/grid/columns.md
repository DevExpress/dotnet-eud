---
title: Columns
author: Natalia Kazakova
legacyId: 117531
---
# Columns
The Grid dashboard item supports four types of columns.

![wdd-grid-columns-overview](../../../../images/img125253.png)
* **Dimension**
	
	A dimension column displays values from the bound data item "as is".  If the dimension column is bound to a data source containing images, it can display images.
* **Hyperlink**
	
	A dimension column allows you to display hyperlinks in the Grid dashboard item. You can provide hyperlinks as a separate data column, or they can be automatically created at run-time from any column using the specified **URI pattern**.
	
	![grid_hyperlink_column](../../../../images/grid_hyperlink_column.png)


* **Measure**
	
	A measure column displays summaries calculated against data in the bound data item.
	
	Values in the measure column can be displayed as text or represented by bars.
	
	![wdd-grid-measure-options](../../../../images/img125786.png)
	
	To select between these modes, open the column menu and go to the **Options** section.
* **Delta**
	
	A delta column calculates summaries against two measures: the **Actual** value and the **Target** value. When you switch the column type to **Delta**, a new **Target** data item container appears.
	
	![wdd-grid-delta-target-data-section](../../../../images/img125787.png)
	
	The difference between these values is displayed within the column.
	
	You can configure delta options in the **Delta Options** section of the [column menu](../../ui-elements/data-item-menu.md).
* **Sparkline**
	
	A sparkline column visualizes the variation of summary values over time.
	
	The sparkline column is bound to the measure providing sparkline values and to the dimension providing a date-time interval. Add the required date-time dimension to the **Sparkline** placeholder to show values depending on time.
	
	![wdd-grid-sparkline-add-date](../../../../images/img125788.png)
	
	You can configure sparkline options in the data item's **Sparkline Options** section.

When you drop a data item into the Columns section, the type for the new column is determined automatically based on the data type.

To change the column type, open the [column menu](../../ui-elements/data-item-menu.md) and click the corresponding type button.

![wdd-grid-column-type](../../../../images/img125212.png)