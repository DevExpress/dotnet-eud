---
title: Enable Content Editing in Print Preview
author: Anna Gubareva
legacyId: 117924
---
# Enable Content Editing in Print Preview
This document describes how to enable editing the content of specific controls in [Print Preview](../../report-designer-reference/report-designer-ui/preview-tab.md).

This topic consists of the following sections.
* [Text Editing](#textediting)
* [Check Box Editing](#checkboxediting)

## <a name="textediting"/>Text Editing
The [Label](../../report-designer-reference/report-controls/label.md), [Table Cell](../../report-designer-reference/report-controls/table-cell.md) or [Character Comb](../../report-designer-reference/report-controls/character-comb.md) controls can be assigned editors to customize their content in Print Preview.

To demonstrate this feature, use the report similar to one created in the following tutorial: [Change or Apply Data Grouping to a Report](../../report-editing-basics/change-or-apply-data-grouping-to-a-report.md).

To enable content editing, do the following.
1. Select one or more controls that you want to become editable in Print Preview (to select multiple controls, click them while holding down CTRL or SHIFT).
	
	Switch to the [Property Grid](../../report-designer-reference/report-designer-ui/property-grid.md), expand the **Edit Options** property and set the **Enabled** property to **Yes**.
	
	![eud-win-report-labels-edit-options-enabled](../../../../../images/img126925.png)
2. To provide a mask for editing decimal values of the **UnitPrice** field, set the **Editor Name** property to **Fixed-Point Positive** to assign the required editor with a corresponding mask.
	
	![eud-win-report-label-edit-options-editor-name](../../../../../images/img126926.png)

Switch to the [Preview Tab](../../report-designer-reference/report-designer-ui/preview-tab.md). To highlight all editing fields available in the document, click the **Editing Fields** ![eud-win-reports-preview-editing-fields-button](../../../../../images/img126929.png) button in the Print Preview toolbar.

Clicking a field will invoke the appropriate editor. To apply the entered values and navigate between editing fields, use the TAB and SHIFT+TAB keys.

![eud-win-report-content-editing](../../../../../images/img126928.png)

## <a name="checkboxediting"/>Check Box Editing
In addition to editing text, you can enable switching [Check Box](../../report-designer-reference/report-controls/check-box.md) states in Print Preview. When two or more check boxes have identical **Group ID** values, the corresponding editors belong to a single logical group (i.e., only one option can be selected within a group at a time).

![eud-win-report-check-box-edit-options](../../../../../images/img126927.png)

> [!NOTE]
> The changes made to a control's content in Print Preview have no effect on other parts of the document (e.g., the related summary results, grouping, sorting, bookmarks and other settings that have already been processed before generating the document).