---
title: Binding Report Elements to Data
author: Eugeniy Burmistrov
legacyId: 5568
---
# Binding Report Elements to Data

> [!WARNING]
> This topic describes the approach you can use when  *expression bindings* are **not enabled** in the Report Designer. If the **Expressions** (![Expressions](../../../../images/icon-expressions.svg)) icon is available in the [Property Grid] (../report-designer-reference/report-designer-ui/property-grid.md), then *expression bindings* are enabled, and you should refer to the [Binding Report Elements Using Expression Bindings](binding-report-elements-using-binding-expressions.md) topic instead.


Report [controls](../report-designer-reference/report-controls.md) can display both [static](add-or-modify-static-information-in-your-report.md) information and data fetched from a [bound database](../create-reports/binding-a-report-to-data.md).

In the [Design Panel](../report-designer-reference/report-designer-ui/design-panel.md) and in the [Report Explorer](../report-designer-reference/report-designer-ui/report-explorer.md), each data-bound control has a yellow database icon (![Database](../../../../images/icon-database.png)).

![RD_CreateReports_BindControl_4](../../../../images/img8337.png)

You can use the following approaches to include information from a data source to your report:

* [Using the Field List](#using-the-field-list)
* [Using the Smart Tag](#using-the-smart-tag)
* [Using the Property Grid](#using-the-property-grid)

After a control is bound to data, you can apply additional customizations  listed in the [Special Capabilities](#special-capabilities) section.

## Using the Field List
* To bind an existing report control to a data field, click the required field item in the [Field List](../report-designer-reference/report-designer-ui/field-list.md), and then drag and drop it onto the control. The yellow database icon inside it will indicate that it has been successfully bound.

    ![RD_Elements_FieldList_1](../../../../images/img8266.png)

* To add a new data-bound control, simply drag the required data field from the Field List onto a report band. This will create a [Label](../report-designer-reference/report-controls/label.md) bound to this data field.

    ![RD_Elements_FieldList_0](../../../../images/img8265.png)

* A more flexible way to create data-bound elements is to right-click a Field List item, and then drag and drop it onto a report. This invokes the [Context Menu](../report-designer-reference/report-designer-ui/context-menu.md), where you can choose a control to visualize data. The selected control will be automatically created and bound to a selected data field.
	
	![RD_Elements_FieldList_2](../../../../images/img8267.png)

## Using the Smart Tag
Click a control's [Smart Tag](../report-designer-reference/report-designer-ui/smart-tag.md), and in the invoked actions list, expand the **Data Binding** drop-down list, and select the required data field.

![RD_CreateReports_BindControl_1](../../../../images/img8334.png)

## Using the Property Grid
Focus a control. In the [Property Grid](../report-designer-reference/report-designer-ui/property-grid.md), expand the **(Data Bindings)** category that contains binding options. Specify a data field for the required attribute (e.g. **Text**).

![RD_CreateReports_BindControl_2](../../../../images/img8335.png)

## Special Capabilities
* After a control is bound, you can [apply formatting](change-value-formatting-of-report-elements.md) to its dynamic content (e.g., treat it as a currency, or as a date and time).
* It is possible to make a control display the result of a summary function calculated across the data field to which it is bound. For details, refer to the [Add Totals to a Report](add-totals-to-a-report.md) topic.
* You can combine both static and dynamic content within the same control (e.g., append a text prefix or postfix), or bind a control to multiple data fields. For details, refer to the [Use Mail Merge in Report Elements](use-mail-merge-in-report-elements.md).
* You can [create a calculated field](add-calculated-fields-to-a-report.md) and bind the control to it.
* A calculated field may use both [parameters](add-parameters-to-a-report.md) requested each time a report is displayed.
