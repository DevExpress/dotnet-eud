---
title: Layout
author: Natalia Kazakova
legacyId: 118038
---
# Layout
This topic describes how to change a layout algorithm used to arrange Treemap tiles. To do this in the Web Dashboard, go to the Treemap's [Options](../../ui-elements/dashboard-item-menu.md) menu  and open the **Layout** section.

![wdd-treemap-layout-options](../../../../images/img125963.png)

## Layout Algorithm
To change a layout algorithm, select the required direction in the Layout Algorithm list. The following algorithms are available.
* The **Slice and Dice** algorithm divides the space between items, slicing it in the specified direction depending on item value.
	
	![wdd-treemap-slice-and-dice](../../../../images/img125964.png)
* The **Squarified** algorithm arranges tiles so that their width/height ratio will be closer to 1.
	
	![wdd-treemap-squarified](../../../../images/img125965.png)
* The **Striped** algorithm is a modified version of the Squarified algorithm. The difference here is that tiles are drawn side by side as columns or rows.
	
	![wdd-treemap-stripped](../../../../images/img125966.png)

## Layout Direction
You can also set a layout direction to specify an arrangement of tiles depending on their sizes. The Treemap arranges tiles in descending order from maximum to minimum values. To do this, select the required direction in the **Layout Direction** list.
* **Bottom Left - Top Right** arranges tiles from the bottom-left to the top-right corner.
* **Bottom Right - Top Left** arranges tiles from the bottom-right to the top-left corner.
* **Top Left - Bottom Right** arranges tiles from the top-left to the bottom-right corner.
* **Top Right - Bottom Left** arranges tiles from the top-right to the bottom-left corner.