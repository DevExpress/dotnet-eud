---
title: GS1 - DataBar
author: Anna Vekhina
---
# GS1 - DataBar

The **GS1 DataBar** barcode is based on a family of symbols often used in the **GS1 DataBar Coupon** (coupon codes commonly used in retail).

These barcodes can encode up to **14** digits, which makes them suitable for **GTIN 8**, **12**, **13** and **14**.

**GS1 DataBar Expanded** and **GS1 DataBar Expanded Stacked** can encode up to **74** numeric or **41** alphanumeric characters, and provide the capability to utilize all **GS1 Application Identifiers** (e.g., expiration date, batch and serial number). These barcodes are often used in manufacturer coupons.

![](../../../../images/eurd-web-bar-code-gs1-databar.png)

## Add the Barcode to a Report

1. Drag the **Barcode** item from the report controls toolbox tab and drop it onto the report. 

    ![](../../../../images/eurd-web-add-bar-code-to-report.png)

2. Set the control’s **Symbology** property to **DataBar**. 

    ![](../../../../images/data-bar-in-designer.png)

3. Specify [common](add-bar-codes-to-a-report.md) barcode properties and properties [specific](#specific-properties) to **Data Bar**.

## Specific Properties

In the [property grid](../../report-designer-tools/ui-panels/properties-panel.md), expand the **Symbology** list and specify the following properties specific to **Data Bar**:

* **FNC1 Functional Character**
	
	Specifies the symbol (or set of symbols) in the barcode text that will be replaced with the **FNC1** functional character when the barcode's bars are drawn.

* **Segments In Row**
	
	Specifies the number of data segments per row in the Expanded Stacked type of a GS1 DataBar barcode.

* **Type**
	
	Specifies the type of a GS1 DataBar barcode.
