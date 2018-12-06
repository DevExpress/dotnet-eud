---
title: Picture Box
author: Anna Gubareva
---
# Picture Box

## <a name="overview"></a>Overview
The **Picture Box** control allows you to embed _static_ (stored with the report) or _dynamic_ (obtained from a data source) images into a report.

To add this control to a report, drag the **Picture Box** item from the [Toolbox](../../report-designer-tools/toolbox.md) onto the report's area.

![](../../../../../images/eurd-win-add-picture-box-to-report.png)

The Picture Box can display images with the following formats: BMP, JPG, JPEG, GIF, TIF, TIFF, PNG, ICO, DIB, RLE, JPE, JFIF, EMF, WMF.


Use the **Image** or **Image URL** property to specify the image the Picture Box displays. You can access these properties in the control's smart tag.

![](../../../../../images/eurd-win-picture-box-image-property.png)

The specified image is [saved](../../save-reports.md) with the report if you use the **Image** property. If you use the **Image URL** property, only the path to the image is stored. 

## Bind to Data
You can use the Picture Box to display an image [dynamically obtained](../../bind-to-data/bind-controls-to-data-expression-bindings.md) from a data source. Click the control's smart tag, expand the **Image** property's **Expression** drop-down list and select the data field.

![](../../../../../images/eurd-win-picture-box-bind-to-data.png)

You can bind the **Image URL** property to data in the same way. 

Click the **Expression** option's ellipsis button to invoke the **Expression Editor**. This editor allows you to construct a complex binding expression with two or more data fields.

You can also drag and drop a field that contains image data from the [Field List](../../report-designer-tools/ui-panels/field-list.md) to create a new Picture Box bound to this field.

![](../../../../../images/eurd-win-picture-box-drop-from-field-list.png)

See the [Bind Report Controls to Data](../../bind-to-data/bind-controls-to-data-expression-bindings.md) topic for more information about how to create data-aware controls.


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
