---
title: Filter Data at the Data Source Level
author: Anna Vekhina
---
# Filter Data at the Data Source Level

This tutorial illustrates how to filter data at the report data source level, as opposed to the [report level](filter-data-at-the-report-level.md). This approach is recommended when dealing with comparatively large data sources when the retrieval process is slow.

1. [Create a new report](../../add-new-reports.md) or open an existing one.

2. Bind you report to a required data source. See the [Bind to Data](../../bind-to-data.md) section to learn more about providing data to reports.

3. Switch to the [Field List](../../report-designer-tools/ui-panels/field-list.md) and drop the required fields onto the report's [Detail](../../introduction-to-banded-reports.md) band.

    ![](../../../../images/eurd-web-filter-data-drop-fields.png)

4. Select the data source and click **Edit query**.

    ![](../../../../images/eurd-web-filter-data-edit-query.png)

    Click **Run Query Builder** in the invoked [Data Source Wizard](../../report-designer-tools/data-source-wizard.md). 

    ![](../../../../images/eurd-web-filter-data-source-wizard.png)

5. Expand the **Query Properties** section in the invoked [Query Builder](../../report-designer-tools/query-builder.md). Click the ellipsis button for the **Filter** property to construct a filtering expression in the invoked [Filter Editor](../../report-designer-tools/filter-editor.md).

    ![](../../../../images/eurd-web-filter-data-source-filter-string.png)

    Every filter condition consists of three parts:
    * A data field name.
    * Criteria operator, such as **Equals**, **Is less than**, **Is between**, etc.
    * A static operand value, another data field or a query parameter. See the [Specify Query Parameters](../../bind-to-data/specify-query-parameters.md) topic to learn about embedding these parameters into filter conditions.

    You can arrange specific conditions into groups with **And**, **Or**, **Not And**, and **Not Or** operators.

Switch to [Print Preview](../../preview-print-and-export-reports.md) to see the result.

![](../../../../images/eurd-web-filter-data-source-result.png)
