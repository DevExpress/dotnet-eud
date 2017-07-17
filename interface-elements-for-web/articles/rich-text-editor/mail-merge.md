---
title: Mail Merge
author: Anna Kondratova
legacyId: 113845
---
# Mail Merge
Document fields are special placeholders for non-static data that might change (be updated on a field update). These placeholders are replaced with actual data when the document is rendered for display or printing. The default **Mail Merge** tab can be used to work with fields (create, update, switch between field display modes).

To insert a field, position the mouse cursor within a document and select the **Create Field** button in the **Mail Merge** tab (or use the **Ctrl+F9** shortcut). Field codes appear between curly brackets ( { } ).

![EUD_ASPxRichEdit_MailMerge_CreateField](../../images/img118711.png)

The following field codes are supported:

**DATE** - Inserts the current date and time.

**TIME** - Inserts the current time.

**DOCVARIABLE** - Enables you to programmatically insert complex content when this field is updated.

**HYPERLINK** - Enables you to navigate to another location or to a bookmark.

**NUMPAGES** - Inserts the total number of pages.

**PAGE** - Inserts the number of the page containing the field.