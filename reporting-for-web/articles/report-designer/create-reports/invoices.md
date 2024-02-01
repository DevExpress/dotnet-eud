---
title: Invoices
author: Anna Vekhina
---
# Invoices

This tutorial describes how to create a simple invoice report displaying information about customers and their orders. You can perform similar steps to create various invoice layouts depending on your requirements.

![](../../../images/eurd-web-invoice-report-result.png)

## Create a Report and Bind It to Data

1. [Create a new report](../add-new-reports.md) or [open an existing one](../open-reports.md).

2. Invoke the designer [menu](../report-designer-tools/menu.md) and click **Add Data Source...**.

   ![](../../../images/eurd-web-data-source-menu.png) 

3. Select **Database** on the first page of the invoked Data Source Wizard and click **Next**.

	![](../../../images/eurd-web-data-source-wizard-select-db.png)

4. Select a data connection on the next page.

    ![](../../../images/eurd-web-invoice-select-data-connection-in-wizard.png)

5. On the same page, you can choose which tables, views and/or stored procedures to add to the report.
	
	Obtain data from two different tables to display information about customers and orders at the same hierarchical level in the report. Click the plus button for the **Queries** category to create a custom query. In the invoked [Query Builder](../report-designer-tools/query-builder.md), add the required data tables to a query and join them based on a key column.
	
	![](../../../images/eurd-web-invoice-join-tables-in-query-builder.png)

6. On the same wizard page, select the data view providing order details for listing products included in each order in the invoice. 

    ![](../../../images/eurd-web-invoice-add-view.png)

7. On the same page, specify a master-detail relationship between the queries. Select the required key fields (columns) to connect tables.
	
	![](../../../images/eurd-web-invoice-master-detail-relationships.png)

8. Click **Finish** to complete the wizard.

After these steps, make sure that an appropriate data member is assigned to the report.

![](../../../images/eurd-web-invoice-report-data-member.png)

## Prepare the Master Report Layout
Create the master report layout to display basic information about customers and their orders.

1. Switch to the [Field List](../report-designer-tools/ui-panels/field-list.md) and drop the required data fields onto the [Detail band](../introduction-to-banded-reports.md). New controls of appropriate types are automatically created and bound to the corresponding fields.
	
	![](../../../images/eurd-web-invoice-master-layout-dynamic-fields.png)

2. Drop [Label](../use-report-elements/use-basic-report-controls/label.md) controls from the [Toolbox](../report-designer-tools/toolbox.md) onto the band to display static captions for specific data fields.
	
	![](../../../images/eurd-web-invoice-master-layout-static-labels.png)

3. Double-click the added labels one after another and enter the required text.
	
	![](../../../images/eurd-web-invoice-master-layout-specify-static-text.png)

4. Use the [Line](../use-report-elements/draw-lines-and-shapes/draw-lines.md) control to separate data.
	
	![](../../../images/eurd-web-invoice-master-layout-add-line.png)

## Prepare the Detail Report Layout
Perform the following steps to create a detail report and construct its layout to show the order details in a tabular form:

1. From the the report's context menu, select the **Insert Detail Report Band** command to create a [Detail Report Band](../introduction-to-banded-reports.md).
	

2. Select the Detail Report band and select the master-detail relationship's name in the **Data Member** property's drop-down list.

    ![](../../../images/eurd-web-invoice-bind-detail-report.png)

3. Add dynamic content to the detail report. Go to the **Field List**, select the data fields while holding down CTRL or SHIFT and drag-and-drop them onto the Detail band. This automatically creates a [Table](../use-report-elements/use-tables.md) control with table cells bound to the corresponding fields.
	
	You should drag-and-drop fields from the category corresponding to the master-detail relationship to correctly generate the detail report's data.
	
	![](../../../images/eurd-web-invoice-detail-layout-add-dynamic-table.png)

4. Add the Group Header band to the detail report to display captions for table columns. Select the Detail Report band and click **Insert Group Header Band** in the context menu.
	
	![](../../../images/eurd-web-underlay-report-addgroupheader.png)

5. To create column headers, drop the [Table](../use-report-elements/use-tables/table-overview.md) control from the **Toolbox** onto the Group Header band and enter the required text in the table's cells.
	
	![](../../../images/eurd-web-invoice-detail-layout-add-table-headers.png)

6. Select the Detail Report band, expand the **Behavior** category and set the band's **Page Break** property to **After the Band** to print each order on a separate page.
	
	![](../../../images/eurd-web-invoice-detail-report-page-break.png)

## Create a Calculated Field
This section demonstrates how to create a [custom field](../shape-report-data/use-calculated-fields.md) whose values are calculated using a pre-defined expression.

Do the following to evaluate an extended price based on the price, quantity and discount values obtained from a database:

1. In the [Field List](../report-designer-tools/ui-panels/field-list.md), select the detail table and click **Add calculated field**.
	
	![](../../../images/eurd-web-invoice-add-calculated-field.png)

2. Click the **Edit** button for the calculated field and change its name to **ExtendedPrice**. Click the **Expression** property's ellipsis button, and in the invoked [Expression Editor](../report-designer-tools/expression-editor.md), construct the expression based on the **UnitPrice**, **Quantity** and **Discount** fields.
	
	![](../../../images/eurd-web-invoice-calculated-field-expression.png)

3. You can use the created calculated field as an ordinary data field. Add a cell to a table in the Detail band and drop the calculated field onto this cell. Additionally, create one more table cell in the Group Header for displaying the corresponding caption.
	
	![](../../../images/eurd-web-invoice-drop-calculated-field-onto-report.png)


