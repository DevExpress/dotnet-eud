---
title: Industrial 2 of 5
author: Anna Gubareva
---
# Industrial 2 of 5

**Industrial 2 of 5** is a low-density numerical barcode that is used in the photofinishing and warehouse sorting industries, as well as to sequentially number airline tickets.

![](..\/..\/..\/..\/images/eurd-win-bar-code-industrial-2-of-5.png)

## Add the Barcode to a Report

1. Drag the **Barcode** item from the report controls toolbox tab and drop it onto the report. 

    ![](..\/..\/..\/..\/images/drag-and-drop-barcode.png)

2. Set the control’s **Symbology** property to **Industrial2of5**. 

    ![](..\/..\/..\/..\/images/industrial-2-of-5-in-designer.png)

3. Specify [common param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  barcode properties and properties [specific](#specific-properties) to **Industrial2of5**.

## Specific Properties

In the [property grid param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } , expand the **Symbology** list and specify the following properties specific to **Industrial 2 of 5**:

* **Calculate a Checksum**

    Specifies whether to calculate a checksum for the barcode.

* **Wide Narrow Ratio**

    Specifies the density of a barcode's bars.