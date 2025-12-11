---
title: Code 128
author: Anna Vekhina
---
# Code 128

**Code 128** is a very effective, high-density symbology which permits the encoding of alphanumeric data. The symbology includes a checksum digit for verification, and the barcode can also be verified character-by-character, allowing the parity of each data byte to be verified.

This symbology has been widely implemented in many applications where a relatively large amount of data must be encoded in a relatively small amount of space. Its specific structure also allows numerical data to be effectively encoded at double-density.

![](../../../../images/eurd-web-bar-code-code-128.png)

## Add the Barcode to a Report

1. Drag the **Barcode** item from the report controls toolbox tab and drop it onto the report. 

    ![](../../../../images/eurd-web-add-bar-code-to-report.png)

2. Set the control’s **Symbology** property to **Code128**. 

    ![](../../../../images/code-128-in-designer.png)

3. Specify [common](add-bar-codes-to-a-report.md) barcode properties and properties [specific](#specific-properties) to **Code 128**.

## Specific Properties

In the [property grid](../../report-designer-tools/ui-panels/properties-panel.md), expand the **Symbology** list and specify the following properties specific to **Code 128**:

* **Character Set**
	
	Specifies the set of symbols which can be used when setting the barcode's text.

* **FNC1 Functional Character**
  
    A substring/character that serves as the placeholder for the FNC1 functional character.

* **FNC2 Functional Character**
  
    A substring/character that serves as the placeholder for the FNC2 functional character.

* **FNC3 Functional Character**
  
    A substring/character that serves as the placeholder for the FNC3 functional character.

* **FNC4 Functional Character**
  
    A substring/character that serves as the placeholder for the FNC4 functional character.