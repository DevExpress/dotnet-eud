---
title: Image Settings
author: Natalia Kazakova
legacyId: 116557
---
# Image Settings
You can customize the representation of Image and Bound Image dashboard items in different ways.

## Image Alignment
To specify how the image is aligned within the dashboard item, use the **Alignment** group in the **Design** ribbon tab.

![Image_Alignment_Ribbon](../../../../images/img20213.png)

## Image Size Mode
You can specify the image size mode that defines how the image fits within the dashboard item.

To do this, use the **Size Mode** group in the Ribbon's **Design** tab.

![Image_SizeMode_Ribbon](../../../../images/img20223.png)

The following table illustrates each size mode in two cases: when the image is smaller than the dashboard item, and vice versa.

| Size Mode | Image Smaller than Dashboard Item | Image Larger than Dashboard Item | Description |
|---|---|---|---|
| Clip | ![Image_SizeMode_1_Clip](../../../../images/img20215.png) | ![Image_SizeMode_2_Clip](../../../../images/img20219.png) | The image is clipped if it is larger than the **Image** dashboard item. |
| Stretch | ![Image_SizeMode_1_Stretch](../../../../images/img20217.png) | ![Image_SizeMode_2_Stretch](../../../../images/img20221.png) | The image is stretched or shrunk to fit the size of the **Image** dashboard item. |
| Squeeze | ![Image_SizeMode_1_Squeeze](../../../../images/img20216.png) | ![Image_SizeMode_2_Squeeze](../../../../images/img20220.png) | If the dimensions of the **Image** dashboard item exceed those of the image it contains, the image is shown in full-size. Otherwise, the image is resized to fit the dimensions of the **Image** dashboard item. |
| Zoom | ![Image_SizeMode_1_Zoom](../../../../images/img20218.png) | ![Image_SizeMode_2_Zoom](../../../../images/img20222.png) | The image is sized proportionally (without clipping), so that it best fits the **Image** dashboard item. If the aspect ratio of the **Image** dashboard item is the same as the aspect ratio of the image, it will be resized to fit into the **Image** dashboard item while maintaining its aspect ratio. Otherwise, the image will be resized in the closest fitting dimension (either the height or the width), and the remaining dimension will be resized while maintaining the image's aspect ratio. |