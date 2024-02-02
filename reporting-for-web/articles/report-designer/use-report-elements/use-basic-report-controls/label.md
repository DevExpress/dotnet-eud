---
title: Label
author: Anna Vekhina
---
# Label

## Label Overview
The **Label** control displays plain text in a report. Drag the **Label** item from the [Toolbox](../../report-designer-tools/toolbox.md) onto the report's area to add a Label control to it.

![](../../../../images/eurd-web-drop-report-control-from-toolbox.png)

Double-click the label to invoke its in-place editor and enter the desired static text.

![](../../../../images/eurd-web-label-static-text.png)

Press CTRL+Enter to submit text changes and exit the label's in-place editing mode.

## Bind to Data
### Display Field Values

You can [bind](../bind-controls-to-data.md) the label's **Text** property to a data field obtained from a report's data source. Switch to the [Properties](../../report-designer-tools/ui-panels/properties-panel.md) panel, expand the **Label Tasks** category and click the **Text** property's marker. Select **Text Expression** from the popup menu. Then select a data field or construct a binding [expression](../../use-expressions/expression-language.md) in the invoked [Expression Editor](../../report-designer-tools/expression-editor.md).

![](../../../../images/eurd-web-label-bind-to-data-field.png)

You can use the Expression Editor to construct a complex binding expression that involves two or more data fields.

![](../../../../images/eurd-web-label-expression-binding.png)

You can also drag and drop a numeric or text field from the [Field List](../../report-designer-tools/ui-panels/field-list.md) to create a new label bound to this field.

![](../../../../images/eurd-web-label-drag-field-from-field-list.png)

See the [Bind Controls to Data](../bind-controls-to-data.md) topic for more information.

The **Process Duplicates Mode**, **Process Duplicates Target** and **Process Null Values** options enable you to hide a control when a duplicated or null value appears in an assigned data source.

![](../../../../images/eurd-web-label-process-duplicates-mode.png)

You can also use the **Text Format String** property to specify output values' [format](../../shape-report-data/format-data.md).

![](../../../../images/eurd-web-label-format-string.png)

The ellipsis button invokes the **FormatString** editor:

![](../../../../images/eurd-web-label-formatstring-editor.png)
### Display Summaries

Specify a data range in the **Running** property and select the summary function in the [Expression Editor](../../report-designer-tools/expression-editor.md) to display a [summary function's result](../../shape-report-data/calculate-summaries/calculate-a-summary.md) in a label.

![](../../../../images/eurd-web-label-summary-function.png)

The ellipsis button invokes the Expression Editor:

![](../../../../images/eurd-web-label-summary-function-editor.png)

## Adjust the Label Size and Content
### Static Content

You can change a label's size to fit its static text using the **Fit Bounds To Text** command from the label's context menu:

* If the **Word Wrap** option is enabled, the command displays control content in multiple lines. It reduces control height and adjusts its width to fit its content.
	
	![](../../../../images/eurd-web-label-fit-bounds-to-text-word-wrap-enabled.png)

* If the **Word Wrap** option is disabled and the control's content is partially visible, the command adjusts the control's size to display this content.
	
	![](../../../../images/eurd-web-label-fit-bounds-to-text-word-wrap-disabled.png)

This command's result also depends on the control's **Text Alignment** and **Right To Left** settings.

Use the **Fit Text To Bounds** button to adjust the control's font size to fit its area. The **Word Wrap** option defines whether the text can occupy multiple lines or should be in a single line.

![](../../../../images/eurd-web-label-fit-text-to-bounds.png)

These commands are not available in the following cases:

* A label's text is an empty string;
* A label's text is bound to data;
* A label's **Angle** property is specified.


### Data-Bound Labels

The **Can Grow** and **Can Shrink** properties allow you to increase or decrease the control's height according to its content in Print Preview mode.

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

See the [Lay out Dynamic Report Content](../../lay-out-dynamic-report-content.md) topic for more information.


## Interactivity
Set the **Enabled** option in the **Edit Options** category section to **Yes** to [edit a label's content](../../provide-interactivity/edit-content-in-print-preview.md) in Print Preview mode.

![](../../../../images/eurd-web-label-edit-options-enabled.png)

Clicking this label in a previewed document invokes the appropriate editor.

![](../../../../images/eurd-web-label-content-editing-in-print-preview.png)

Use the label's **Interactive Sorting** option to click this label in Print Preview to sort report data. Set the **Target Band** property to the Group Header or Detail band, and specify the data field in the **Field Name** property.

![](../../../../images/eurd-web-label-interactive-sorting-options.png)

Refer to [Sort a Report in Print Preview](../../provide-interactivity/sort-a-report-in-print-preview.md) for a step-by-step tutorial.


## Markup Text ##
Enable the **Allow Markup Text** property to format the label's text with markup tags.

![](../../../../images/eurd-web-label-markup-text-allow-markup-text-buttom-tag-examples.png)

**Label** supports the following tags:

| Tag | End Tag | Description |
| --- | ------- | ----------- |
| **&lt;br&gt;** |   | Inserts a single line break. Enable the **WordWrap** property to use this tag. |
| **&lt;nbsp&gt;** | - | Inserts a space. |
| **&lt;color**=_value_**&gt;** | **&lt;/color&gt;** | Specifies the text color. |
| **&lt;backcolor**=_value_**&gt;** | **&lt;/backcolor&gt;** | Specifies the background color. |
| **&lt;size**=_value_**&gt;** | **&lt;/size&gt;** | Specifies the font size. |
| **&lt;b&gt;** | **&lt;/b&gt;** | Defines bold text. |
| **&lt;i&gt;** | **&lt;/i&gt;** | Defines italic text. |
| **&lt;s&gt;** | **&lt;/s&gt;** | Defines strikethrough text. |
| **&lt;u&gt;** | **&lt;/u&gt;** | Defines underlined text. |
| **&lt;image=**_value_**&gt;**  | - | Inserts an image from the report's named image collection. Supports both raster images and SVG images. Use the report's **Image Resources** property to provide images and reference them by their **Id**. The **image** tag's **size** attribute sets the image display pixel size. If the specified width/height exceeds the label's width/height, it is reduced to display the entire image. Specify the **size** attribute after the tag's value followed by the ";" character. |
| **&lt;href=**_value_**&gt;** | **&lt;/href&gt;** | Displays a hyperlink. The value string specifies the hyperlink source, and the string between the opening and closing tags is the text to display. |

When a report is exported to XLS or XLSX, the following rich-text content is converted from labels into Excel-native rich-text content:

| | |
| --- | --- |
| Text format | \<b>, \<i>, \<u>, \<s> |
| Line break | \<br> |
| Non-breaking space | \<nbsp> |
| Font | \<font=**[font name]**> |
| Font size | \<size=**[font size]**> |
| Foreground color | \<color=**[color]**> |
