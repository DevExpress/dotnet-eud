---
title: Create a Balance Sheet
author: Anna Gubareva
---
# Balance Sheets

This tutorial describes how to use the Cross Tab control to create a **Balance Sheet** report.

![](../../../../images/eurd-win-balance-sheet-report.png)

> [!Tip]
> This tutorial shows how to configure a Cross Tab using the [Report Wizard](../report-designer-tools/report-wizard.md). See the [Cross-Tab Reports](cross-tab-reports.md) tutorial for information on how to use the Cross-Tab Report Wizard.

## Add a Cross Tab and Bind It to Data

1. Invoke the Report Wizard and [add a blank report](../add-new-reports.md) to your application.

1. Drop the Cross Tab control from the Toolbox onto the report's [Detail band](../introduction-to-banded-reports.md).

    ![](../../../../images/eurd-win-balance-sheet-drop-cross-tab-from-toolbox.png)

3. Click the Cross Tab's smart tag, expand the **Data Source** property's drop-down menu and click **Add New Data Source**.

    ![](../../../../images/eurd-win-balance-sheet-cross-tab-add-data-source.png)

4. Use the invoked [Data Source Wizard](../report-designer-tools/data-source-wizard.md) to bind the Cross Tab to a data source.

Click **Finish** to complete the Data Source Wizard and assign the created data source to the Cross Tab.

![](../../../../images/eurd-win-balance-sheet-cross-tab-data-source.png)

The data source structure becomes available in the [Field List](../report-designer-tools/ui-panels/field-list.md).

![](../../../../images/eurd-win-balance-sheet-field-list.png)

> [!Note]
> Ensure that the report's **Data Source** property is not set if you place a Cross Tab into the [Detail band](../introduction-to-banded-reports.md). Otherwise, the Cross Tab data is printed as many times as there are rows in the report data source.

## Define the Cross Tab Layout

1. Drop data fields from the Field List onto the Cross Tab's areas to define the Cross Tab's rows, columns, and data.

    A row is added to the bottom of the Cross Tab to display grand total values calculated against the added row or column header.

    ![](../../../../images/eurd-win-balance-sheet-drop-type.gif)

    Drop nested row headers next to the parent header cells to create a hierarchy.

    ![](../../../../images/eurd-win-balance-sheet-drop-subtype.gif)

Switch to Print Preview to see the Cross Tab populated with data.

![](../../../../images/eurd-win-balance-sheet-layout-preview.png)

## Specify Group Settings

As you can see in the image above, the Cross Tab displays data for individual days.

Select the column header cell and click its smart tag. Set the **Group Interval** property to group data.

![](../../../../images/eurd-win-balance-sheet-date-group-interval.png)

![](../../../../images/eurd-win-balance-sheet-date-group-interval-preview.png)

## Specify Layout Options

1. The Cross Tab control stacks row headers horizontally. You can change the view so that parent values span the entire row header panel width.

    Select the Cross Tab and switch to the [Property Grid](../report-designer-tools/ui-panels/property-grid-tabbed-view.md). Expand the **Layout Options** group and enable the **Hierarchical Row Layout** property.

    ![](../../../../images/eurd-win-balance-sheet-hierarchical-row-layout.png)

2. Set the **Corner Header Display Mode** property to **None** to merge cells in the top-left corner into a single empty cell.

    ![](../../../../images/eurd-win-balance-sheet-corner-header-display-mode.png)

Switch to Print Preview to see the result.

![](../../../../images/eurd-win-balance-sheet-layout-options-preview.png)

## Hide Grand Totals

1. Select the bottom right cell and click its smart tag. Disable the **Row Visible** and **Column Visible** properties to hide the row and column that display grand total values. Invisible cells are filled with a hatch brush.

    ![](../../../../images/eurd-win-balance-sheet-row-column-visible.png)

2. Resize the Cross Tab. You can also resize individual rows and columns.

    ![](../../../../images/eurd-win-balance-sheet-adjust-control-size.png)

The Cross Tab control no longer displays grand total values.

![](../../../../images/eurd-win-balance-sheet-hidden-grand-totals-preview.png)

## Sort and Format Data

1. Select the row sub-header cell and change its sort order. The Cross Tab sorts row and column field values in ascending order. Set the **Sort Order** property to **None** to restore the original data source order.

    ![](../../../../images/eurd-win-balance-sheet-sort-order.png)

