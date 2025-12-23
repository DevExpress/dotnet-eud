---
title: UPC Supplemental 5
author: Anna Gubareva
---
# UPC Supplemental 5

**5**-digit supplemental barcodes are used on books to indicate the suggested retail price.

![](..\/..\/..\/..\/images/eurd-win-bar-code-upc-supplemental-5.png)

## Add the Barcode to a Report

1. Drag the **Barcode** item from the report controls toolbox tab and drop it onto the report. 

    ![](..\/..\/..\/..\/images/drag-and-drop-barcode.png)

2. Set the control’s **Symbology** property to **UPCSupplemental5**. 

    ![](..\/..\/..\/..\/images/upc-supplemental-5-in-designer.png)

3. Specify [common param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  barcode properties.