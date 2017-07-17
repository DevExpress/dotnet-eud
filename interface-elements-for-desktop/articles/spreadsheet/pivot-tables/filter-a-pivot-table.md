---
title: Filter a Pivot Table
author: Polina Fedorova
legacyId: 117806
---
# Filter a Pivot Table
The **Spreadsheet** provides numerous ways to apply filtering to the PivotTable fields to display only data that meets specific criteria. Select the task you wish to perform.
* [Use a Report Filter](#page)
* [Filter Row or Column Items](#item)
* [Use a Label Filter](#labels)
* [Use a Date Filter](#date)
* [Use a Value Filter](#values)
* [Use Multiple Filters per Field](#multiple)
* [Remove a Filter](#remove)

<a name="page"/>

## Use a Report Filter
A report filter allows you to filter the entire PivotTable report to show data for specific items. To use a report filter, follow the steps below.
1. Click the arrow ![Spreadsheet_FilterAndSortArrow](../../../images/img25500.png) in the report filter field.
	
	![Spreadsheet_PivotTable_Filter_PageFilter_Arrow](../../../images/img126632.png)
2. In the invoked dialog, click the **Uncheck All** button to deselect the values. Then, select the check box for the item you wish to display. To select multiple items, select the **Select Multiple Items** check box at the pane bottom. Click **OK** to apply changes.
	
	![Spreadsheet_PivotTable_Filtering_PageFilter_Dialog](../../../images/img126633.png)
3. The resulting report is shown in the image below. The **Filter** button ![Spreadsheet_AppliedFilterIcon](../../../images/img25636.png) appears in the report filter field to indicate that the filter is applied. 
	
	![Spreadsheet_PivotTable_Filtering_PageFilter_Resultq](../../../images/img126634.png)

<a name="item"/>

## Filter Row or Column Items
1. Click the arrow ![Spreadsheet_FilterAndSortArrow](../../../images/img25500.png) in the **Row Labels** or **Column Labels** cell. If there are multiple fields in the area, select the row or column field you wish to filter.
2. In the drop-down menu, select **Item Filter...**
	
	![Spreadsheet_PivotTable_Filter_ItemFilter_ContextMenu](../../../images/img126635.png)
3. In the invoked dialog, click the **Uncheck All** button to deselect the values. Then, select the item(s) you wish to display and click **OK**. 
	
	![Spreadsheet_PivotTable_Filter_ItemFilter_Dialog](../../../images/img126636.png)
4. The resulting report is shown in the image below. The **Filter** button ![Spreadsheet_AppliedFilterIcon](../../../images/img25636.png) appears in the row or column label to indicate that the filter is applied. 
	
	![Spreadsheet_PivotTable_Filter_ItemFilter_Result](../../../images/img126637.png)

<a name="labels"/>

## Use a Label Filter
1. Click the arrow ![Spreadsheet_FilterAndSortArrow](../../../images/img25500.png) in the **Row Labels** or **Column Labels** cell. If there are multiple fields in the area, select the row or column field you wish to filter.
2. Point to the **Label Filters** item and select one of the built-in comparison operators. 
	
	![Spreadsheet_PivotTable_Filtering](../../../images/img126446.png)
3. In the invoked dialog, specify the filter criteria and click **OK**. 
	
	![Spreadsheet_PivotTable_LabelFilteringDialog](../../../images/img126447.png)
4. The resulting report is shown in the image below. The **Filter** button ![Spreadsheet_AppliedFilterIcon](../../../images/img25636.png) appears in the row or column label to indicate that the filter is applied.
	
	![Spreadsheet_PivotTable_Filtering_Labels_Result](../../../images/img126469.png)

<a name="date"/>

## Use a Date Filter
1. Click the arrow ![Spreadsheet_FilterAndSortArrow](../../../images/img25500.png) in the header of the row or column field containing dates.
2. Point to the **Date Filters** item and select one of the built-in dynamic filter types to display dates that fall within a specified time period (next, this or last week, month, year, etc.) or select the **Before**, **After**, **Equals** or **Between** item to find dates that are before, after or equal to the specified date, or between two dates. 
	
	![Spreadsheet_PivotTable_Filter_Dates_ContextMenu](../../../images/img126638.png)
3. In the invoked **Date Filter** dialog, specify the date(s) to filter by and click **OK**.
	
	![Spreadsheet_PivotTable_Filter_Dates_Dialog](../../../images/img126639.png)
4. The resulting report is shown in the image below. The **Filter** button ![Spreadsheet_AppliedFilterIcon](../../../images/img25636.png) appears in the row or column label to indicate that the filter is applied.
	
	![Spreadsheet_PivotTable_Filter_Dates_Result](../../../images/img126640.png)

<a name="values"/>

## Use a Value Filter
A value filter allows you to filter items in a row or column field based on summary values. To use a value filter, follow the steps below.
1. Click the arrow ![Spreadsheet_FilterAndSortArrow](../../../images/img25500.png) in the **Row Labels** or **Column Labels** cell. If there are multiple fields in the area, select the row or column field to which a filter should be applied.
2. Point to the **Value Filters** item and select one of the built-in comparison operators. 
	
	![Spreadsheet_PivotTable_Filtering_Values_ContextMenu](../../../images/img126467.png)
3. In the invoked dialog, specify the filter criteria and click **OK**. Note that the filtering will be applied to the filtered field's **Grand Total** values. 
	
	![Spreadsheet_PivotTable_Filtering_Values_Dialog](../../../images/img126468.png)
4. The resulting report is shown in the image below. The **Filter** button ![Spreadsheet_AppliedFilterIcon](../../../images/img25636.png) appears in the row or column label to indicate that the filter is applied. 
	
	![Spreadsheet_PivotTable_Filtering_Values_Result](../../../images/img126470.png)

<a name="multiple"/>

## Use Multiple Filters per Field
To enable the capability to apply multiple filters to a single row or column field, do the following.
* On the **PivotTable Tools** | **Analyze** tab, in the **PivotTable** group, click the **PivotTable Options** button.
	
	![Spreadsheet_PivotTable_Filtering_PivotTableOptions](../../../images/img126775.png)
* In the invoked **PivotTable Options** dialog, switch to the **Totals &#38; Filters** tab and check the **Allow multiple filters per field** box.
	
	![Spreadsheet_PivotTable_Filtering_MultipleFilters](../../../images/img126774.png)

<a name="remove"/>

## Remove a Filter
To remove a filter, do the following.
* To remove a filter from a specific field, click the **Filter** button ![Spreadsheet_AppliedFilterIcon](../../../images/img25636.png) and select the **Clear Filter From 'Field Name'**  item in the drop-down menu. 
	
	![Spreadsheet_PivotTable_Filtering_Remove](../../../images/img126448.png)
* To clear all filters applied to the PivotTable fields at once, on the **PivotTable Tools** | **Analyze** tab, in the **Actions** group, click **Clear PivotTable** | **Clear Filters**. 
	
	![Spreadsheet_PivotTable_Filtering_RemoveAllFilters](../../../images/img126772.png)