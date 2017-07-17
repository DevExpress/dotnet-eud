---
title: Data Explorer
author: Eugeniy Burmistrov
legacyId: 17315
---
# Data Explorer
This topic describes how to use the **Data Explorer** in Snap.

This topic consists of the following sections.
* [Overview](#overview)
* [Data Type Reference](#description)

## <a name="overview"/>Overview
The Data Explorer is essential for managing data in Snap applications. It allows you to **add new data sources** to a Snap document, access their structure and run the [Query Builder](../../connect-to-data/use-the-query-builder.md) to customize a data source.

![snap-data-explorer-data-source-context-menu](../../../../images/img21372.png)

Using the Data Explorer, you can also manage a report's parameters, as well as the [calculated fields](../../connect-to-data/use-calculated-fields.md) supplied to the data source tables.

You can create a Snap report layout by dropping the data members from the Data Explorer onto a document's [design surface](design-surface.md). The data members correspond to the columns created on the design surface, and the data member names are displayed in the column headers.

![How-to-Bind-Report-to-MS-SQL-Server-09](../../../../images/img18483.png)

To display data in a chart, drop data fields from the Data Explorer onto the corresponding chart areas.

![ReportWithChart-02](../../../../images/img18288.png)

When a data field is added to your document, its data type determines what **element** is created (e.g., text, **chart**, or **bar code**).

## <a name="description"/>Data Type Reference
In the Data Explorer, different icons are assigned to various data objects. These icons are explained in the following table.

| Regular Data Source | Mail Merge Data Source | Description |
|---|---|---|
| ![snap-data-explorer-icon-dataset](../../../../images/img18794.png) | ![snap-data-explorer-icon-mail-merge-dataset](../../../../images/img21420.png) | Designates an individual data source. When expanded, shows the hierarchy of its tables and/or views. |
| ![field-list-icon-table](../../../../images/img18799.png) | ![snap-data-explorer-icon-mail-merge-data-table](../../../../images/img21421.png) | Designates a data table or view within a data source. When expanded, shows the hierarchy of its data fields. You can drag a data table and drop it onto the document surface, after which the entire table structure will be presented in the report in a tabular form. |
| ![field-list-icon-parameters](../../../../images/img18797.png) | ![field-list-icon-parameters](../../../../images/img18797.png) | Parameters. Lists the report parameters. You can include parameters in a document's filtering expression or calculated fields, or you can use them directly in your reports, (e.g., by dropping them onto the document surface). |

For every table or view, the Data Explorer lists the available data fields. Depending on the data type, it will automatically assign one of the following icons.

| Regular Data Source | Mail Merge Data Source | Data Type | Displayed Contents |
|---|---|---|---|
| ![field-list-icon-boolean](../../../../images/img18791.png) | ![snap-data-explorer-field-icon-mail-merge-boolean](../../../../images/img21425.png) | Boolean | Check Box, plain text |
| ![field-list-icon-byte](../../../../images/img18792.png) | ![snap-data-explorer-field-icon-mail-merge-byte](../../../../images/img21426.png) | Byte | Bar Code, Picture |
| ![field-list-icon-date-time](../../../../images/img18795.png) | ![snap-data-explorer-field-icon-mail-merge-date-time](../../../../images/img21428.png) | Date-time | Plain text |
| ![field-list-icon-number](../../../../images/img18796.png) | ![snap-data-explorer-field-icon-mail-merge-numeric](../../../../images/img21424.png) | Numeric | Plain text, Bar Code |
| ![field-list-icon-string](../../../../images/img18798.png) | ![snap-data-explorer-field-icon-mail-merge-string](../../../../images/img21423.png) | String | Plain text, Bar Code |
| ![field-list-icon-calculated-field](../../../../images/img18793.png) | ![field-list-icon-calculated-field](../../../../images/img18793.png) | **Calculated field** | Determined by the result of the calculation. |