---
title: GS1- Data Matrix
author: Anna Gubareva
---
# GS1- Data Matrix

The **GS1 Data Matrix** uses a special start combination to differentiate the **GS1 DataMatrix** symbol from other **Data Matrix ECC 200** symbols. This is achieved by using the **Function 1 Symbol Character** (**FNC1**) in the first position of the encoded data. It enables scanners to process the information according to the **GS1 System Rules**.

![](../../../../../images/eurd-win-bar-code-gs1-datamatrix.png)

The following properties are specific to the **GS1 DataMatrix** type and available in the [Property Grid](../../report-designer-tools/ui-panels/property-grid) under the **Symbology** property:


* **FNC1 Functional Character**
	
	Specifies the symbol (or set of symbols) in the bar code text that will be replaced with the **FNC1** functional character when the bar code's bars are drawn.

* **Human-Readable Text**

    Specifies whether or not parentheses should be included in the bar code's text to improve the readability of the bar code's text.

* **Matrix Size**

	Specifies the bar code matrix size.