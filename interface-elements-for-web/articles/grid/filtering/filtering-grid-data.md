---
title: Filtering Data
author: Svetlana Nikulina
legacyId: 4144
---
# Filtering Data
Grid provides different elements that allows you to filter data.

**Filter Buttons**

Click a filter button to invoke the filter dropdown, which lists unique values in a column.

If the dropdown displays check boxes, check them to select the required values, and click **OK** to apply the filter criteria.

![filter_header.png](../../../images/img17833.png)

If the dropdown does not display check boxes, click the required value to apply the filter criteria.

![ASpxGridView_HeaderFilter](../../../images/img7159.png)

The filter dropdown only displays values that match the applied filter criteria. To remove the filter, click **(All)**.

Note that if a filter is applied to a column, other column header filters display unique values of the sorted rows. To show the full list of values (include values of rows hidden by sorting), hold down SHIFT and click a header filter button.

For columns containing date and time data, the dropdown displays a [date range header filter](date-range-header-filter.md).


**Filter Row**

Type text within the **Filter Row**. A filter condition is automatically created based on the value entered, and this is applied to the corresponding column.

![ASPxGridView_AutoFilterRow](../../../images/img7157.png)

If the **Apply** button is displayed, the filter is applied on button click.

![FilterRow](../../../images/img22709.png)

To remove the column filter, clear the text in the auto-filter row. To remove the grid's entire filter, click **Clear**.

![ASPxGridView_ClearAutoFilterRow](../../../images/img7158.png)



**Search Panel**

The [Search Panel](search-panel.md) enables you to filter data and highlight search results.


**Filter Builder**

The [Filter Builder](creating-complex-filter-criteria-with-the-filter-control.md) enables you to create complex filter criteria.

**Customization Dialog**

The [customization dialog](../customization-dialog/filtering-page.md) enables you to filter grid data by entering filter criteria.