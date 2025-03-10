---
title: Table Reports
author: Anna Vekhina
---
# Table Reports

This tutorial describes how to create a data-bound report that displays information in a tabular format. Table reports should not be confused with hierarchical [master-detail reports](master-detail-reports-with-detail-report-bands.md), nor with [cross-tab reports](cross-tab-reports.md).

![](../../../images/eurd-web-table-report-result.png)

1. [Create a new report](../add-new-reports.md) or [open an existing one](../open-reports.md).

2. [Bind the report](../bind-to-data.md) to a required data source.

3. Add the [Page Header](../introduction-to-banded-reports.md) band to the report to print the column headers at the top of every document page. To do this, select the **Insert Page Header** Band command from the report's context menu.

    ![](../../../images/eurd-web-table-report-insert-page-header.png)

4. Switch to the [Field List](../report-designer-tools/ui-panels/field-list.md), select data fields, hold `Shift` when you drag fields and drop them onto the report design area. This creates a data table with data field names.

    ![](../../../images/eurd-web-table-report-add-static-captions.png)

5. To provide dynamic content to the report, select data fields and drop them onto the Detail band in the Field list.

    ![](../../../images/eurd-web-table-report-add-dynamic-content.png)

    This creates a table with the same number of cells as the number of fields selected with each cell bound to the appropriate data field.

6. Click an empty place on the report's surface and draw a rectangle around the table to select it. 

    ![](../../../images/eurd-web-table-report-select-both-tables.png)

    Alternatively, you can select one cell and press `Esc` to move one level up and select an entire row.

7. Expand the **Appearance** category and specify the **Font**, **Text Alignment**, and **Borders** properties to customize table appearance.

    ![](../../../images/eurd-web-table-report-set-up-appearance.png)

8. Define a currency format for the **UnitPrice** cell. Select the cell and click the **Text Format String** property's ellipsis button. Select the appropriate format in the invoked **Format String Editor** editor and click **OK**.

    ![](../../../images/eurd-web-table-report-format-string.png)

9.  To further improve table readability, you can apply different visual styles to odd and even rows. See [Report Visual Styles](../customize-appearance/report-visual-styles.md) to learn more.

    ![](../../../images/eurd-web-table-report-odd-even-styles.png)

    See the [Use Tables](../use-report-elements/use-tables.md) section to learn how to add or remove table rows and cells, and how to convert table cells to separate label controls.


Switch to [Print Preview](../preview-print-and-export-reports.md) to see the generated report.

![](../../../images/eurd-web-table-report-result.png)