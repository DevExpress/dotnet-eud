---
title: Add Controls to a Report
author: Anna Gubareva
---
# Add Controls to a Report

This document describes how to add [controls](../../../../../articles/report-designer/report-designer-for-winforms/use-report-elements.md) to a report.

## <a id="addcontrolsfromthetoolbox"></a>Add Controls from the Standard Controls Bar

Use the End-User Designer's [Toolbox](../../../../../articles/report-designer/report-designer-for-winforms/report-designer-tools/ui-panels/toolbox.md) to add controls to your report.

![eurd-add-controls](../../../../../images/eurd-add-controls.png)

## <a id="addfieldsfromthefieldlist"></a>Add Data-Bound Controls from the Field List

You can drag fields from the [Field List](../../../../../articles/report-designer/report-designer-for-winforms/report-designer-tools/ui-panels/field-list.md) onto your report to add data-bound controls, after you [bound](../../../../../articles/report-designer/report-designer-for-winforms/bind-to-data.md) your report to a data source.

### Add a Control

Drag a field from the [Field List](../../../../../articles/report-designer/report-designer-for-winforms/report-designer-tools/ui-panels/field-list.md) and drop it onto the report's surface.

![eurd-add-controls-from-field-list](../../../../../images/eurd-add-controls-from-field-list.png)

To add a control of specific type, do either of the following:

* Hold down the SHIFT key and drop a data field onto a report's surface.
* Right-click a data field and drop it onto a report's surface.

This invokes a context menu where you can select which control to add.

![eurd-add-controls-from-field-list-picturebox](../../../../../images/eurd-add-controls-from-field-list-picturebox.png)

### Add a Table

Hold the CTRL or SHIFT key and click several fields. Drop them onto the report's surface to add a table with its cells bound to these fields.

![eurd-add-controls-add-table](../../../../../images/eurd-add-controls-add-table.png)

Drop an entire data table from the [Field List](../../../../../articles/report-designer/report-designer-for-winforms/report-designer-tools/ui-panels/field-list.md) to add a report table with columns bound to the data table's fields.

![eurd-add-controls-add-entire-table](../../../../../images/eurd-add-controls-add-entire-table.png)

To add column headers, do either of the following:

* Select the fields and hold the CTRL or SHIFT key when you drop them onto a report surface.
* Drag and drop fields with the right mouse button.

![eurd-add-controls-add-column-headers](../../../../../images/eurd-add-controls-add-column-headers.png)

 This adds a new table whose cells display the field names.

## <a id="addcontrolsfromexternalsources"></a>Add Content from External Sources

You can add text and graphics from external applications to your reports:

* Drag a file, text or image from an external application onto your report.

	![eurd-add-controls-drag-rich-text](../../../../../images/eurd-add-controls-drag-rich-text.png)

* Copy a file, text or image from an external application, and paste it into your report.

	![eurd-add-controls-copy-text](../../../../../images/eurd-add-controls-copy-text.png)

The following table shows which file types transform into report controls:

| File Type | Control |
| --- | --- |
| .TXT | A [Label](../../../../../articles/report-designer/report-designer-for-winforms/use-report-elements/use-basic-report-controls/label.md) control that contains file contents. |
| .DOC, .DOCX, .RTF, .HTM, .HTML | A [Rich Text](../../../../../articles/report-designer/report-designer-for-winforms/use-report-elements/use-basic-report-controls/rich-text.md) control that contains file content. |
| .JPG, .PNG, .BMP, .GIF, .TIF, .SVG | A [Picture Box](../../../../../articles/report-designer/report-designer-for-winforms/use-report-elements/use-basic-report-controls/picture-box.md) control that contains the image. |