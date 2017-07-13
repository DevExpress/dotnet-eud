---
title: Enable Content Editing in Print Preview
---
# Enable Content Editing in Print Preview
This document describes how to enable editing the content of specific controls in [Print Preview](../../document-preview.md).

This topic consists of the following sections.
* [Text Editing](#textediting)
* [Check Box Editing](#checkboxediting)

## <a name="textediting"/>Text Editing
The **Label**, **Table Cell** and **Character Comb** [report controls](../../report-elements/report-controls.md) can be assigned editors to customize their content in Print Preview.

To enable content editing for a specific control, do the following.
1. Select a control that you want to become editable in Print Preview and switch to the [Properties Panel](../../interface-elements/properties-panel.md). In the **Behavior** category, expand the **Edit Options** property and set the **Enabled** property to **Yes**.
	
	![eud-web-report-label-edit-options-enabled](../../../../images/img126945.png)
2. To provide a mask for editing integer values, set the **Editor Name** property to **Integer Positive** to assign the required editor with a corresponding mask.
	
	![eud-web-report-label-edit-options-editor-name](../../../../images/img126946.png)

Switch the report to the [Preview](../../document-preview.md) mode. To highlight all editing fields available in the document, click the **Editing Fields** ![eud-web-report-editing-fields-button](../../../../images/img126947.png) button in the Print Preview toolbar. Clicking a field will invoke the appropriate editor.

![eud-web-report-content-editing](../../../../images/img126948.png)

## <a name="checkboxediting"/>Check Box Editing
In addition to editing text, you can enable switching [Check Box](../../report-elements/report-controls.md) states in Print Preview. When two or more check boxes have identical **Group ID** values, the corresponding editors belong to a single logical group (i.e., only one option can be selected within a group at a time).

![eud-web-check-box-edit-options](../../../../images/img126949.png)

> The changes made to a control's content in Print Preview have no effect on other parts of the document (e.g., the related summary results, grouping, sorting, bookmarks and other settings that have already been processed before generating the document).