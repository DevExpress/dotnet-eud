---
title: PDF Export Options
author: Anna Gubareva
legacyId: 115380
---
# PDF Export Options

Before you [export a document](export-a-document.md) to PDF, you can specify PDF-specific options in the **Export Options** panel.

![Web Document Viewer - PDF Export Options panel](../../images/img121802.png)

## General Options

* **Signatures**

	Provides access to digital signatures. Select a signature to sign the document on export to PDF.
* **Convert Images to JPEG**
	
	Specifies whether to convert all bitmaps in the document to JPEG format on export to PDF.
* **Show Print Dialog on Open**
	
	Specifies whether to display the **Print** dialog when the user opens the resulting PDF file in a PDF viewer.
* **Never Embed Fonts**
	
	Specifies font names to exclude from embedding in the resulting file. To separate fonts, use semicolons.
* **Export Editing Fields To AcroForms**
	
	Specifies whether to convert a report's editing fields to interactive forms.

* **Image Quality**
	
	Specifies the document's image quality level. The higher the quality, the bigger the file, and vice versa.
* **PDF A Compatibility**
	
	Specifies document compatibility with the **PDF/A** specification.
* **Page Range**
	
	Specifies a range of pages to include in the resulting file. To separate page numbers, use commas. To set page ranges, use hyphens.
* **Rasterization Resolution**
	
	Specifies the image resolution for raster images.

## Document Options
The **Document Options** complex property contains options that specify the **Document Properties** of the created PDF file. Click the complex property's header to access its nested options.

![Web Document Viewer - PDF Document Options panel](../../images/img121803.png)

## PDF Password Security Options
This complex property allows you to adjust the security options of the resulting PDF file.

![Web Document Viewer - PDF Password Security Options panel](../../images/img121804.png)
* **Open Password**
	
	Specifies the password for opening the exported PDF document.
* **Encryption Level**
	
	Specifies the algorithm used to encrypt PDF content.
* **Permissions Password**
	
	Specifies the PDF permissions password for the document.
* **PDF Permissions Options**
	
	Provides access to the options that specify the permissions for printing, changing, copying, and accessing the exported document.