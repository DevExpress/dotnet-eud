---
title: Interleaved 2 of 5
author: Anna Gubareva
---
# Interleaved 2 of 5

**Interleaved 2 of 5** is a higher-density numerical barcode based upon the **Standard 2 of 5** symbology. It is used primarily in the distribution and warehouse industry.

![](..\/..\/..\/..\/images/eurd-win-bar-code-interleaved-2-of-5.png)

## Add the Barcode to a Report

1. Drag the **Barcode** item from the report controls toolbox tab and drop it onto the report. 

    ![](..\/..\/..\/..\/images/drag-and-drop-barcode.png)

2. Set the control’s **Symbology** property to **Interleaved2of5**. 

    ![](..\/..\/..\/..\/images/interleaved-2-of-5-in-designer.png)

3. Specify [common param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  barcode properties and properties [specific](#specific-properties) to **Interleaved 2 of 5**.

## Specific Properties

In the [property grid param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } , expand the **Symbology** list and specify the following properties specific to **Interleaved 2 of 5**:

* **Calculate a Checksum**

    Specifies whether to calculate a checksum for the barcode.

* **Wide Narrow Ratio**

    Specifies the density of a barcode's bars.