---
title: Label
author: Anna Vekhina
---
# Label

## Label Overview
The **Label** control displays plain text in a report. You can add this control by dragging the **Label** item from the [Toolbox](../../report-designer-tools/toolbox.md) onto the report's area.

![](../../../../images/eurd-web-drop-report-control-from-toolbox.png)

You can double-click the label to invoke its in-place editor and enter the desired static text.

![](../../../../images/eurd-web-label-static-text.png)

Press CTRL+Enter to submit text changes and exit the label's in-place editing mode.

## Bind to Data
### Display Field Values

You can [bind](../../bind-to-data/bind-controls-to-data-expression-bindings.md) the label's **Text** property to a data field obtained from a report's data source. Switch to the [Properties](../../report-designer-tools/ui-panels/properties-panel.md) panel, expand the **Actions** category and click the **Expression** property's ellipsis button. Select the required data field in the invoked **Expression Editor**.

![](../../../../images/eurd-web-label-bind-to-data-field.png)

You can use the **Expression Editor** to construct a complex binding expression involving two or more data fields.

![](../../../../images/eurd-web-label-expression-binding.png)

You can also drag and drop a numeric or text field from the [Field List](../../report-designer-tools/ui-panels/field-list.md) to create a new label bound to this field.

![](../../../../images/eurd-web-label-drag-field-from-field-list.png)

See the [Bind Controls to Data](../../bind-to-data/bind-controls-to-data-expression-bindings.md) topic to learn more about creating data-aware controls.

The **Process Duplicates Mode**, **Process Duplicates Target** and **Process Null Values** options enable you to hide a control when a duplicated or null value appears in an assigned data source.

![](../../../../images/eurd-web-label-process-duplicates-mode.png)

You can also specify output values' [format](../../shape-report-data/shape-data-expression-bindings/format-data.md) using the **Text Format String** property.

![](../../../../images/eurd-web-label-format-string.png)

### Display Summaries

You can make the label display a [summary function's result](../../shape-report-data/shape-data-expression-bindings/calculate-a-summary.md) by setting the **Running** property to the required range and selecting the summary function in the **Expression Editor**.

![](../../../../images/eurd-web-label-summary-function.png)


## Adjust the Label Size and Content
### Static Content

You can change a label's size to fit its static text using the **Fit Bounds To Text** command in the **Actions** category:

* If the **Word Wrap** option is enabled, the command displays control content in multiple lines. It decreases the control's height and adjusts the width to fit this content.
	
	![](../../../../images/eurd-web-label-fit-bounds-to-text-word-wrap-enabled.png)

* If the **Word Wrap** option is disabled and the control's content is partially visible, the command adjusts the control's size to display this content.
	
	![](../../../../images/eurd-web-label-fit-bounds-to-text-word-wrap-disabled.png)

This command's result also depends on the control's **Text Alignment** and **Right To Left** settings.

Use the **Fit Text To Bounds** command to adjust the control's font size to fit its area. The **Word Wrap** option defines whether the resulting text can occupy multiple lines or should be in a single line.

![](../../../../images/eurd-web-label-fit-text-to-bounds.png)

These commands are not available in the following cases:

* A label's text is an empty string;
* A label's text is bound to data;
* A label's **Angle** property is specified.


### Data-Bound Labels

The **Can Grow** and **Can Shrink** properties allow you to increase or decrease the control's height according to its content in Print Preview.

| Can Grow is enabled | Can Grow is disabled |
|---|---|
| ![](../../../../images/eurd-web-label-can-grow-true.png) | ![](../../../../images/eurd-web-label-can-grow-false.png) |


| Can Shrink is enabled | CanShrink is disabled |
|---|---|
| ![](../../../../images/eurd-web-label-can-shrink-true.png) | ![](../../../../images/eurd-web-label-can-shrink-false.png) |

The **Auto Width** property specifies whether to adjust a data-bound label's width to its content automatically.

You can also use the opposite **Text Fit Mode** property to adjust a control's font size to fit its boundaries in Print Preview. This property is not available if the **Can Grow**, **Can Shrink** or **Auto Width** option is enabled.

![](../../../../images/eurd-web-label-text-fit-mode-property.png)

| Text Fit Mode = None | Text Fit Mode = Grow Only | Text Fit Mode = Shrink Only | Text Fit Mode = Shrink And Grow |
|---|---|---|---|
| ![](../../../../images/eurd-web-label-text-fit-mode-none.png) | ![](../../../../images/eurd-web-label-text-fit-mode-grow-only.png) | ![](../../../../images/eurd-web-label-text-fit-mode-shrink-only.png) | ![](../../../../images/eurd-web-label-text-fit-mode-shrink-and-grow.png) |

See the [Lay out Dynamic Report Content](../../lay-out-dynamic-report-content.md) topic for more information on these options.


## Interactivity
You can enable [editing a label's content](../../provide-interactivity/edit-content-in-print-preview.md) in Print Preview by setting the **Enabled** option in the **Edit Options** section to **Yes**.

![](../../../../images/eurd-web-label-edit-options-enabled.png)

Clicking this label in a previewed document invokes the appropriate editor.

![](../../../../images/eurd-web-label-content-editing-in-print-preview.png)

Use the label's **Interactive Sorting** option to enable sorting report data by clicking this label in Print Preview. Set the **Target Band** property to the required Group Header or Detail band, and the **Field Name** property to the corresponding data field.

![](../../../../images/eurd-web-label-interactive-sorting-options.png)

Refer to [Sort a Report in Print Preview](../../provide-interactivity/sort-a-report-in-print-preview.md) for a step-by-step tutorial.
