---
title: Context Menu
author: Svetlana Nikulina
legacyId: 11833
---
# Context Menu
A **Context menu** is displayed when you right-click the content (text, image, table, etc.) in the editor.

A context menu can be invoked only in the editor's Design and HTML [view modes](view-modes.md).

![ASPxHtmlEditor-DesignView](../../../images/img11322.png)

## Context Menu Commands
The context menu contains the following commands.

| Command | Description |
|---|---|
| **Commands available in Design view** |
| Cut | Cuts the selection to the clipboard. (See the note below the table) |
| Copy | Copies the selection to the clipboard. (See the note below the table) |
| Paste | Pastes content from the clipboard to the current cursor position. (See the note below the table) |
| Select All | Selects all editor content. |
| Unlink | Removes the current link element. |
| Change Link... | Invokes the **Change Link** dialog for the current link. |
| Change Image... | Invokes the **Change Image** dialog for the current image. |
| Change Audio... | Invokes the **Change Audio** dialog for the current audio element. |
| Change Video... | Invokes the **Change Video** dialog for the current video element. |
| Change Flash... | Invokes the **Change Flash** dialog for the current flash element. |
| Change YouTube Video... | Invokes the **Change YouTube Video** dialog for the current YouTube video element. |
| Change Placeholder... | Invokes the **Change Placeholder** dialog for the current placeholder. |
| Table Properties... | Invokes the **Table Properties** dialog for the current table. |
| Row Properties... | Invokes the **Row Properties** dialog for the current row. |
| Column Properties... | Invokes the **Column Properties** dialog for the current column. |
| Cell Properties... | Invokes the **Cell Properties** dialog for the current cell. |
| Insert Table | Insert a new table |
| Insert Row Above | Inserts a table row above the current one. |
| Insert Row Below | Inserts a table row below the current one. |
| Insert Column to the Left | Inserts a table column to the left of the current one. |
| Insert Column to the Right | Inserts a table column to the right of the current one. |
| Split Horizontally | Splits the current cell horizontally into two cells. |
| Split Vertically | Splits the current cell vertically into two cells. |
| Merge Right | Merges the current table cell with the right one. |
| Merge Down | Merges the current table cell with the bottom one. |
| Delete Table | Deletes the current table. |
| Delete Row | Deletes the current table row. |
| Delete Column | Deletes the current table column. |
| **Commands available in the HTML view** |
| Outdent | Decrease an indent for the current paragraph. |
| Indent | Increase an indent for the current paragraph. |
| Comment | Comments the selected code lines. |
| Uncomment | Uncomments the selected HTML. |
| Format Document | Formats the HTML document. |
| Collapse Tag | Collapses the current tag. |
| Expand Tage | Expands the current tag. |

Default command visibility is switched based on the currently selected element.

> [!NOTE]
> Some browsers (e.g., Firefox, Chrome) do not allow scripts to work with the clipboard for security reasons. Therefore, the Cut, Copy, and Paste commands are removed from the context menu for these browsers.