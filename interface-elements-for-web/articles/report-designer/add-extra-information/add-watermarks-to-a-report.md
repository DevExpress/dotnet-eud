---
title: Add Watermarks to a Report
author: Anna Vekhina
---
# Add Watermarks to a Report

This tutorial describes how to add watermarks to a report and use preprinted forms.

![eurd-win-add-watermarks-result](../../../../images/eurd-win-add-watermarks-result.png)

## <a name="addwatermark"></a>Add a Watermark to a Report
To add a watermark to a report, do the following.

1. Switch to the [Properties](..\report-designer-tools\ui-panels\properties-panel.md) panel and expand the **Watermark** node in the **Appearance** category.
	
	![](../../../images/eurd-web-add-watermarks-properties-panel.png)

2. In the **Watermark** node, specify either the **Text** or **Image** property, depending on the type of watermark you wish to add.
	
	For a text watermark, specify the text, direction and font options.
	
	![](../../../images/eurd-web-watermark-text.png)
	
	For a picture watermark, you need to specify an image. To do this, click the ellipsis button for the **Image** property.
	
	![](../../../images/eurd-web-watermark-image.png)
	
	In the invoked dialog, select the file containing the image that you wish to use as a watermark and click **Open**. Next, specify the size mode and alignment options for the picture.
	
	Additionally, for both textual and picture watermarks, you can adjust the transparency, position (in front of or behind the document content), and the page range in which the watermark will be printed.

## <a name="preprintedform"></a>Supply a Preprinted Form
You can use a picture watermark as a template, to display an image of the preprinted form on the report's body at design time.

To display a watermark at design time, expand the **Design** category and enable the **Draw the Watermark** property.

![](../../../images/eurd-web-add-preprinted-watermark.png)

The following image illustrates a report with a watermark shown at design-time that contains a template of a preprinted form.

![](../../../images/eurd-web-add-a-template-watermark.png)

Place report controls on the report's body according to the layout of the preprinted form.

![](../../../images/eurd-web-add-a-template-watermark-result.png)