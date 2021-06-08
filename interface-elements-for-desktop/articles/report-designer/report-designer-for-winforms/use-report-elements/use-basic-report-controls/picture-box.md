---
title: Picture Box
author: Anna Gubareva
---
# Picture Box

## <a name="overview"></a>Overview

Use the **Picture Box** control to add images to a report. The images can have one of the following formats: BMP, JPG, JPEG, GIF, TIF, TIFF, PNG, ICO, DIB, RLE, JPE, JFIF, EMF, WMF, SVG.

To add the **Picture Box** control to a report, drag the **Picture Box** item from the [Toolbox](../../report-designer-tools/toolbox.md) onto the report's area.

![](../../../../../images/eurd-win-add-picture-box-to-report.png)


Specify one of the following properties to set an image:

- **Image Source**  
    Save the image to the report definition.
- **Image Url**  
    Only save a path to the image.

![](../../../../../images/eurd-win-picture-box-image-property.png)

## Assign an External Image

Click the **Image Source** / **Image URL** property's ellipsis button to invoke the **Open File** dialog.

![](../../../../../images/eurd-win-ImageSource-OpenFileDialog.png)

The selected image or its URL is saved to the report definition **.repx** file.

## Assign an Image from the Report's Image Collection

Set the report's **Image Resources** property.

![](../../../../../images/eurd-win-ImageResources-Editor.png)

Click the **Picture Box**'s smart tag. In the invoked menu, click the **Expression** option's ellipsis button to open the **Expression Editor**. Choose an image from the **Images** collection:

![ImageSource-OpenFileDialog](../../../../../images/eurd-win-ImageSource-ExpressionEditor-ImagesCollection.png)


## Bind a Picture Box to Data

Use one of the following techniques to add the **Picture Box** control that obtains an image from a data source.

- Click the control's smart tag. In the invoked menu, expand the **Expression** drop-down list for the **Image Source** property and select a data field.

    ![](../../../../../images/eurd-win-picturebox-set-field.png)

    You can bind the **Image Url** property to data in a similar way. In this instance, the URL that specifies the image location is obtained from the data source.  

    Click the **Expression** option's ellipsis button to invoke the **Expression Editor**. Use this editor to construct a [binding expression](../../use-expressions.md) that can include two or more data fields.

- Drag an image data field from the report's [Field List](../../report-designer-tools/ui-panels/field-list.md) and drop it onto a report band.

    ![](../../../../../images/eurd-win-picture-box-drop-from-field-list.png)

- Right-click a data field in the [Field List](../../report-designer-tools/ui-panels/field-list.md) and drop it onto a report band. Select the **Picture Box** item in the invoked context menu.

    ![](../../../../../images/eurd-win-picture-box-drop-right-click.png)


See the [Bind Report Controls to Data](../bind-controls-to-data.md) topic for more information about how to create data-aware controls.

## SVG Support Limitations

The **Picture Box** control does not support the following SVG content:

- Gradient colors
- Text (you can convert text to curves as a workaround)
- Animations
- External .css styles

Export (except for PDF) has the following limitations:

- SVG images are converted to metafiles because document viewers may not support SVG format.
    
- SVG images are exported as PNG in the Microsoft Azure environment.


The **Medium Trust** permission level does not support SVG.

## Image Size Modes

Use the **Sizing** property to specify an image's position in the Picture Box. 

![](../../../../../images/eurd-win-picture-box-sizing-property.png)

This control supports the following image size modes:

* **Normal**
    
    The image is displayed at the top left corner with its original dimensions. The image is clipped if it does not fit the control's boundaries. 

    ![](../../../../../images/eurd-win-picture-box-image-size-mode-normal.png)

* **Stretch Image**

    The image is stretched or shrunk to fill the control's width and height.

    ![](../../../../../images/eurd-win-picture-box-image-size-mode-stretch-image.png)

* **Auto Size**

    The control's dimensions are adjusted to the image's size.

    ![](../../../../../images/eurd-win-picture-box-image-size-mode-auto-size.png)

* **Zoom Image**

    The image is resized proportionally without clipping it to fit the control dimensions.

    ![](../../../../../images/eurd-win-picture-box-image-size-mode-zoom-image.png)

* **Squeeze**

    The image is centered and shown full-size if the control dimensions exceed the image size. Otherwise, the image is resized to fit the control's boundaries.

    ![](../../../../../images/eurd-win-picture-box-image-size-mode-squeeze.png)

* **Tile**

    The original image is replicated within the control starting from the top left corner. The replicated image is clipped if it does not fit the control's boundaries.

    ![](../../../../../images/eurd-win-picture-box-image-size-mode-tile.png)

You can also use the **Image Alignment** property in the **Normal**, **Squeeze** and **Zoom Image** modes to specify the alignment in relation to the control's boundaries.

## Interactivity

You can add a possibility to load/change an image and/or draw a signature in a picture box when it is displayed in Print Preview. To do this, enable the **Edit Options** | **Enabled** property.

![picture-box-enable-content-editing](../../../../../images/eurd-win-picture-box-enable-content-editing.png)

Click the picture box in a previewed document and an editor invokes.

![picture-box-content-editing](../../../../../images/eurd-win-picture-box-content-editing.png)

> [!Tip]
> You can draw borders for the picture box to make the editor visible in Print Preview, if an image is not specified.

Refer to the [Content Editing in Print Preview](../../provide-interactivity/edit-content-in-print-preview.md) topic for details and to the [Interactive E-Forms](../../create-reports/interactive-e-forms.md) tutorial to see how the E-Form demo report uses this picture box mode.
