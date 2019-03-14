---
title: Using Filter Windows
author: Natalia Kazakova
legacyId: 11139
---
# Using Filter Windows
Depending on the settings made by your application vendor, the Pivot Table can display an individual Filter Window for each field, or an integrated Filter Window for a group of fields.

This topic describes how to filter data using both types of Filter Windows.

## Excel-style Filter Window
The Excel-style filter popup's content depends on the type of data the related field displays. 

In the **"Values"** tab, end-users can select specific field values from the Pivot Grid. 

![pivot-filter-excel-style-values](../../../../../images/pivot-filter-excel-style-values.png)

The **"Filters"** tab supplies users with additional options related to the field type. For example, when filtering a string field, you can show only those records that begin with 'C': 

![pivot-filter-excel-style-textfilters](../../../../../images/pivot-filter-excel-style-textfilters.png)

Filters applied using the Excel-style filter popup are displayed in the Filter Panel and can be changed in the Filter Editor dialog, which allows end-users to apply complex filter conditions.

> The Excel-style filter cannot be used to apply filtering in OLAP mode. 



## Simple Filter Window
A simple Filter Window allows you to hide visible and show previously hidden values of a particular field.

![EU_XtraPivotGrid_FilterDropdownStandard](../../../../../images/img16180.png)

In the Filter Window, uncheck field values that should be hidden and check values that should be visible. Then, click **OK** to close the window and apply the filtering.

Note that you can customize Filter Window settings using the toolbar displayed at the top of the window. To learn how to do this, see [Filtering Options](filtering-options.md).

## Hierarchical Filter Window
A hierarchical Filter Window displays values of several fields, arranged in a tree-like manner.

![EU_XtraPivotGrid_FilterDropdownHierarchical](../../../../../images/img16181.png)

In the Filter Window, uncheck field values that should be hidden and check values that should be visible.

Use the ![EU_XtraPivotGrid_ExpandButton](../../../../../images/img16184.png) buttons to expand field values and access their child values. To collapse an expanded field value and hide its child values, use the ![EU_XtraPivotGrid_CollapseButton](../../../../../images/img16183.png) button.

You can also expand and collapse all values on a particular level. To do this, right-click any field value and select **Collapse All** or **Expand All** from the context menu.

For instance, to expand all quarters and display months, right-click any quarter value and select **Expand All** from the context menu as shown on the image below.

![EU_XtraPivotGrid_HierarchicalFilterContextMenu](../../../../../images/img16229.png)

Click **OK** to close the window and apply the filtering.

Note that you can customize Filter Window settings using the toolbar displayed at the top of the window. To learn how to do this, see [Filtering Options](filtering-options.md).

## Filtering Indication
You can determine whether a field is filtered by looking at its header. Filter buttons for these fields are visible even when you are not hovering over their headers.

![EU_XtraPivotGrid_Filter_FilteredField](../../../../../images/img7616.png)

## Removing Filtering
To remove filtering against a specific field, invoke its Filter Window and select **(Show All)**.