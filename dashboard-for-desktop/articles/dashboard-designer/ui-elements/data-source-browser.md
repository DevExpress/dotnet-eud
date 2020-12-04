---
title: Data Source Browser
author: Natalia Kazakova
legacyId: 17252
---
# Data Source Browser
The **Data Source Browser** allows you to navigate through dashboard data sources. It displays the data source structure and allows you to [bind dashboard items](../bind-dashboard-items-to-data/bind-dashboard-items-to-data.md) to the required data source fields using drag-and-drop operations. The Data Source Browser also enables you to manage [calculated fields](../work-with-data/creating-calculated-fields.md).

![UIElements_DataSourceBrowser_Browser](../../../images/img20675.png)

The Data Source Browser contains the following elements.
* **Data Source** drop-down list - allows you to select the required data source.
* **Query/Data Member** drop-down list - allows you to select the required query or data member.
* The following **Command buttons** are available.
	
	The ![UIElements_DataSourceBrowser_GroupFieldsButton](../../../images/img20695.png) button groups fields by type.
	
	The ![UIElements_DataSourceBrowser_SortAscendingButton](../../../images/img20696.png) and ![UIElements_DataSourceBrowser_SortDescendingButton](../../../images/img20697.png) buttons are used to switch the sort order.
	
	The ![DataSourceBrowser_RefreshFieldList](../../../images/img118211.png) button is used to refresh the Field List.
* **Field List** displays data source fields. You can drag these fields to the [data item placeholders](data-items-pane.md) to specify data binding.

The Data Source Browser identifies the following data field types.

| Icon | Description |
|---|---|
| ![field-list-icon-boolean](../../../images/img18791.png) | Boolean |
| ![field-list-icon-byte](../../../images/img18792.png) | Byte |
| ![field-list-icon-date-time](../../../images/img18795.png) | Date-time |
| ![field-list-icon-number](../../../images/img18796.png) ![UIElements_DataSourceBrowser_FieldListIconNumericFloat](../../../images/img20881.png) | Numeric |
| ![field-list-icon-string](../../../images/img18798.png) | String |
| ![field-list-icon-calculated-field](../../../images/img18793.png) ![SummaryCalculatedFieldIcon](../../../images/img118212.png) | [Calculated field](../work-with-data/creating-calculated-fields.md) |