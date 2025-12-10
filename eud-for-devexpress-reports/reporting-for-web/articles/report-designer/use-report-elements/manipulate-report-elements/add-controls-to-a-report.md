---
title: Add Controls to a Report
author: Anna Vekhina
---
# Add Controls to a Report

## Add Report Controls
To display a data field's value in your report, drag the corresponding item from the [Field List](../../report-designer-tools/ui-panels/field-list.md) and drop it onto the report's detail band. This creates a new report control bound to the corresponding field.

![](~/eud-for-devexpress-reports/reporting-for-web/images/eurd-web-drop-field-from-field-list.png)

You can also use the [Toolbox](../../report-designer-tools/toolbox.md) to add other controls to your report and display content such as text, images, charts, barcodes, and so on.

![](~/eud-for-devexpress-reports/reporting-for-web/images/eurd-web-report-add-label.png)

The Web Report Designer supports drag & drop operations from outside the browser window (making it easier to add content to your report documents):

- **Image files** - Drag & drop an image file onto the report surface to create a [Picture Box](../../use-report-elements/use-basic-report-controls/picture-box.md).
- **Text files** - Drop a TXT file to create a label, or drop an RTF, DOCX, or HTML file to insert a [Rich Text](../../use-report-elements/use-basic-report-controls/rich-text.md) control with associated file content.
- **PDF files** - Drop a PDF file to insert a [PDF Content](../../use-report-elements/use-basic-report-controls/pdf-content.md) control.
- **Existing controls** - Dropping a file onto an existing report control updates content with new file data.

This document describes how to add the most commonly used controls to a report. See [Use Report Elements](../../use-report-elements.md) for a complete list of available controls.

## Display Text
Use the following controls to display text in a report:

* [Label](../use-basic-report-controls/label.md)
	
	Displays plain text in a report. 

	![](~/eud-for-devexpress-reports/reporting-for-web/images/eurd-web-label.png)
	

* [Rich Text](../use-basic-report-controls/rich-text.md)
	
	Displays rich text in a report. You can apply different font settings to the control's content and load content from an external HTML file.

	![](~/eud-for-devexpress-reports/reporting-for-web/images/eurd-web-rich-text.png)
	

* [Table](../use-tables.md)
	
	Contains any number of cells arranged in one or more rows.
	Each table cell can display plain text or contain other controls.

	![](~/eud-for-devexpress-reports/reporting-for-web/images/eurd-web-table.png)
	
* [Character Comb](../use-basic-report-controls/character-comb.md)
	
	Displays each character in a separate cell and can be used to create printed forms.

	![](~/eud-for-devexpress-reports/reporting-for-web/images/eurd-web-character-comb.png)
	

Double-click any of these controls to invoke an in-place editor where you can enter text.

![](~/eud-for-devexpress-reports/reporting-for-web/images/eurd-web-in-place-editor.png)

Press CTRL+Enter to submit changes and close this mode.

You can use corresponding properties of the **Appearance** category to access the selected control's font and alignment settings.

![](~/eud-for-devexpress-reports/reporting-for-web/images/eurd-web-label-appearance.png)


Labels and other text-oriented controls can display the following content:

* **Static content**
	
	A control's content does not change once it is specified in a published document.

	![](~/eud-for-devexpress-reports/reporting-for-web/images/eurd-web-static-content.png)

* **Dynamic content**
	
	A connected data source supplies this content. In a published document, it changes according to the printed data source record.

	![](~/eud-for-devexpress-reports/reporting-for-web/images/eurd-web-dynamic-content.png)
	
	You can use the [Format String Editor](../../report-designer-tools/format-string-editor.md) to format dynamic content.

	![](~/eud-for-devexpress-reports/reporting-for-web/images/eurd-web-format-string-editor.png)
	

* **Mixed content**
	
	You can combine labels' and other text-oriented controls' static and dynamic content within the same control.	
	
	Use the **Format String** property in the **Action** category to format this field's value.

	![](~/eud-for-devexpress-reports/reporting-for-web/images/eurd-web-format-string-property.png)

## Display Page Information
Use the [Page Info](../use-basic-report-controls/page-info.md) control to display information about document pages, such as the current page number and/or total number of pages.

![](~/eud-for-devexpress-reports/reporting-for-web/images/eurd-web-page-info.png)

You can also use this control to add information about a report's author and the document's creation date.

See the following tutorials for detailed instructions:

* [Add Page Numbers](../../add-navigation/add-page-numbers.md)
* [Display the User Name in a Report](../../add-extra-information/display-the-user-name-in-a-report.md)
* [Display the Current Date and Time in a Report](../../add-extra-information/display-the-current-date-and-time-in-a-report.md)

## Display Check Boxes, Images and Barcodes
Drop a Boolean data field from the Field List onto a report to create a [Check Box](../use-basic-report-controls/check-box.md) control bound to that field.

![](~/eud-for-devexpress-reports/reporting-for-web/images/eurd-web-check-box.png)

Check boxes can display different states depending on the underlying data values.

![](~/eud-for-devexpress-reports/reporting-for-web/images/eurd-web-check-boxe-states.png)

Use the [Picture Box](../use-basic-report-controls/picture-box.md) control to display images in a report. You can load an image from an external file, from a bound data source, or from a web location using the specified URL.

![](~/eud-for-devexpress-reports/reporting-for-web/images/eurd-web-picture-box.png)

To display barcodes, use the [Barcode](../use-bar-codes.md) control.

![](~/eud-for-devexpress-reports/reporting-for-web/images/eurd-web-bar-code.png)

## <a name="drawinglinesshapes"></a>Drawing Lines and Shapes
Use the [Shape](../draw-lines-and-shapes/draw-shapes.md) control to draw simple graphics in a report (circles, crosses or arrows).

![](~/eud-for-devexpress-reports/reporting-for-web/images/eurd-web-display-shapes.png)

The [Line](../draw-lines-and-shapes/draw-lines.md) control enables you to draw straight or slanted lines in a single band.

![](~/eud-for-devexpress-reports/reporting-for-web/images/eurd-web-lines.png)

The [Cross-Band Line and Box](../draw-lines-and-shapes/draw-cross-band-lines-and-boxes.md) controls enable you to draw lines and boxes spanning multiple report bands.