2. Format the data. Hold down SHIFT or CTRL and select cells. Specify the cells' **Text Format String** property.

    ![](../../../../images/eurd-win-balance-sheet-text-format-string.png)

![](../../../../images/eurd-win-balance-sheet-sort-format-options-preview.png)

## Customize Appearance

1. Select the Cross Tab, switch to the **Properties** window and expand the **Styles** property. Use the **General Style** property to specify common appearance settings that apply to all Cross Tab cells. Set the following properties:

    * **Background Color** to **White**
    * **Border Color** to **SlateGray**
    * **Font** to **Tahoma 8.25**
    * **Foreground Color** to **SlateGray**

    ![](../../../../images/eurd-win-balance-sheet-general-style.png)

2. Expand the **Header Area Style** property and do the following:

    * reset the **Background Color** property value to inherit the color from the general style;
    * set the **Foreground Color** property to **MidnightBlue** to override the general foreground color;
    * set the **Font** property to **Tahoma 8.25** to override the general font.

    ![](../../../../images/eurd-win-balance-sheet-header-area-style.png)

3. Expand the **Total Area Style** property and set the following properties to override general settings:

    * **Font** to **Tahoma 8.25 Bold**
    * **Foreground Color**  to **MidnightBlue**

    ![](../../../../images/eurd-win-balance-sheet-total-area-style.png)

4. Select the row sub-header cell and set the following appearance properties:

    * **Foreground Color**  to **SlateGray**
    * **Font** to **Tahoma 8.25**

    These values apply to the selected cell only and override values specified for the entire header area.

    ![](../../../../images/eurd-win-balance-sheet-cell-appearance-settings.png)

![](../../../../images/eurd-win-balance-sheet-styles-preview.png)

5. Select the cells in the top row and in the rows with total values. Set the **Borders** property to **Bottom** and **Border Width** property to **2**.

    ![](../../../../images/eurd-win-balance-sheet-add-borders.png)

6. Select the cells you did not customize in the previous step and set the **Borders** property to **None**.

    ![](../../../../images/eurd-win-balance-sheet-remove-borders.png)

7. Select the cells in the top row and set the **Background Color** property to **LightSteelBlue**.

    ![](../../../../images/eurd-win-balance-sheet-back-color-for-top-row.png)

8. Select the row sub-header cell and the next cell in the data area. Set their **Background Color** property to **AliceBlue**.

    ![](../../../../images/eurd-win-balance-sheet-back-color-for-rows.png)

![](../../../../images/eurd-win-balance-sheet-appearance-preview.png)

## Apply Odd and Even Row Styles

Use the **GroupRowIndex** variable in [expressions](../use-expressions.md) to identify odd and even rows.

Select the row sub-header cell and the next cell in the data area. Go to the **Properties** window and open the **Expressions** tab. Click the **Background Color** property's marker, select **Background Color Expression** and specify the following expression:

_iif([Arguments.GroupRowIndex] % 2 == 1, Rgb(235, 241, 252), ?)_

![](../../../../images/eurd-win-balance-sheet-odd-even-expression.png)

![](../../../../images/eurd-win-balance-sheet-odd-even-preview.png)

As you can see, the row backgrounds do not start from the page's left border, but have indents. These indents correspond to auxiliary cells in a tree.

Select these auxiliary cells and disable the **Column Visible** property.

![](../../../../images/eurd-win-balance-sheet-hide-tree-view-cells.png)

To add indents to row field values and imitate a tree-like view, set the **Padding** property for the Cross Tab's cells.

![](../../../../images/eurd-win-balance-sheet-tree-paddings.png)

![](../../../../images/eurd-win-balance-sheet-final-appearance-preview.png)

## Add a Report Title

1. Right-click the report and select **Insert Band / ReportHeader** from the context menu.

    ![](../../../../images/eurd-win-balance-sheet-add-report-header.png)

2. Drop a [Label](../use-report-elements/use-basic-report-controls/label.md) from the Toolbox onto the created Report Header.

    ![](../../../../images/eurd-win-balance-sheet-drop-label-onto-report-header.png)

3. Double-click the label and type the report title. Specify appearance settings.

    ![](../../../../images/eurd-win-balance-sheet-title.png)

Switch to Print Preview to see the final result.

![](../../../../images/eurd-win-balance-sheet-report.png)