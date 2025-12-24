---
title: Preview, Print and Export Reports
---
# Preview, Print and Export Reports

## Preview a Report
To switch a report to the print preview mode, click the **Preview** tab. You will see your report populated with data and broken down into pages, as specified.

![eurd-win-preview](../../images/eurd-win-preview.png)

## Print a Report

When in the Print Preview mode, you can print out your report using the appropriate menu and toolbar commands.

![eurd-win-print](../../images/eurd-win-print.png)

## Export a Report

When in the Print Preview mode, you can export your report to files in different formats. The resulting files can either be saved to the hard drive or sent by e-mail.

![eurd-win-export](../../images/eurd-win-export.png)


The following documents describe the basics of report exporting and format-specific export options.
<<<<<<<< HEAD:eud-for-devexpress-reports/reporting-for-desktop/report-designer/report-designer-for-winforms/preview-print-and-export-reports.md
* <!-- [Exporting from Print Preview](~/interface-elements-for-desktop/print-preview/print-preview-for-winforms/exporting/exporting-from-print-preview.md) - Link disabled: interface-elements not included -->
* <!-- [PDF-Specific Export Options](~/interface-elements-for-desktop/print-preview/print-preview-for-winforms/exporting/pdf-specific-export-options.md) - Link disabled: interface-elements not included -->
* <!-- [HTML-Specific Export Options](~/interface-elements-for-desktop/print-preview/print-preview-for-winforms/exporting/html-specific-export-options.md) - Link disabled: interface-elements not included -->
* <!-- [MHT-Specific Export Options](~/interface-elements-for-desktop/print-preview/print-preview-for-winforms/exporting/mht-specific-export-options.md) - Link disabled: interface-elements not included -->
* <!-- [RTF-Specific Export Options](~/interface-elements-for-desktop/print-preview/print-preview-for-winforms/exporting/rtf-specific-export-options.md) - Link disabled: interface-elements not included -->
* <!-- [XLS-Specific Export Options](~/interface-elements-for-desktop/print-preview/print-preview-for-winforms/exporting/xls-specific-export-options.md) - Link disabled: interface-elements not included -->
* <!-- [XLSX-Specific Export Options](~/interface-elements-for-desktop/print-preview/print-preview-for-winforms/exporting/xlsx-specific-export-options.md) - Link disabled: interface-elements not included -->
* <!-- [CSV-Specific Export Options](~/interface-elements-for-desktop/print-preview/print-preview-for-winforms/exporting/csv-specific-export-options.md) - Link disabled: interface-elements not included -->
* <!-- [TXT-Specific Export Options](~/interface-elements-for-desktop/print-preview/print-preview-for-winforms/exporting/txt-specific-export-options.md) - Link disabled: interface-elements not included -->
* <!-- [Image-Specific Export Options](~/interface-elements-for-desktop/print-preview/print-preview-for-winforms/exporting/image-specific-export-options.md) - Link disabled: interface-elements not included -->
========
* <!-- [Exporting from Print Preview](~/interface-elements-for-desktop/articles/print-preview/print-preview-for-winforms/exporting/exporting-from-print-preview.md) - Link disabled: interface-elements not included -->
* <!-- [PDF-Specific Export Options](~/interface-elements-for-desktop/articles/print-preview/print-preview-for-winforms/exporting/pdf-specific-export-options.md) - Link disabled: interface-elements not included -->
* <!-- [HTML-Specific Export Options](~/interface-elements-for-desktop/articles/print-preview/print-preview-for-winforms/exporting/html-specific-export-options.md) - Link disabled: interface-elements not included -->
* <!-- [MHT-Specific Export Options](~/interface-elements-for-desktop/articles/print-preview/print-preview-for-winforms/exporting/mht-specific-export-options.md) - Link disabled: interface-elements not included -->
* <!-- [RTF-Specific Export Options](~/interface-elements-for-desktop/articles/print-preview/print-preview-for-winforms/exporting/rtf-specific-export-options.md) - Link disabled: interface-elements not included -->
* <!-- [XLS-Specific Export Options](~/interface-elements-for-desktop/articles/print-preview/print-preview-for-winforms/exporting/xls-specific-export-options.md) - Link disabled: interface-elements not included -->
* <!-- [XLSX-Specific Export Options](~/interface-elements-for-desktop/articles/print-preview/print-preview-for-winforms/exporting/xlsx-specific-export-options.md) - Link disabled: interface-elements not included -->
* <!-- [CSV-Specific Export Options](~/interface-elements-for-desktop/articles/print-preview/print-preview-for-winforms/exporting/csv-specific-export-options.md) - Link disabled: interface-elements not included -->
* <!-- [TXT-Specific Export Options](~/interface-elements-for-desktop/articles/print-preview/print-preview-for-winforms/exporting/txt-specific-export-options.md) - Link disabled: interface-elements not included -->
* <!-- [Image-Specific Export Options](~/interface-elements-for-desktop/articles/print-preview/print-preview-for-winforms/exporting/image-specific-export-options.md) - Link disabled: interface-elements not included -->
>>>>>>>> 05df5c28763b4aa9fb5c78d15422603198f71820:eud-for-devexpress-reports/reporting-for-desktop/articles/report-designer/report-designer-for-winforms/preview-print-and-export-reports.md


