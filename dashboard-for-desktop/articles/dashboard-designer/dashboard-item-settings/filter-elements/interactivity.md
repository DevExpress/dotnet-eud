---
title: Interactivity
author: Natalia Kazakova
legacyId: 17941
---
# Interactivity
This document describes the filtering capabilities supported by filter elements. You can use filter elements to apply master filtering to other dashboard items or introduce hierarchical filtering by adding several connected filters.

## Master Filtering
The **Dashboard** allows you to use any data aware dashboard item as a filter for other dashboard items (**Master Filter**). To learn more, see the [Master Filtering](../../interactivity/master-filtering.md) topic, which describes filtering concepts common to all dashboard items.

> [!IMPORTANT]
> Note that filter elements do not support Master Filter selection modes. You can switch the selection mode by [changing the type](filter-elements-overview.md) of the required filter element.

Depending on the filter element type, you can select a value(s) to make other dashboard items display only data related to the selected value(s).

![FilterElements_Interactivity](../../../../images/img24829.png)

You can also create a set of related filter elements containing relevant filter values. For instance, in the image below, the **State/Province** filter element contains states related to the 'United States' value, while the **City** filter element contains cities related to the 'New York' value.

![CascadingFiltering](../../../../images/img24833.png)

Disable the **Ignore Master Filters** option for the required filter element to allow applying filtering to this element.

## Filter Element Options
_Standard_ Combo Box and _Radio_ List Box filter elements have the _(Allow Empty Filter)_ option that enables the filter mode without selected items. To enable the mode, click the **Allow Empty Filter** button in the **Design** ribbon tab.

![ShowAllValue_Ribbon](../../../../images/img26111.png)

The **Enable Search** button displays the search box that allows you to search and filter as you type: 

![Enable_Search](../../../../images/img256001.png)