---
title: Dashboard Items Layout
author: Natalia Kazakova
legacyId: 16515
---
# Dashboard Items Layout
The **Dashboard Designer** provides the capability to arrange and resize dashboard items and [groups](../dashboard-item-settings/dashboard-item-group.md) in various ways, using simple drag-and-drop operations.

![Layout_ItemsLayoutMain](../../../images/img20477.png)

* [Layout Concepts](#layout-concepts)
* [Item Resizing](#item-resizing)
* [Maximize and Restore Item](#maximize-and-restore-item)
* [Item Positioning](#item-positioning)

## Layout Concepts
The dashboard arranges dashboard items and [groups](../dashboard-item-settings/dashboard-item-group.md) using _layout items_ and _layout groups_. They are special containers that are used to present a dashboard layout as a hierarchical structure.
* A layout item is used as a container that displays an individual dashboard item.
* A layout group is used as a container that is used to arrange layout items (or other layout groups) either horizontally or vertically. At the same time, layout groups are used as containers that display [dashboard item groups](../dashboard-item-settings/dashboard-item-group.md).

Thus, a dashboard layout is hierarchically arranged from the root layout group to bottommost layout items, which display individual dashboard items.

![DashboardLayoutHierarchy](../../../images/img25963.png)

## Item Resizing
You can resize individual items/groups of items by dragging their edges.

![Layout_ResizingItem](../../../images/img20595.png)

By default, a 2x2 layout group of dashboard items is horizontally oriented and contains two child layout groups. This arranges dashboard items in two 'columns' and allows you to set a different height for items in different columns. You can switch the orientation of the 2x2 group to **Vertical** using the indicator at the group intersection.

![ItemsResizing_Crosshair](../../../images/img24753.png)

This allows you to specify different widths for dashboard items in different 'rows'. The table below lists and describes different modes.

| Indicator | Result | Description |
|---|---|---|
| ![VertIndicator_Layout](../../../images/img24756.png) | ![Crosshair_VerticalResizing](../../../images/img25985.png) | Orients the layout group horizontally and allows you to change the height of individual items and the width of 'columns'. |
| ![HorzIndicator_Layout](../../../images/img24755.png) | ![Crosshair_HorizontalResizing](../../../images/img25984.png) | Orients the layout group vertically and allows you to change the width of individual items and the height of 'rows'. |

## Maximize and Restore Item
You can expand any dashboard item into the whole dashboard size to examine data in greater detail. The expanded dashboard item size in this case is the same as the root layout group.

- To maximize a dashboard item, click the **Maximize** button in the [dashboard item caption](dashboard-item-caption.md).

	![](../../../images/win-dashboard-maximize-dashboard-item.png)

- To restore the item size, click **Restore**.

	![](../../../images/win-dashboard-restore-dashboard-item.png)

## Item Positioning
You can change the position of a dashboard item by using drag-and-drop and one of the following approaches.
* If the [caption](dashboard-item-caption.md) of the dashboard item is visible, click it and hold down the left mouse button while dragging the item.
* If the caption of the dashboard item is not visible, click the ![Layout_DragAndDropIcon](../../../images/img20487.png) icon in the top left corner, and hold down the left mouse button while dragging the item.

Depending on the required dashboard item position, a new layout group is created (if required) to maintain the arrangement of items. Thus, the dashboard item can be inserted to the desired area of a new or existing dashboard layout group.

The following table illustrates how a dashboard item is dragged.

| Action | Description |
|---|---|
| ![DashboardDesigner_DraggingItem_1](../../../images/img117901.png) | Select the required dashboard item. |
| ![DashboardDesigner_DraggingItem_2](../../../images/img117902.png) | Drag the dashboard item to the expected area. The _drag indicator_ ( ![DashboardDesigner_DragIndicator](../../../images/img117906.png) ) will show possible positions for the dashboard item. |
| ![DashboardDesigner_DraggingItem_3](../../../images/img117903.png) | Move the mouse cursor to the required position. The _drop indicator_ ( ![DashboardDesigner_DropIndicator](../../../images/img117907.png) ) highlights the hovered position. |
| ![DashboardDesigner_DraggingItem_4](../../../images/img117904.png) | Then, the _drop indicator_ sequentially displays areas that can be occupied by the dashboard item. Release the left mouse button when the drop indicator displays the required area. |
| ![DashboardDesigner_DraggingItem_5](../../../images/img117905.png) | The dashboard item is moved to a new position. |