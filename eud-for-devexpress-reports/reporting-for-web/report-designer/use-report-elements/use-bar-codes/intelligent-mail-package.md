---
title: Intelligent Mail Package
author: Anna Vekhina
---
# Intelligent Mail Package

The **Intelligent Mail Package Barcode** (**IMPB**) was developed for the use on mail in the United States. Barcodes of this symbology are used only for packages as opposed to [Intelligent Mail param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  barcodes, which are used for postcards, letters, and flats.

This barcode is capable of encoding package tracking information required for more efficient sorting and delivering of packages with the capability of piece-level tracking.

![](..\/..\/..\/images/eurd-web-bar-code-intelligent-mail-package.png)

## Add the Barcode to a Report

1. Drag the **Barcode** item from the report controls toolbox tab and drop it onto the report. 

    ![](..\/..\/..\/images/eurd-web-add-bar-code-to-report.png)

2. Set the control’s **Symbology** property to **IntelligentMailPackage**. 

    ![](..\/..\/..\/images/intelligent-mail-package-in-designer.png)

3. Specify [common param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  barcode properties and properties [specific](#specific-properties) to **Intelligent Mail Package**.

## Specific Properties

In the [property grid param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } , expand the **Symbology** list and specify the following property specific to **Intelligent Mail Package**:

* **FNC1 Functional Character**
	
	Specifies the symbol (or set of symbols) in the barcode text that will be replaced with the **FNC1** functional character when the barcode's bars are drawn.