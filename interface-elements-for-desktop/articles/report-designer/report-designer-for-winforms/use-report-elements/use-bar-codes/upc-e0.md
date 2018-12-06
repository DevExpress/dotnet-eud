---
title: UPC-E0
author: Anna Gubareva
---
# UPC-E0

**UPC-E** is a variation of **UPC-A** which allows for a more compact bar code by eliminating "extra" zeros. Since the resulting **UPC-E** bar code is about half the size as an **UPC-A** bar code, **UPC-E** is generally used on products with very small packaging, where a full **UPC-A** bar code could not reasonably fit.

The **UPC-E0** is a kind of **UPC-E** code with the number system set to **0**. In the human readable string of the bar code the first digit signifies the number system (always **0** for this code type), and the last digit is the check digit of the original **UPC-A** code.

In the example below,  the original **UPC-A** code is "**04210000526**". We should remove the leading zero when assigning the string to the control's property, since the code format itself implies its presence. The checksum digit (**4**) is calculated automatically, and the symbology algorithm transforms the rest of the numeral string. The result is **425261**, and it is encoded along with the number system prefix and the check digit into the scanner-readable form.

![](../../../../../images/eurd-win-bar-code-upc-e0.png)


Not every **UPC-A** code can be transformed into the **UPC-E0** (it must meet special requirements). 