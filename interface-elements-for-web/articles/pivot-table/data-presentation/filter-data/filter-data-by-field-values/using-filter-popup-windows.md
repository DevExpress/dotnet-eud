---
title: Using Filter Popup Windows
author: Natalia Kazakova
legacyId: 11187
---
# Using Filter Popup Windows
Depending on the settings made by your application vendor, the Pivot Table can display an individual Filter Window for each field, or an integrated Filter Window for a group of fields.

This topic describes how to filter data using both types of Filter Windows.

## Simple Filter Window
A simple Filter Window allows you to hide visible and show previously hidden values of a particular field.

![EU_StandardFilterWindow](../../../../../images/img16237.png)

In the Filter Window, uncheck field values that should be hidden and check values that should be visible. Then, click **OK** to close the window and apply the filtering.

## Hierarchical Filter Window
A hierarchical Filter Window displays values of several fields, arranged in a tree-like manner.

![EU_HierarchicalFilterWindow](../../../../../images/img16234.png)

In the Filter Window, uncheck field values that should be hidden and check values that should be visible.

Use the ![EU_HierarchicalFilterWindow_ExpandButton](../../../../../images/img16236.png) buttons to expand field values and access their child values. To collapse an expanded field value and hide its child values, use the ![EU_HierarchicalFilterWindow_CollapseButton](../../../../../images/img16235.png) button.

Click **OK** to close the window and apply the filtering.

## Filtering Indication
If a field's values are filtered, the corresponding filter button is highlighted.

![ASPxPivotGrid_DataFiltering2](../../../../../images/img8921.png)

## Removing Filtering
To remove filtering against a specific field, invoke its Filter Window and select **(Show All)**.