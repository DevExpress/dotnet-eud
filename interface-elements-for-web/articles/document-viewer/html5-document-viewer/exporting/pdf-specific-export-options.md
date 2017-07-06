---
title: PDF-Specific Export Options
---
# PDF-Specific Export Options
Before [exporting a document](../../../../../interface-elements-for-web/articles/document-viewer/html5-document-viewer/exporting/export-a-document.md) to PDF, you can specify PDF-specific options in the dedicated **Export Options** panel.

![EUD_HTML5DV_PdfExportOptions](../../../../images/Img121802.png)

## General Options
* **Convert Images to Jpeg**
	
	Specifies whether all bitmaps contained in the document should be converted to JPEG format during export to PDF.
* **Show Print Dialog on Open**
	
	Specifies whether the **Print** dialog should be displayed when the resulting PDF file is opened in an appropriate application.
* **Compressed**
	
	Specifies whether the resulting file should be compressed.
* **Never Embedded Fonts**
	
	Specifies font names which should not be embedded into the resulting file. To separate fonts, use semicolons.
* **Image Quality**
	
	Specifies the document's image quality level. The higher the quality, the bigger the file, and vice versa.
* **PDF A Compatibility**
	
	Specifies document compatibility with the **PDF/A** specification.
* **Page Range**
	
	Specifies a range of pages which will be included in the resulting file. To separate page numbers, use commas. To set page ranges, use hyphens.

## Document Options
The **Document Options** complex property contains options which specify the **Document Properties** of the created PDF file. Click the complex property's header to access its nested options.

![EUD_HTML5DV_PdfDocumentOptions](../../../../images/Img121803.png)

## PDF Password Security Options
This complex property allows you to adjust the security options of the resulting PDF file.

![EUD_HTML5DV_PdfSecurityOptions](../../../../images/Img121804.png)
* **OpenPassword**
	
	Specifies the password for opening the exported PDF document.
* **PermissionsPassword**
	
	Specifies the PDF permissions password for the document.
* **PDF Permissions Options**
	
	Provides access to the options which specify the permissions for printing, changing, copying and accessing the exported document.