## Format Data
The next step is to specify report elements' [value formatting](../shape-report-data/format-data.md) to improve displaying their incoming data.

1. In the master report's Detail band, select controls bound to date fields while holding down CTRL. Switch to the [Properties](../report-designer-tools/ui-panels/properties-panel.md) panel, expand the **Data** category and click the **Text Format String** property's ellipsis button. In the invoked **Format String Editor**, activate the **DateTime** category and select the format, for example, display dates as a month (name) followed by the day (number) and year (four digits).
	
	![](../../../images/eurd-web-invoice-format-date-fields.png)

2. Select the table cell bound to the **Discount** data field in the detail report's Detail band. Expand the **Cell Tasks** category, click the **Text Format String** property's ellipsis button, and in the invoked **Format String Editor**, apply the **Percent** format. In this case, field values are multiplied by 100 and displayed with a percent symbol.
	
	![](../../../images/eurd-web-invoice-format-discount-field.png)

3. In the detail report's Detail band, select the cells bound to the **UnitPrice** and **ExtendedPrice** fields. Invoke the **Format String Editor** once again and choose the format preset from the **Currency** category (for instance, **c2**).

## Calculate a Summary
Do the following to calculate a total price for each order as a sum of **Extended Price** values:

1. Add the Group Footer band to the detail report in the same way as the Group Header.

2. Drop the Label control onto the added band and expand the **Label Tasks** category in the Properties panel. Select the **Summary** section and set the **Running** property to **Report** to calculate the summary for the entire detail report and click the **Expression** property's ellipsis button. In the invoked [Expression Editor](../report-designer-tools/expression-editor.md), specify the following expression to calculate the total price:
	
	![](../../../images/eurd-web-invoice-specify-summary-function.png)

3. Use the **Text Format String** property to format the summary's value (for instance, set it to **Total: {0:c2}**).
	
	![](../../../images/eurd-web-invoice-summary-format-string.png)

## Sort Data
Perform the following steps to sort data in the detail report:

1. Select the **Detail** band in the detail report. Select the **Sort Fields** section in the **Detail Tasks** category and add a new sort field to sort the detail report's data by the required data field.
	
	![](../../../images/eurd-web-invoice-sort-data.png)

2. Click the ![](../../../images/eurd-web-order-ascending.png) or ![](../../../images/eurd-web-order-descending.png) buttons to define the sort order within the group (ascending or descending). Use the ![](../../../images/eurd-web-disable-sorting.png) button to disable sorting in grouped data.


## Customize the Report Appearance
Do the following to customize the report and its elements' appearance:

1. Click the gray area around the design surface to select the report, and in the [Properties](../report-designer-tools/ui-panels/properties-panel.md) panel, specify the font settings. These settings are distributed to all report elements.
	
	![](../../../images/eurd-web-invoice-report-appearance-properties.png)

2. You can adjust a control's font independently from its parent (for instance, make summary values bold).
	
	![](../../../images/eurd-web-invoice-report-control-appearance-properties.png)

3. Change specific controls' (bound to date fields, price fields, etc.) text alignment using the **Text Alignment** property.
	
	![](../../../images/eurd-web-invoice-report-control-text-alignment.png)

4. Create a global [visual style](../customize-appearance/report-visual-styles.md) to apply it afterwards to multiple controls. Switch to the [Report Explorer](../report-designer-tools/ui-panels/report-explorer.md) panel, select the **Styles** node and click the plus button ![](../../../images/eurd-web-styles-create.png) to add a new report visual style.

    ![](../../../images/eurd-web-invoice-add-style.png)

5. Select the created style and click the **Properties** ![](../../../images/eurd-web-styles-edit.png) button in the Report Explorer. This opens the Properties panel where you can adjust the settings of the selected style.

    ![](../../../images/eurd-web-invoice-report-style-settings.png)

6. Select report elements, expand the **Styles** category and choose a style in the **Style** property's drop-down list to apply the style to the selected elements.

    ![](../../../images/eurd-web-invoice-apply-report-style.png)

7. You can provide different appearances to alternating (odd and even) table rows in the detail report. Select the table and expand the **Styles** property in the Property Grid. Invoke the drop-down list for the **EvenStyle** property and select **New**.
	
	![](../../../images/eurd-web-invoice-create-even-style.png)
	
	Specify the created style's appearance settings (for example, background color).

## Add Additional Information
Do the following to provide additional information to your invoices, such as the report name and current date:

1. Add the Page Header band to the master report to display the required information on each invoice page.

2. Drop the Label control from the **Toolbox** onto the Page Header, double-click the control and type "**Invoice**". Specify the required appearance settings (font, foreground color, etc.).
	
	![](../../../images/eurd-web-invoice-page-header-report-name.png)

3. Add the [Page Info](../use-report-elements/use-basic-report-controls/page-info.md) control to the Page Header band to display system date in the report.
	
	![](../../../images/eurd-web-invoice-add-page-info.png)

4. Expand the **Page Info Tasks** category and set the **Page Information** property to **Current Date and Time**. Click the **Text Format String** property's ellipsis button, and in the invoked **Format String Editor**, select a date format as in the **Format Data** section above.
	
    ![](../../../images/eurd-web-invoice-page-info-text-format-string.png)

## View the Result
The invoice report is now ready. Switch to [Print Preview](../preview-print-and-export-reports.md) to see the result.

![](../../../images/eurd-web-invoice-report-result.png)