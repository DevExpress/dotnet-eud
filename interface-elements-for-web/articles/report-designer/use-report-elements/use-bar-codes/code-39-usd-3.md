---
title: Code 39 (USD-3)
author: Anna Vekhina
---
# Code 39 (USD-3)

**Code 39**, the first alpha-numeric symbology to be developed, is still widely used, particularly in non-retail environments. It is the standard bar code used by the United States Department of Defense, and is also used by the Health Industry Bar Code Council (HIBCC). **Code 39** is also known as "**3 of 9 Code**" and "**USD-3**".

![](../../../../images/eurd-web-bar-code-code-39.png)

## Add the Bar Code to a Report

1. Drag the **Bar Code** item from the report controls toolbox tab and drop it onto the report. 

    ![](../../../../images/eurd-web-add-bar-code-to-report.png)

2. Set the control’s **Symbology** property to **Code39**. 

    ![](../../../../images/code-39-in-designer.png)

3. Specify [common](add-bar-codes-to-a-report.md) barcode properties and properties [specific](#specific-properties) to **Code 39**.

## Specific Properties

In the [property grid](../../report-designer-tools/ui-panels/properties-panel.md), expand the **Symbology** list and specify the following properties specific to **Code 39**:

* **Calculate a Checksum**

    Specifies whether to calculate a checksum for the bar code.

* **Wide Narrow Ratio**

    Specifies the density of a bar code's bars.