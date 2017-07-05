---
title: Columns
---
The Grid dashboard item supports four types of columns.

![wdd-grid-columns-overview](../../../../images/Img125253.png)
* **Dimension**
	
	A dimension column displays values from the bound data item "as is".  If the dimension column is bound to a data source containing images, it can display images.
* **Measure**
	
	A measure column displays summaries calculated against data in the bound data item.
	
	Values in the measure column can be displayed as text or represented by bars.
	
	![wdd-grid-measure-options](../../../../images/Img125786.png)
	
	To select between these modes, open the column menu and go to the **Options** section.
* **Delta**
	
	A delta column calculates summaries against two measures: the **Actual** value and the **Target** value. When you switch the column type to **Delta**, a new **Target** data item container appears.
	
	![wdd-grid-delta-target-data-section](../../../../images/Img125787.png)
	
	The difference between these values is displayed within the column.
	
	You can configure delta options in the **Delta Options** section of the [column menu](../../../../../dashboard-for-web/articles/web-dashboard-designer-mode/ui-elements/data-item-menu.md).
* **Sparkline**
	
	A sparkline column visualizes the variation of summary values over time.
	
	The sparkline column is bound to the measure providing sparkline values and to the dimension providing a date-time interval. Add the required date-time dimension to the **Sparkline** placeholder to show values depending on time.
	
	![wdd-grid-sparkline-add-date](../../../../images/Img125788.png)
	
	You can configure sparkline options in the data item's **Sparkline Options** section.

When you drop a data item into the Columns section, the type for the new column is determined automatically based on the data type.

To change the column type, open the [column menu](../../../../../dashboard-for-web/articles/web-dashboard-designer-mode/ui-elements/data-item-menu.md) and click the corresponding type button.

![wdd-grid-column-type](../../../../images/Img125212.png)