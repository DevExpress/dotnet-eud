---
title: Mail Merge
author: Anna Kondratova
legacyId: 113845
---
# Mail Merge
Document fields are special placeholders for non-static data that might change (be updated on a field update). These placeholders are replaced with actual data when the document is rendered for display or printing. Use buttons in the **Mail Merge** tab to work with fields.


To insert a field, position the mouse cursor in a document and click the **Create Field** button in the **Mail Merge** tab (or press CTRL+F9).

![EUD_ASPxRichEdit_MailMerge_CreateField](../../images/img118711.png)

You can use the following field codes:

* **DATE** - Inserts the current date and time.
* **TIME** - Inserts the current time.
* **PAGE** - Inserts the number of the page containing the field.
* **NUMPAGES** - Inserts the total number of pages.
* **MERGEFIELD** - Inserts a field merged with a data source.
* **DOCVARIABLE** - Enables you to programmatically insert complex content when this field is updated.



The **Show All Field Codes** button displays field codes for all fields in the document.

The **Show All Field Results** button displays field results for all fields in the document.

To calculate a field result, the field needs to be updated. Fields are updated automatically when the document is saved or printed. 

Click the **Update All Fields** button to update fields manually, or select a field(s) and press F9.

