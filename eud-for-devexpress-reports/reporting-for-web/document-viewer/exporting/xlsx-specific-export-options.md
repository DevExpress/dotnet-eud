---
title: XLSX Export Options
author: Anna Gubareva
legacyId: 115384
---
# XLSX Export Options

Before you [export a document](export-a-document.md) to XLSX format, you can specify XLSX-specific options in the **Export Options** panel.

![Web Document Viewer - XLSX Export Options panel](../../images/img121837.png)

* **Export Mode**
	
	Specifies how a document is exported to XLSX. The following modes are available:
	* The **Single File** mode allows you to export a document to a single file without dividing it into pages.
	* The **Single File PageByPage** mode allows you to export a document to a single file while preserving the page-by-page breakdown. In this mode, the **Page Range** option is available.
* **Export Hyperlinks**
	
	Specifies whether to include hyperlinks in the resulting file.
* **Page Range**
	
	Specifies a range of pages to include in the resulting file. To separate page numbers, use commas. To set page ranges, use hyphens.
* **Raw Data Mode**
	
	Specifies whether to enable the raw data export mode. In this mode, only a document's actual data is exported to XLSX, ignoring non-relevant elements, such as images, graphic content, font and appearance settings.
* **Sheet Name**
	
	Specifies the name of the sheet in the created XLSX file.
* **Show Grid Lines**
	
	Specifies whether to show grid lines in the resulting XLSX file.
* **Text Export Mode**
	
	Specifies whether to convert value formatting to the native XLSX format string (if possible) or embed it into cell values as plain text.
* **Rasterize Images**
	
	Specifies whether to rasterize vector images, such as pictures, charts, or barcodes.
* **Rasterization Resolution**
	
	Specifies the image resolution for raster images.
* **Fit To Printed Page Width**
	
	Shrinks the width of the exported document's printout to one page.
* **Fit To Printed Page Height**
	
	Shrinks the height of the exported document's printout to one page.
* **Ignore Errors**
	
	Specifies which document errors to ignore in the resulting XLSX file.
* **Right To Left Document**
	
	If you use right-to-left fonts in a report, enable the **Right-to-Left Document** option to use the right-to-left layout for sheets in the exported XLSX file.

## Document Options
The **Document Options** complex property contains options that specify the **Document Properties** of the created XLSX file. Click the complex property's header to access its nested options.

![XLSX Document Options panel](../../images/img1218331.png)

## Encryption Options
This complex property allows you to adjust the encryption options of the resulting XLSX file.

![XLSX Encryption Options panel](../../images/img1218332.png)
* **Type**
	Specifies one of the following encryption types:
	* Strong (default) type uses the **Agile Encryption** mechanism.
	* Compatible type uses the **Standard Encryption** that is compatible with Excel 2007.
* **Password**
	Sets a password for the exported XLSX file. Passwords for XLSX files are stored as plain text in report definitions. Ensure that only trusted parties have access to report definition files.

