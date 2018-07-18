---
title: Code 93 Extended
author: Anna Gubareva
---
# Code 93 Extended

Using **Code 93**'s "Full ASCII Mode", it is possible to encode all **128** ASCII characters. This is accomplished by using the (**$**), (**/**), (**%**), and (**&#0043;**) symbols as "shift" characters. These characters combined with the single character that follows indicate which Full ASCII character is to be used.

![](../../../../../images/eurd-win-bar-code-code-93-extended.png)

The following property is specific to the **Code 93 Extended** type and available in the [Property Grid](../../report-designer-tools/ui-panels/property-grid) under the **Symbology** property:

* **Calculate a Checksum**

    Specifies whether to calculate a checksum for the bar code.

    > [!NOTE]
	> A checksum of a **Code 93 Extended** bar code can contain characters that are not supported by this bar code symbology. For this reason, the checksum is not included in the **Code 93 Extended** bar code's displayed text.