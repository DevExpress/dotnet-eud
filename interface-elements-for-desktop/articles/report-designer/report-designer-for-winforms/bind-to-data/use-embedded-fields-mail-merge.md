---
title: Use Embedded Fields (Mail Merge)
author: Anna Gubareva
---
# Use Embedded Fields (Mail Merge)

This topic describes how to provide data to report controls using the advanced **Mail Merge** binding method. This feature allows you to create templates in which data source values populate specific fields while other text remains constant (that is, allows you to combine static and dynamic content within the same control).

## <a name="embedfields"></a>Embed Fields in a Control Text
You can apply mail merge to the control's **Text** property only. Double-click the required control on the design surface to invoke the in-place editor. Insert data field names with square brackets to create embedded fields and use any prefixes or postfixes.

![](../../../../images/eurd-win-mail-merge-insert-data-fields.png)

You can embed a [parameter](../shape-report-data/use-report-parameters.md)'s value into a control's content using the **Parameters.ParameterName** syntax.

![](../../../../images/eurd-win-mail-merge-insert-parameters.png)

A database barrel icon is displayed above the control if embedded fields are valid in the current data context (specified by the report's **Data Source** and **Data Member** properties).

For the [Rich Text](../use-report-elements/use-basic-report-controls/rich-text.md) control, you can select any text part and adjust its color and font options using the [Toolbar](../report-designer-tools/toolbar.md)'s **Font** group.

![](../../../../images/eurd-win-mail-merge-format-text.png)

Embedded fields are replaced with values obtained from an assigned data source when previewing or exporting a report:

![](../../../../images/eurd-win-mail-merge-preview-result.png)

Consider the following specifics and limitations when using embedded fields:

* Field names should not use dots and spaces to be interpreted correctly.
* Mail Merge is not available for a table's nested fields in a master-detail hierarchy.
* Embedded fields cannot be exported to [XLS](../../../print-preview/print-preview-for-winforms/exporting/xls-specific-export-options.md) and [XLSX](../../../print-preview/print-preview-for-winforms/exporting/xlsx-specific-export-options.md) as values; they are always exported as plain text. We recommend using [text formats](../shape-report-data/shape-data-expression-bindings/format-data.md) instead if you need to accompany dynamic data with static text.

## <a name="formatfields"></a>Format Embedded Fields
The mail merge feature enables you to apply formats to embedded field values. Select a required data field and click the control's smart tag. Click the **Format String** property's ellipsis button, and in the invoked **Format String Editor**, choose a built-in format pattern.

![](../../../../images/eurd-win-mail-merge-format-string.png)

This adds the selected format to the target data field by separating it from the field name with the **!** symbol and applies this format to field values when previewing a document.

![](../../../../images/eurd-win-mail-merge-format-string-result.png)

## <a name="supportedcontrols"></a>Supported Controls
You can apply the mail merge feature to the **Text** of the following report controls:

* [Bar Code](../use-report-elements/use-bar-codes.md)
* [Character Comb](../use-report-elements/use-basic-report-controls/character-comb.md)
* [Check Box](../use-report-elements/use-basic-report-controls/check-box.md)
* [Label](../use-report-elements/use-basic-report-controls/label.md)
* [Rich Text](../use-report-elements/use-basic-report-controls/rich-text.md)
* [Table Cell](../use-report-elements/use-tables.md)