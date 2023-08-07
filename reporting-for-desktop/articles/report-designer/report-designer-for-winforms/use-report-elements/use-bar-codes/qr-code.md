---
title: QR Code
author: Anna Gubareva
---
# QR Code

A **QR Code** (**QR** is the abbreviation for **Quick Response**) is a two-dimensional code, readable by **QR** scanners, mobile phones with a camera, and smartphones. **QR Code** can encode textual, numeric and binary data.

![](../../../../../images/eurd-win-bar-code-qr-code.png)

## Add the Barcode to a Report

1. Drag the **Barcode** item from the report controls toolbox tab and drop it onto the report. 

    ![](../../../../../images/drag-and-drop-barcode.png)

2. Set the control’s **Symbology** property to **QRCode**. 

    ![](../../../../../images/qrcode-in-designer.png)

3. Specify [common](add-bar-codes-to-a-report.md) barcode properties and properties [specific](#specific-properties) to **QR Code**.

## Specific Properties

In the [property grid](../../report-designer-tools/ui-panels/property-grid-tabbed-view.md), expand the **Symbology** list and specify the following properties specific to **QR Code**:

* **Auto Module**
    Gets or sets whether the Module property value should be calculated automatically based upon the barcode's size.

* **Compaction Mode**

    Specifies whether numeric, alpha-numeric or byte information should be used as the barcode's data.
	
* **Error Correction Level**

    Specifies the amount of redundancy built into the barcode's coding, to compensate for calculation errors.

* **Version**

    Specifies the barcode's size.
	
* **Logo**

    Specifies the image that overlays the QR code.    
