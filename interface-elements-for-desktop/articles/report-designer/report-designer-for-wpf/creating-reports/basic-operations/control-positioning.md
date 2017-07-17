---
title: Control Positioning
author: Anna Gubareva
legacyId: 116398
---
# Control Positioning
This document describes how to easily construct professionally looking reports by precisely aligning their [elements](../../report-elements/report-controls.md) to each other. These are useful when creating new reports from scratch or when fixing cluttered report layouts with dozens of randomly scattered controls.

To select an appropriate alignment mode for report elements, use a report's **Snapping Mode**.

![EUD_WpfReportDesigner_Positioning_1](../../../../../images/img123807.png)

## Snap Grid
When a report is being edited in the Report Designer, it is lined up by the snap grid. This helps to establish the distance between report elements and align them to each other.

![EUD_WpfReportDesigner_Positioning_2](../../../../../images/img123808.png)

In the **Snap to Grid** mode, a report control that is being relocated using the mouse or the ARROW keys is automatically aligned with the nearest grid cell. When resizing the report control, its size is discretely changed by one grid cell. You can temporarily ignore snapping to the grid when moving and resizing controls. For this, hold down the CTRL key when using the mouse and the ALT key when using the keyboard.

You can select whether the snap grid should be drawn over a report surface by setting the **Draw the Grid** option in the [Properties Panel](../../interface-elements/properties-panel.md).

![EUD_WpfReportDesigner_Positioning_3](../../../../../images/img123809.png)

You also can adjust the **Snap Grid Size**, which is measured in the [measurement units](change-measurement-units-of-a-report.md) set for your report.

## Snap Lines
If the **Snap Lines** mode is selected, report elements are aligned using snap lines. These are special guide lines, which appear around the report control that is being moved or resized and indicate this control's bounds and the distance to other report elements (controls and bands).

![EUD_WpfReportDesigner_Positioning_4](../../../../../images/img123810.png)

To disable snapping using snap lines for controls being relocated or resized, additionally hold down the ALT key.

## Snap Lines and Snap Grid
The **Snap to Grid and Snap Lines** mode enables snapping to both the snap grid and snap lines.

## No Snapping
To disable snapping in your report, set the **Snapping Mode** property to **None**. In this case, report controls are moved and resized by one measurement unit defined by the **Report Unit** property.