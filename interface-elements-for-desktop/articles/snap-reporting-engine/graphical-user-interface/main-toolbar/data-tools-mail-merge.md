---
title: 'Data Tools: Mail Merge'
---
# Data Tools: Mail Merge
The commands available in the **Mail Merge** section of the **Data Tools** toolbar are divided into the following categories.
* [Data](#data)
* [Current Record](#currentrecord)
* [Publish](#publish)

## <a name="data"/>Data
| Command | Large&nbsp;Icon | Small&nbsp;Icon | Description |
|---|---|---|---|
| Data Source | ![icon-toolbar-mail-merge-data-source](../../../../images/Img22258.png) | ![icon-small-toolbar-mail-merge-data-source](../../../../images/Img22253.png) | Enables **mail merge** for a connected data source. After enabling this mode, the data source icon is displayed in green in the [Data Explorer](../../../../../interface-elements-for-desktop/articles/snap-reporting-engine/graphical-user-interface/snap-application-elements/data-explorer.md). There is no functionality for disabling mail merge once it has been implemented. |
| Filter | ![icon-toolbar-mail-merge-filter](../../../../images/Img22259.png) | ![icon-small-toolbar-mail-merge-filter](../../../../images/Img22254.png) | Invokes the **FilterString Editor** to [filter data](../../../../../interface-elements-for-desktop/articles/snap-reporting-engine/connect-to-data/filter-data.md) in a mail merge document. |
| Sort | ![icon-toolbar-mail-merge-sort](../../../../images/Img22261.png) | ![icon-small-toolbar-mail-merge-sort](../../../../images/Img22256.png) | Invokes the **Sort** dialog to [sort data](../../../../../interface-elements-for-desktop/articles/snap-reporting-engine/connect-to-data/sort-data.md) in a mail merge document. |

## <a name="currentrecord"/>Current Record
| Command | Icon | Description |
|---|---|---|
| Current Record | ![icon-toolbar-mail-merge-current-record](../../../../images/Img22257.png) | Allows you to navigate through records in a mail merge document. You can navigate to the **Next Page**, the **Previous Page**, the **First Page** or the **Last Page**. |

## <a name="publish"/>Publish
| Command | Large&nbsp;Icon | Small&nbsp;Icon | Description |
|---|---|---|---|
| Finish&nbsp;&amp;&nbsp;Merge | ![icon-toolbar-mail-merge-finish-and-merge](../../../../images/Img22260.png) | ![icon-small-toolbar-mail-merge-merge](../../../../images/Img22255.png) | Finalizes a mail merge document by supplying actual values to data elements added to a document template. This command invokes a drop-down menu to select the publishing format of a document. The following options are available:**Export** - exports the created document to a selected third-party format; **Print** - invokes the print dialog to adjust the page options of the document before sending it to a printer; **Print Preview** - displays the created document in a print preview window that provides options to navigate, print and/or export the document. |

After selecting the document's output format, the **Export Range** dialog is invoked to specify the range of data records that the document should include.

![snap-mail-merge-export-range-dialog](../../../../images/Img22262.png)

In this dialog, you can choose from the following separators to isolate different data records:
* **None**;
* **Page Break**;
* **Section (Next Page)**;
* **Section (Even Page)**;
* **Section (Odd Page)**;
* **Paragraph**.