---
title: UPC Shipping Container Symbol (ITF-14)
author: Anna Vekhina
---
# UPC Shipping Container Symbol (ITF-14)

The **UPC Shipping Container Symbol** (**ITF-14**) barcode is used to mark packaging materials that contain products labeled with a **UPC** or **EAN** product identification number.

This barcode provides a **GS1** implementation of an **Interleaved 2 of 5** barcode for encoding a **Global Trade Item Number** (an identifier for trade items developed by **GS1**). This barcode always uses a total of **14** digits.

The thick black border around the symbol (the **Bearer Bar**) is intended to improve barcode reading reliability.

![](../../../../images/eurd-web-bar-code-itf-14.png)

## Add the Barcode to a Report

1. Drag the **Barcode** item from the report controls toolbox tab and drop it onto the report. 

    ![](../../../../images/eurd-web-add-bar-code-to-report.png)

2. Set the control’s **Symbology** property to **ITF14**. 

    ![](../../../../images/itf14-in-designer.png)

3. Specify [common](add-bar-codes-to-a-report.md) barcode properties and properties [specific](#specific-properties) to **ITF14**.

## Specific Properties

In the [property grid](../../report-designer-tools/ui-panels/properties-panel.md), expand the **Symbology** list and specify the following properties specific to **ITF14**:

* **Calculate a Checksum**

    Specifies whether to calculate a checksum for the barcode.

* **Wide Narrow Ratio**

    Specifies the density of a barcode's bars.