---
title: 'General Tools: File'
author: Eugeniy Burmistrov
legacyId: 17329
---
# General Tools: File
The **File** toolbar contains the basic file management and printing commands.

These commands are divided into the following categories.
* [Common](#common)
* [Data](#data)

## <a name="common"/>Common
| Command | Large Icon | Small Icon | Description |
|---|---|---|---|
| New | ![icon-toolbar-common-new](../../../../images/img20392.png) | ![icon-small-toolbar-common-new](../../../../images/img20406.png) | Creates a new Snap document. |
| Open | ![icon-toolbar-common-open](../../../../images/img20394.png) | ![icon-small-toolbar-common-open](../../../../images/img20407.png) | Opens an existing document. |
| Save | ![icon-toolbar-common-save](../../../../images/img20393.png) | ![icon-small-toolbar-common-save](../../../../images/img20412.png) | Saves a document template to an SNX file. When saving a document for the first time, the **Save As** dialog will appear. |
| Save As | ![icon-toolbar-common-save-as](../../../../images/img20396.png) | ![icon-small-toolbar-common-save-as](../../../../images/img20413.png) | Saves a document template to a new SNX file. This command invokes the **Save As** dialog, allowing you to specify a name and location for the new file. |
| Export... | ![icon-toolbar-common-export-document](../../../../images/img20395.png) | ![icon-small-toolbar-common-export](../../../../images/img20405.png) | Exports a document into one of the supported third-party formats (**DOC**, **DOCX**, **HTML**, **PDF**, **RTF**, **Image**, etc.). |
| Quick Print | ![icon-toolbar-common-quick-print](../../../../images/img20399.png) | ![icon-small-toolbar-common-quick-print](../../../../images/img20410.png) | Sends a document to the default printer with default printing options. |
| Print | ![icon-toolbar-common-print](../../../../images/img20398.png) | ![icon-small-toolbar-common-print](../../../../images/img20408.png) | Invokes the **Print** dialog, allowing you to select a printer and specify the printing options. |
| Print Preview | ![icon-toolbar-common-print-preview](../../../../images/img20397.png) | ![icon-small-toolbar-common-print-preview](../../../../images/img20409.png) | Retrieves all data required to populate the report **fields** to assemble and preview a document before publishing, ignoring the current [Editor Row Limit](data-tools-list.md) setting. Calling this command for a mail-merge document renders only one page of the document. To render a mail-merge document for a specified range of data records, use the **Finish &amp; Merge** option in the [Data Tools: Mail Merge](data-tools-mail-merge.md) tab. |
| Undo | ![icon-toolbar-common-undo](../../../../images/img20400.png) | ![icon-small-toolbar-common-undo](../../../../images/img20414.png) | Cancels the last change made to the document. |
| Redo | ![icon-toolbar-common-redo](../../../../images/img20401.png) | ![icon-small-toolbar-common-redo](../../../../images/img20411.png) | Reverses the results of the last undo. |

## <a name="data"/>Data
| Command | Large&nbsp;Icon | Small&nbsp;Icon | Description |
|---|---|---|---|
| Add New Data Source | ![icon-toolbar-data-add-new-data-source](../../../../images/img20402.png) | ![icon-small-toolbar-common-data-add-new-data-source](../../../../images/img20404.png) | Invokes the **Create Data Source wizard**, allowing you [to connect the document to a new data source](../../connect-to-data/connect-a-document-to-a-data-source.md) and specify its data connection options (e.g., data provider, login information and connection name). A data table selected with the wizard is included in the data source. To add more tables and specify their data relations, use the [Query Designer](../../connect-to-data/use-the-query-builder.md). |