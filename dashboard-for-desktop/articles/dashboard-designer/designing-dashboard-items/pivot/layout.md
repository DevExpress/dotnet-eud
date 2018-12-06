---
title: Layout
author: Natalia Kazakova
legacyId: 16604
---
# Layout
This topic describes how to control the Pivot dashboard item layout, the visibility of totals and grand totals, etc.
* [Layout Type](#layouttype)
* [Totals Visibility](#totalsvisibility)
* [Totals Position](#totalsposition)
* [Values Visibility](#valuesvisibility)
* [Values Position](#valuesposition)
* [Reset Layout Options](#resetlayout)

## <a name="layouttype"/>Layout Type
If the Pivot dashboard item contains a hierarchy of dimensions in the [Rows](providing-data.md) section, you can specify the layout used to arrange values corresponding to individual groups.

| Layout type | Example | Description |
|---|---|---|
| **Compact** | ![Pivot_CompactLayout](../../../../images/img127490.png) | Displays values from different Row dimensions in a single column. Note that in this case totals are shown at the top of a group, and you cannot change [totals position](#totalsposition). |
| **Tabular** | ![Pivot_TabularLayout](../../../../images/img127491.png) | Displays values from different Row dimensions in separate columns. |

Use the **Layout** button in the **Design** ribbon tab to change the Pivot layout.

![Pivot_LayoutButtonRibbon](../../../../images/img128425.png)

## <a name="totalsvisibility"/>Totals Visibility
You can control the visibility of totals and grand totals for the entire Pivot dashboard item. For instance, the image below displays the Pivot dashboard item with the disabled row totals.

![Pivot_DisableRowTotals_Example](../../../../images/img127500.png)

To manage the visibility of totals and grand totals, use the **Totals** and **Grand Totals** buttons in the **Design** ribbon tab, respectively.

![Pivot_TotalsVisibilityRibbon](../../../../images/img128426.png)

These buttons invoke a popup menu that allows you to manage the visibility of column and row totals/grand totals separately.

Moreover, you can control the visibility of totals for individual dimensions/measures by using the data item's context menu (**Show Totals** and **Show Grand Totals** options).

![Pivot_ShowTotals_DataItemMenu](../../../../images/img127503.png)

## <a name="totalsposition"/>Totals Position
If necessary, you can change the Pivot dashboard item’s totals/grand totals position. For instance, in the image below the row totals are moved from the bottom to the top.

![Pivot_RowTotals_Bottom_Top](../../../../images/img127504.png)

To manage totals position, use the **Row Totals Position** and **Column Totals Position** buttons in the **Design** ribbon tab.

![Pivot_TotalsPositionRibbon](../../../../images/img128427.png)

## <a name="valuesvisibility"/>Values Visibility
The Pivot dashboard item can contain several measures in the [Values](providing-data.md) section to hide summary values corresponding to specific measures. For instance, the image below shows the Pivot with hidden _Quantity_ values.

![Pivot_ValuesVisibility](../../../../images/img127507.png)

To do this, use the **Show Values** command in the measure menu.

![Pivot_ValuesVisibility_Menu](../../../../images/img127508.png)

## <a name="valuesposition"/>Values Position
The Pivot dashboard item allows you to control the position of headers used to arrange summary values corresponding to different measures. For instance, you can display values in columns or rows.

![Pivot_ValuesPosition](../../../../images/img127505.png)

To manage this position, use the **Values Position** button in the **Design** ribbon tab.

![Pivot_ValuesPositionRibbon](../../../../images/img128428.png)

## <a name="resetlayout"/>Reset Layout Options
To reset layout options, click the **Reset Layout Options** button in the **Design** ribbon tab.

![Pivot_ResetLayoutOptionsRibbon](../../../../images/img128429.png)