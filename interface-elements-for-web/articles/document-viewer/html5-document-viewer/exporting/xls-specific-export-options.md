---
title: XLS-Specific Export Options
---
Before [exporting a document](../../../../../interface-elements-for-web/articles/document-viewer/html5-document-viewer/exporting/export-a-document.md) to XLS format, you can specify XLS-specific options in the dedicated **Export Options** panel.

![EUD_HTML5DV_XlsExportOptions](../../../../images/Img121833.png)
* **Export Mode**
	
	Specifies how a document is exported to XLS.
* **Export Hyperlinks**
	
	Specifies whether hyperlinks should be exported to the XLS document.
* **Page Range**
	
	Specifies a range of pages which will be included in the resulting file. To separate page numbers, use commas. To set page ranges, use hyphens.
* **Raw Data Mode**
	
	Specifies whether to enable the raw data export mode. In this mode, only a document's actual data is exported to XLS, ignoring non-relevant elements, such as images, graphic content, font and appearance settings.
* **Sheet Name**
	
	Specifies the name of the sheet in the created XLS file.
* **Show Grid Lines**
	
	Specifies whether grid lines should be visible in the resulting XLS file.
* **Suppress 256 Columns Warning**
	
	Specifies whether to suppress the warning that appears if the resulting XLS file has more than **256** columns.
* **Suppress 65536 Rows Warning**
	
	Specifies whether to suppress the warning that appears if the resulting XLS file has more than **65,536** rows.
* **Text Export Mode**
	
	Specifies whether value formatting should be converted to the native XLS format string (if it is possible), or embedded into cell values as plain text.
* **Workbook Color Palette Compliance**
	
	Specifies the color palette compatibility mode with different workbook versions. The workbook palette can store no more than **56** colors. If you select the **ReducePaletteExactColors** value, original color values are kept, but only the first **56** colors are included in the palette. Choose **AdjustColorsToDefaultPalette** to degrade the color values to match the **56** standard colors of the default workbook palette.