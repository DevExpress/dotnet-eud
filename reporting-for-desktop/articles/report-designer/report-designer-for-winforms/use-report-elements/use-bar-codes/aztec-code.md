---
title: Aztec Code
author: Natalia Kazakova
---
# Aztec Code

**Aztec Code** is a matrix code that has the potential to use less space than other matrix barcodes because it does not require a surrounding blank "quiet zone". Aztec codes are widely used for transport ticketing.

![Aztec Code](~/reporting-for-desktop/images/bar-code-aztec-code.png)

Refer to the following article for more details: [Aztec Code](https://en.wikipedia.org/wiki/Aztec_Code).

## Add the Barcode to a Report

1. Drag the **Barcode** item from the report controls toolbox tab and drop it onto the report. 

    ![](~/reporting-for-desktop/images/drag-and-drop-barcode.png)

2. Set the control's **Symbology** property to **Aztec Code**. 

    ![](~/reporting-for-desktop/images/aztec-code-in-designer-win.png)

3. Specify [common](add-bar-codes-to-a-report.md) barcode properties and properties [specific](#specific-properties) to **Aztec Code**.

## Specific Properties

In the [property grid](../../report-designer-tools/ui-panels/property-grid-tabbed-view.md), expand the **Symbology** list and specify the following properties specific to **Aztec Code**:

- **Compaction Mode**

  Specifies whether text or binary mode should be used to encode the barcode's data.

- **Error Correction Level**

  Specifies the amount of redundancy built into the bar code to compensate for calculation errors.

- **Version**
  
  Specifies the Aztec Code version.