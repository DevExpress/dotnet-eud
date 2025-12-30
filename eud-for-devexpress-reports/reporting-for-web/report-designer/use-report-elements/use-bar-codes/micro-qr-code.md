---
title: Micro QR Code
author: Natalia Kazakova
---
# Micro QR Code

A **Micro QR Code** is a two-dimensional code. It is a more compact version of a standard [QR code](qr-code.md): a Micro QR Code can encode up to 35 numeric characters or 21 alphanumeric characters, enough to store a product ID or a short URL. In comparison, a standard QR code can contain up to 7,089 characters.

Micro QR Codes are often used in industries such as electronics, medical devices, and retail, where space-efficient labeling is essential.

![micro-qr-code](../../../images/micro-qr-code.png)

Refer to the following article for more information: [Micro QR Code](https://www.qrcode.com/en/codes/microqr.html).

## Add the Barcode to a Report

1. Drag the **Barcode** item from the report controls toolbox tab and drop it onto the report. 

    ![add barcode to report designer](../../../images/eurd-web-add-bar-code-to-report.png)

2. Set the control’s **Symbology** property to **Micro QR Code**. 

    ![Micro QR Code Properties](../../../images/micro-qrcode-in-designer-web.png)

3. Specify [common](add-bar-codes-to-a-report.md) barcode properties and properties [specific](#specific-properties) to **Micro QR Code**.

## Specific Properties

In the [property grid](../../report-designer-tools/ui-panels/properties-panel.md), expand the **Symbology** list and specify the following properties specific to **Micro QR Code**:

- **Compaction Mode**
  
  Specifies whether the barcode contains a number, an alphanumeric string, or a byte array.

- **Error Correction Level**
  
  Specifies the amount of redundancy built into the Micro QR code to compensate for calculation errors.

- **Include Quiet Zone**

  Specifies whether to add a blank space around the Micro QR code to help separate the Micro QR code from neighboring elements.

- **Version**
  
  Gets or sets the barcode’s version.