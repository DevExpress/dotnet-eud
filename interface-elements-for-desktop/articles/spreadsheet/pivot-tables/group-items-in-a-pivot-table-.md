---
title: 'Group Items in a Pivot Table '
---
Grouping can help you get a clearer view of data and show only data you want to analyze. The following topic describes how to group [dates](#date), [numbers](#number) or [selected items](#text) in a pivot table.

<a name="date"/>

## Group a Pivot Table by Date
1. Right-click a cell within a row or column field containing dates and select **Group...**
	
	![Spreadsheet_PivotTable_GroupingDates_ContextMenu](../../../images/Img126549.png)
	
	...or on the **PivotTable Tools** | **Analyze** tab, in the **Group** group, click the **Group Field** button.
	
	![Spreadsheet_PivotTable_Grouping_Ribbon](../../../images/Img126551.png)
2. The **Grouping** dialog is invoked. Type the first and last date or time you want to group by, select one or more date or time intervals for grouping and click **OK**.
	
	![SpreadsheetPivotTable_GroupingDates_Dialog](../../../images/Img126553.png)
3. As a result, the date field will be grouped as shown in the image below.
	
	![Spreadsheet_PivotTable_GroupingDates_Result](../../../images/Img126552.png)

<a name="number"/>

## Group a Pivot Table by Numbers
1. Right-click a cell within a row or column field containing numeric values and select **Group...**
	
	![Spreadsheet_PivotTable_GroupingNumbers_ContextMenu](../../../images/Img126554.png)
	
	...or on the **PivotTable Tools** | **Analyze** tab, in the **Group** group, click the **Group Field** button.
	
	![Spreadsheet_PivotTable_Grouping_Ribbon](../../../images/Img126551.png)
2. The **Grouping** dialog is invoked. Type in start value, end value, interval and click **OK**.
	
	![Spreadsheet_PivotTable_GroupingNumbers_Dialog](../../../images/Img126555.png)
3. The result is shown in the image below.
	
	![Spreadsheet_PivotTable_GroupingNumbers_Result](../../../images/Img126556.png)

<a name="text"/>

## Group Selected Items
1. Select the items that you want to group.
2. Right-click the selected range and select the **Group** item from the context menu...
	
	![Spreadsheet_PivotTable_GroupingLabels_ContextMenu](../../../images/Img126540.png)
	
	...or on the **PivotTable Tools** | **Analyze** tab, in the **Group** group, click the **Group Selection** button.
	
	![Spreadsheet_PivotTable_GroupingLabels_Ribbon](../../../images/Img126541.png)
3. As a result, the selected range will be combined into a single group. To rename the group, select the group header, press **F2** and type the required name.
	
	![Spreadsheet_PivotTable_GroupingLabels_Result](../../../images/Img126542.png)
4. You can also enable or disable displaying the subtotal for the created group. To do that, right-click the group header and select the **Subtotal 'Field Name'** item.
	
	![Spreadsheet_PivotTable_GroupingLables_SubtotalContextMenu](../../../images/Img126543.png)
5. The resulting report is shown in the image below.
	
	![Spreadsheet_PivotTable_GroupingLabels_SubtotalResult](../../../images/Img126544.png)

## Ungroup Data
To ungroup data in a pivot table, do one of the following.
* Right-click the grouped field and select **Ungroup...** from the context menu.
	 
	
	![Spreadsheet_PivotTable_Grouping_UngroupContextMenu](../../../images/Img126465.png)
* Select any cell in the grouped field and on the **Pivot Table Tools** | **Analyze** tab, in the **Group** group, click the **Ungroup** button.
	
	![Spreadsheet_PivotTable_Grouping_UngroupRibbon](../../../images/Img126466.png)
	
Note that ungrouping a numeric or date and time field will remove all groups for that field. If you ungroup a group of selected items, only the selected items will be ungrouped.
