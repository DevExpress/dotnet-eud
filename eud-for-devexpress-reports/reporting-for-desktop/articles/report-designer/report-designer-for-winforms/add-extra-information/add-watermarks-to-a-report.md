---
title: Add Watermarks to a Report
---
# Add Watermarks to a Report

DevExpress Reporting allows you to display text and picture watermarks on report pages. You can also specify an expression that assigns different watermarks to pages.

* How to add watermarks.

* How to specify watermark settings.

* How to use pre-printed forms.

![eurd-win-add-watermarks-result](../../../../images/eurd-win-add-watermarks-result.png)

## <a name="addwatermark"></a>Add a Watermark to a Report

Switch to the [toolbar](../report-designer-tools/toolbar.md)'s **Page** page and press **Watermark**.

![eurd-win-add-watermarks-use-toolbox](../../../../images/eurd-win-add-watermarks-use-toolbox.png)

In the invoked **Watermark** dialog, select either the **Text Watermark** or **Picture Watermark** tab, depending on the type of watermark you wish to add.

## Specify Text Watermark Settings

Specify the following settings:
	
![eurd-win-watermark-editor](../../../../images/eurd-win-watermark-editor.png)
	
* Text

	The watermark’s text.

* Direction

	The incline of the watermark’s text.

* Font

	The font of the watermark’s text.

* Color

	The foreground color of the watermark’s text.

* Size

	The size of the watermark’s text.

* Bold

	Formats the watermark’s text as bold.

* Italic

	Formats the watermark’s text as italic.

* Position

	Specifies whether a watermark should be printed behind or in front of page content.

* Transparency

	The transparency of the watermark’s text.

* Id

	The unique identifier of a watermark used to specify the watermark in the WatermarkId property (See the Manage Watermark Collection section for details).

* Page Range

	The range of pages which contain a watermark.

Click **OK** to add a watermark to the watermark collection. The added watermark is automatically displayed in the report in Preview mode.

> [!NOTE]
> A report can display only one watermark on a report page.

## Specify Picture Watermark Settings

Specify an image. Click the **Load image** option’s **Browse** button.

![eurd-win-watermark-editor-picture](../../../../images/eurd-win-watermark-editor-picture.png)
	
In the invoked **Select Picture** dialog, select the file containing the image that you wish to use as a watermark and click **Open**.
	
![eud-select-picture-dialog](../../../../images/eud-select-picture-dialog.png)

Specify the following picture options:

![eud-specify-picture-watermark-settings](../../../../images/eud-specify-picture-watermark-settings.png)

* Size Mode

	The mode in which a picture watermark is displayed.

* Tiling

	Specifies whether a picture watermark should be tiled.

* Horizontal Alignment

	Specifies the horizontal alignment of the watermark.

* Vertical Alignment

	Specifies the vertical alignment of the watermark.

* Position

	Specifies whether a watermark should be printed behind or in front of page content.

* Transparency

	The transparency of the watermark’s image. The **Transparency** property is unavailable when you specify an SVG image.

* Id

	The unique identifier of a watermark used to specify the watermark in the WatermarkId property (See the Manage Watermark Collection section for details).

* Page Range

	The range of pages which contain a watermark.

> [!NOTE]
> A report can display only one watermark on a report page.	

Click **OK** to add a watermark to the watermark collection. The added watermark is automatically displayed in the report in Preview mode.

### <a name="preprintedform"></a>Supply a Preprinted Form

You can use a picture watermark as a template, to display an image of the preprinted form on the report's body at design time.

To display a watermark at design time, switch to the [toolbar](../report-designer-tools/toolbar.md)'s **View** page and activate  **Watermark**.

![eurd-win-add-preprinted-watermark](../../../../images/eurd-win-add-preprinted-watermark.png)

The following image illustrates a report with a watermark shown at design-time that contains a template of a preprinted form.

![eurd-win-add-a-template-watermark](../../../../images/eurd-win-add-a-template-watermark.png)

Place report controls on the report's body according to the layout of the preprinted form.

![eurd-win-add-a-template-watermark-result](../../../../images/eurd-win-add-a-template-watermark-result.png)

### Supported Image Formats

A picture watermark supports the following formats:

* BMP
* JPG / JPEG / JPE / JFIF
* GIF
* TIF / TIFF
* PNG
* ICO
* DIB
* RLE
* EMF / WMF
* SVG

## Combine Text and a Picture in One Watermark

You can display both text and a picture in one watermark.

For example, create a watermark and specify its text and picture settings.

Set position of the text to In front:

![Position In front](../../../../images/infront-text-position.png)

Set position of the picture to Behind:

![Position Behind](../../../../images/behind-image-position.png)
 
As a result, the image is displayed behind the table, while the text is in front of the content:

![Display text and image watermarks in one page](../../../../images/watermark-text-infront-image-behind.png)

## Display a Specific Watermark in a Report

**Watermark Id** allows you to specify a watermark from the collection to display in the report. This property has a priority over the watermark’s **Page Range** property.

Create two watermarks in the Watermarks collection editor.

![Create two watermarks](../../../../images/add-watermarks-in-the-collection-editor.png)

Set Watermark Id to Watermark2 (the Id option's value)

![Display the second watermark in the collection](../../../../images/propery-grid-watermark-id.png)

The image below shows the result.

![Display specific watermark](../../../../images/display-specific-watermark-example.png)

## Display Watermarks According to the Specified Condition

Bind **Watermark Id** to an expression to apply watermarks stored in the collection to specific report pages.

Create the “First page watermark”, “Even page watermark”, and “Odd page watermark” watermarks with the following settings:

![Create three watermarks](../../../../images/bind-watermarks-to-expression--ui.png)

Specify the expression in the report’s WatermarkId property:

`Iif([Arguments.PageIndex]=0,'Watermark_0',Iif([Arguments.PageIndex]%2=0,'Watermark_1','Watermark_2'))`

![Specify the binding expression](../../../../images/specify-watermark-expression-in-the-expression-editor.png)

The image below shows the result.

![Display different watermarks](../../../../images/watermarks-expression-example.png)