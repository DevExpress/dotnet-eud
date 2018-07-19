---
title: Bar Code Recognition Specifics
author: Anna Gubareva
---
# Bar Code Recognition Specifics

This document describes the main specifics of bar code recognition and how to resolve the most frequently encountered issues when working with bar codes.

## Choose an Appropriate Bar Code Type
Selecting an appropriate bar code type (symbology) depends on your specific business requirements and the applied industrial standards.

In general, consider using [Bar Code 2 of 5 Interleaved](interleaved-2-of-5.md) for encoding digits and [Bar Code 39](code-39-usd-3.md) for encoding the full range of ASCII characters.

## Insert the Function Code One Character (FNC1) or the Application Identifier into a Bar Code
Some encodings enable you to insert a special **FNC1** character for separating application identifiers from the rest of the bar code.

According to the **GS1** specification, the **FNC1** character is always inserted at the first position of the encoded data. Other identifiers can be inserted manually using the default "**#**" character.

Although you can use any ASCII character as the **FNC1** placeholder, it will not be a part of the encoded data as it does not have any direct ASCII representation.

> [!NOTE]
> For the [Code 128](code-128.md) symbology, only **FNC1** characters are currently supported. At present, there is no way to define **FNC2** - **4** characters for this bar code.

For the list of the available application identifiers, refer to the official documentation at [www.gs1.org](http://www.gs1.org/).

## Specify the Bar Code Resolution on Export to Third-Party Formats
At present, only [export to PDF](../../../../print-preview/print-preview-for-winforms/exporting/pdf-specific-export-options.md) preserves the original bar code in its vector form. Export to other formats will keep only the rasterized version of a bar code (with the default DPI set to **96**).

For [XLSX](../../../../print-preview/print-preview-for-winforms/exporting/xlsx-specific-export-options.md) and [XLS](../../../../print-preview/print-preview-for-winforms/exporting/xls-specific-export-options.md) export, the output resolution can be set up manually using the **Rasterization Resolution** property.

## Common Issues
This document section provides solutions to the most common issues that you may encounter when creating bar codes.

* **The bar code is too "dense"**
	
	The more information you wish to encode, the more bars should be drawn and the larger the bar code should become.
	
	The bar code's **Module** property specifies the width of the narrowest bar in a bar code. Although you can set this property to a very small value, the actual value is determined by the maximum resolution of your bar code printer device. Alternatively, consider using the **Auto Module** option to automatically calculate the optimal bar size based on the current bar code dimensions.
	
	> [!NOTE]
	> When bar codes are "dense" and you are manually specifying the Module value, make sure that multiplying this value by the bar code printer resolution results in an integer number. Otherwise, rounding errors may occur on calculating the resulting bar width.
	> 
	> For example, when the Module is set to **0.015** inches and the printer resolution is **300** DPI, their product equals **4.5**, which may be rounded to **4** or **5** pixels for different bars and result in bar code recognition errors. In this case, the Module property should be set to **0.01333** (to make the bar width equal to **4** pixels) or to **0.01667** (to make the bar width equal to **5** pixels).
* **The bar code is correctly displayed on the preview but it is not scanned**
	
	Make sure that your scanner has been correctly set up to be able to recognize a specific kind of a bar code. If you are not certain about how to operate the scanner properly, please refer to its product manual.
	
	Avoid scanning bar codes from the monitor screen (e.g., using an application installed on your smartphone), because the screen DPI may not be sufficient to effectively recognize each particular bar.
* **The bar code is correctly displayed on the preview but it is scanned incorrectly**
	
	The cause for this problem may be an encoding issue specific to the "binary" input mode.
	
	By default, the **UTF-16** encoding is used. However, your scanner device may use a different encoding model or even a codepage (i.e., a specific table that maps abstract values to real human-understandable characters). For additional information on this subject, please refer to the specification of your scanner device.
* **The "There are invalid characters in the text" error occurs**
	
	Different bar code symbologies define different ranges of allowed characters under different character sets. To avoid this error, please check the bar code specification.