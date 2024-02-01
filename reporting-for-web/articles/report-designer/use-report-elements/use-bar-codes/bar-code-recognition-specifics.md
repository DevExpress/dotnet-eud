---
title: Barcode Recognition Specifics
author: Anna Vekhina
---
# Barcode Recognition Specifics

This document describes the main specifics of barcode recognition and how to resolve the most frequently encountered issues when working with barcodes.

## Choose an Appropriate Barcode Type
Selecting an appropriate barcode type (symbology) depends on your specific business requirements and the applied industrial standards.

In general, consider using [Barcode 2 of 5 Interleaved](interleaved-2-of-5.md) for encoding digits and [Barcode 39](code-39-usd-3.md) for encoding the full range of ASCII characters.

## Insert the Function Code Characters (FNC) or the Application Identifier into a Barcode

Some encodings enable you to insert a special **FNC1** character for separating application identifiers from the rest of the barcode.

According to the **GS1** specification, the **FNC1** character is always inserted at the first position of the encoded data. Other identifiers can be inserted manually using the default "**#**" character.

Although you can use any ASCII character as the **FNC1** placeholder, it will not be a part of the encoded data as it does not have any direct ASCII representation.

For the [Code 128](code-128.md) symbology, you can also define **FNC2-4** characters.

For the list of the available application identifiers, refer to the official documentation at [www.gs1.org](http://www.gs1.org/).

## Specify the Barcode Resolution on Export to Third-Party Formats
At present, only [export to PDF](../../../document-viewer/exporting/pdf-specific-export-options.md) preserves the original barcode in its vector form. Export to other formats will keep only the rasterized version of a barcode (with the default DPI set to **96**).

For [XLSX](../../../document-viewer/exporting/xlsx-specific-export-options.md) and [XLS](../../../document-viewer/exporting/xls-specific-export-options.md) export, the output resolution can be set up manually using the **Rasterization Resolution** property.

## Specify the DPI of the Device Used to Print the Bar Code

The **Target Device Dpi** property allows you to specify the DPI of the device on which you wish to print your barcode. The `XRBarCode` control automatically adjusts bar density based on this property's value.

Use the **Target Device Dpi** property to ensure that the bar code is scanned correctly on the target device. This is especially important if your printing device has a non-standard DPI setting.

## Common Issues
This document section provides solutions to the most common issues that you may encounter when creating barcodes.

* **The barcode is too "dense"**
	
	The more information you wish to encode, the more bars should be drawn and the larger the barcode should become.
	
	The barcode's **Module** property specifies the width of the narrowest bar in a barcode. Although you can set this property to a very small value, the actual value is determined by the maximum resolution of your barcode printer device. Alternatively, consider using the **Auto Module** option to automatically calculate the optimal bar size based on the current barcode dimensions.
	
	> [!NOTE]
	> When barcodes are "dense" and you are manually specifying the Module value, make sure that multiplying this value by the barcode printer resolution results in an integer number. Otherwise, rounding errors may occur on calculating the resulting bar width.
	> 
	> For example, when the Module is set to **0.015** inches and the printer resolution is **300** DPI, their product equals **4.5**, which may be rounded to **4** or **5** pixels for different bars and result in barcode recognition errors. In this case, the Module property should be set to **0.01333** (to make the bar width equal to **4** pixels) or to **0.01667** (to make the bar width equal to **5** pixels).
* **The barcode is correctly displayed on the preview but it is not scanned**
	
	Make sure that your scanner has been correctly set up to be able to recognize a specific kind of a barcode. If you are not certain about how to operate the scanner properly, please refer to its product manual.
	
	Avoid scanning barcodes from the monitor screen (e.g., using an application installed on your smartphone), because the screen DPI may not be sufficient to effectively recognize each particular bar.
* **The barcode is correctly displayed on the preview but it is scanned incorrectly**
	
	The cause for this problem may be an encoding issue specific to the "binary" input mode.
	
	By default, the **UTF-16** encoding is used. However, your scanner device may use a different encoding model or even a codepage (i.e., a specific table that maps abstract values to real human-understandable characters). For additional information on this subject, please refer to the specification of your scanner device.
* **The "There are invalid characters in the text" error occurs**
	
	Different barcode symbologies define different ranges of allowed characters under different character sets. To avoid this error, please check the barcode specification.