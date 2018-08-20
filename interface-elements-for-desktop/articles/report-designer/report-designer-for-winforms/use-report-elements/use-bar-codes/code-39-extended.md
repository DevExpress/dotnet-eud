---
title: Code 39 Extended
author: Anna Gubareva
---
# Code 39 Extended

Using **Code 39**'s "Full ASCII Mode", it is possible to encode all **128** ASCII characters. This is accomplished by using the (**$**), (**/**), (**%**), and (**&#0043;**) symbols as "shift" characters. These characters combined with the single character that follows indicate which Full ASCII character is to be used.

![](../../../../../images/eurd-win-bar-code-code-39-extended.png)

The following properties are specific to the **Code 39 Extended** type and listed in the [Property Grid](../../report-designer-tools/ui-panels/property-grid) under the **Symbology** property:

* **Calculate a Checksum**

    Specifies whether to calculate a checksum for the bar code.

* **Wide Narrow Ratio**

    Specifies the density of a bar code's bars.

The **Code 39 Extended** bar code, as opposed to [Code 39](code-39-usd-3.md), automatically replaces all necessary characters with special symbols, when required. This means that you do not need to do this manually, otherwise, the result will be incorrect.

For example, if you want to insert a "TAB" character into a bar code's text, use "\t", which will be replaced by "$I" for coding, and then into "TAB" after scanning:

| Property | Value |
|---|---|
| Bar code's text: | "12345\t678" |
| Coded text: | "12345$I678" |
| Scanned text: | "12345[TAB]678" |

The checksum is not considered to be part of a bar code's text and checksum characters are never replaced. When the bar code's **Show Text** and **Calculate a Checksum** properties are enabled, the bar code will not display a checksum character. This is required to avoid mistakenly treating a checksum as part of bar code text.