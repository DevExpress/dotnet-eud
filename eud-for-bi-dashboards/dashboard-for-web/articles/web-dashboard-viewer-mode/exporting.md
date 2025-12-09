---
title: Exporting
author: Natalia Kazakova
legacyId: 16727
---
# Exporting
The Web Dashboard provides the capability to export an entire dashboard and individual items.
* [Exporting Dashboards](#exportingdashboards)
* [Exporting Dashboard Items](#exportingdashboarditems)

## <a name="exportingdashboards"/>Exporting Dashboards
To export the entire dashboard, click the ![Printing_ExportElementButtonWeb](../../images/img19570.png) button in the [dashboard title](data-presentation/dashboard-layout.md) area and select the required format.

![Printing_ExportMenuWeb](../../images/img19567.png)

### Export to PDF

Invokes a corresponding dialog that allows you to export a dashboard to a PDF file with specific options. The following options are available:

![ExportToPDF_DashboardOptions](../../images/img22288.png)
* **File Name** - Specifies the name of the exported PDF file.
* **Page Layout** - Specifies the page orientation used to export a dashboard. You can select between _Portrait_, _Landscape_ and _Auto_. Note that in the _Auto_ mode, page orientation is selected automatically depending on the horizontal and vertical sizes of a dashboard.
* **Size** - Specifies the standard paper size (for instance, _Letter_ or _A4_).
* **Show Title** - Specifies whether or not to apply the dashboard title to the exported document title.
* **Title** - Specifies the title of the exported document.
* **Scale Mode** - Specifies the mode for scaling when exporting a dashboard.
	
	> [!NOTE]
	> Note that this option is in effect when **Page Layout** is set to a value different from _Auto_.
* **Include | Filters** - Allows you to include master filter values to the exported document.
* **Include | Parameters** - Allows you to include parameter values to the exported document.
* **Position** - Specifies the position of the master filter and parameter values in the exported document. You can select between _Below_ and _Separate Page_.

### Export to Image

Invokes a corresponding dialog that allows you to export a dashboard to an image in the specified format. The following options are available.

![ExportToImage_DashboardOptions](../../images/img22289.png)
* **File Name** - Specifies the name of the exported PDF file.
* **Show Title** - Specifies whether or not to apply the dashboard title to the exported document title.
* **Title** - Specifies the title of the exported document.
* **Image Format** - Specifies the image format in which the dashboard is exported. The following formats are available: _PNG_, _JPEG_, _SVG_, and _GIF_.
* **Resolution (dpi)** - Specifies the resolution (in dpi) used to export a dashboard.
* **Include | Filters** - Allows you to include master filter values to the exported document.
* **Include | Parameters** - Allows you to include parameter values to the exported document.

### Export to Excel

Invokes a corresponding dialog that allows end-users to export dashboard's data to the Excel file. The following options are available:

![ExportToExcel_DashboardOptions_Web](../../images/img128222.png)
* **File Name** - Specifies the name of the exported Image file.
* **Excel Format** - Specifies the Excel workbook format in which the dashboard's data is exported. You can select between _XLSX_ and _XLS_.
* **Include | Filters** - Allows you to include master filter values to the exported document.
* **Include | Parameters** - Allows you to include parameter values to the exported document.
* **Position** - Specifies the position of the master filter and parameter values in the exported document. You can select between _Below_ and _Separate Sheet_.

Specify the required options in the invoked dialog and click the **Export** button to export the dashboard. To reset changes to the default values, click the **Reset** button.

## <a name="exportingdashboarditems"/>Exporting Dashboard Items
To export a dashboard item, click the ![Printing_ExportElementButtonWeb](../../images/img19570.png) button in its [caption](data-presentation/dashboard-layout.md) and choose the required action.

![Printing_ExportElementWeb](../../images/img19610.png)
* **Export to PDF** - Invokes a corresponding dialog that allows you to export a dashboard to a PDF file with specific options.
* **Export to Image** - Invokes a corresponding dialog that allows you to export a dashboard to image in the specified format.
* **Export to Excel** - Invokes a corresponding dialog that allows you to export a dashboard item's data to the Excel workbook or CSV file.

To learn more about exporting specifics of different dashboard items, see the **Exporting** topic for the required [dashboard item](dashboard-items.md).