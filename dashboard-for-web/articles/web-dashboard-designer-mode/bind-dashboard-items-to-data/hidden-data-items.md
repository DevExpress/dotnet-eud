---
title: Hidden Data Items
author: Natalia Kazakova
legacyId: 117957
---
# Hidden Data Items
The **hidden data items** can be used to perform various data shaping and analysis operations by measures or dimensions that do not directly take part in the visual representation of data.

To create hidden data items, click the _Add Measure_ / _Add dimension_ placeholders in the **Hidden Measures** / **Hidden Dimensions** data section and select an appropriate data field.

You can perform the following operations using hidden data items.
* [Filtering](#filtering)
* [Sorting](#sorting)
* [Top N](#topn)
* [Conditional Formatting](#cf)

## <a name="filtering"/>Filtering
You can use **hidden dimensions** to apply [filtering](../data-shaping/filtering.md) to the dashboard item.

![wdd-hidden-data-item-filtering](../../../images/img124648.png)

For example, the Grid on the image above is filtered by the _OrderDate (Quarter)_ hidden dimension.

## <a name="sorting"/>Sorting
You can [sort](../data-shaping/sorting.md) values of the specified dimension by the **hidden measure**.

![wdd-hidden-data-item-sorting](../../../images/img124647.png)

For instance, a data item menu on the image above displays sorting by values of the hidden _UnitPrice (Sum)_ measure.

## <a name="topn"/>Top N
You can use **hidden measures** in [Top N](../data-shaping/top-n.md) conditions.

![wdd-hidden-data-item-top-n](../../../images/img124649.png)

For example, a data item menu on the image above displays the top 5 categories for the _UnitPrice (Sum)_ hidden measure.

## <a name="cf"/>Conditional Formatting
You can create format rules based on **hidden measures** to apply [conditional formatting](../appearance-customization/conditional-formatting.md) to elements corresponding to visible values.

![wdd-hidden-measure-conditional-formating](../../../images/img125668.png)

For example, the Range Set format rule on the image above is calculated by the _Quantity (Sum)_ hidden measure.