## Hide Report Controls in Documents Exported to Specific Formats

You can specify the **Can Publish Options** setting in the Properties grid to exclude report controls from certain export formats.

## Export a Report to PDF with Accessible Tags (PDF/UA Compatibility)

You can specify how Label, Table, Table Row, and Table Cell should be treated by screen readers in the exported PDF document.

When you export a report to PDF, the report elements have no role. Assistive software commonly treats such elements as HTML <div> tags. Change the element’s role to one of the values listed below to help the screen reader correctly identify the element’s purpose in the exported PDF document.

### Define Label Accessible Role

Set the control’s **Accessible Role** property to **Heading 1 - Heading 6** before you export a report.

In the PDF Export Options dialog, set the **PDF/UA Compatibility** property to **PDF/UA1** to conform the exported PDF document to PDF/UA specification. Then, export the report to PDF format.

The result: **Accessible Role** is set to **Heading 2**, and the screen reader treats **Label** as a "level two" heading in the exported document.

### Define Table Accessible Role

You can specify how Table should be treated by screen readers in the exported PDF document. For this, set the control's **Accessible Role** property to **Table** before you export a report.

In the PDF Export Options dialog, set the **PDF/UA Compatibility** property to **PDF/UA1** to conform the exported PDF document to PDF/UA specification. Then, export the report to PDF format.

The result: **Accessible Role** is set to **Table**, and the screen reader treats Table as a table in the exported document.

### Define Table Row Accessible Role

You can specify how Table Row should be treated by screen readers in the exported PDF document. 

Before you export a report, set the **Table**'s **Accessible Role** property to **Table** to define a control as a table. Then, specify **Table Row**'s **Accessible Role**.

In the PDF Export Options dialog, set the **PDF/UA Compatibility** property to **PDF/UA1** to conform the exported PDF document to PDF/UA specification. Then, export the report to PDF format.

The result: **Table Row**'s **Accessible Role** is set to **Table Header Row**, and the screen reader treats **Table Row** as a header row of the table in the exported document. 

### Define Table Cell Accessible Role

Before you export a report, set the **Table**'s **Accessible Role** property to **Table** to define a control as a table. Then, specify the **Table Cell**'s **Accessible Role** property.

> [!NOTE]
> **Accessible Role** is not in effect for cells merged with the Cell's **Row Span** property. 

In the PDF Export Options dialog, set the **PDF/UA Compatibility** property to **PDF/UA1** to conform the exported PDF document to PDF/UA specification. Then, export the report to PDF format.

The result: **Table Cell**'s **Accessible Role** is set to **Table Header Cell**, and the screen reader treats Table Cell with "Bill to:" text as a header cell in the exported document.
