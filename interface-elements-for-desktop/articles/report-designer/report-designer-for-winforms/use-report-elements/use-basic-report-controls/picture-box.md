---
title: Picture Box
author: Anna Gubareva
---
# Picture Box

## <a name="overview"></a>Overview

You can use the **Picture Box** control to embed _static_ (stored with the report definition) or _dynamic_ (obtained from a data source) images into a report. The images can have one of the following formats: BMP, JPG, JPEG, GIF, TIF, TIFF, PNG, ICO, DIB, RLE, JPE, JFIF, EMF, WMF, SVG.

To add the **Picture Box** control to a report, drag the **Picture Box** item from the [Toolbox](../../report-designer-tools/toolbox.md) onto the report's area.

![](../../../../../images/eurd-win-add-picture-box-to-report.png)


Specify one of the following properties to set an image:

- **ImageSource**  
    Use this property to save images along with a report definition.
- **ImageUrl**  
    Use this property to save only the path to the image.

![](../../../../../images/eurd-win-picture-box-image-property.png)

## Bind a Picture Box to Data
You can use the Picture Box to display an image [dynamically obtained](../../bind-to-data/bind-controls-to-data-expression-bindings.md) from a data source. Click the control's smart tag, expand the **Image** property's **Expression** drop-down list and select the data field.

![](../../../../../images/eurd-win-picture-box-bind-to-data.png)

You can bind the **Image URL** property to data in the same way. 

Click the **Expression** option's ellipsis button to invoke the **Expression Editor**. This editor allows you to construct a complex binding expression with two or more data fields.

You can also drag and drop a field that contains image data from the [Field List](../../report-designer-tools/ui-panels/field-list.md) to create a new Picture Box bound to this field.

![](../../../../../images/eurd-win-picture-box-drop-from-field-list.png)

See the [Bind Report Controls to Data](../../bind-to-data/bind-controls-to-data-expression-bindings.md) topic for more information about how to create data-aware controls.

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

Refer to the [Content Editing in Print Preview](../../provide-interactivity/edit-content-in-print-preview.md) topic for details and to the [Create-an-Interactive-E-Form](../../create-popular-reports/create-an-interactive-e-form.md) tutorial to see how the E-Form demo report uses this picture box mode.
