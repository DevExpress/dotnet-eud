---
title: Rich Text
author: Anna Gubareva
---
# Rich Text

## Overview
The **Rich Text** control displays formatted text (static, dynamic or mixed) in your report.

To add this control to a report, drag the **Rich Text** item from the [Toolbox](../../report-designer-tools/toolbox.md) onto the report's area.

![](../../../../../images/eurd-win-add-rich-text-to-report.png)

You can load RTF or HTML content from an external file. Click the control's smart tag and select **Load File**.

![](../../../../../images/eurd-win-rich-text-load-file.png)

In the invoked **Open** dialog, use the drop-down list to define the file's extension (**.rtf**, **.docx**, **.txt**, **.htm** or **.html**), select the file and click **Open**.

You can double-click the Rich Text to invoke its in-place editor and enter static text. Use the [Toolbar](../../report-designer-tools/toolbar.md)'s **Font** group to format the text. 

![](../../../../../images/eurd-win-rich-text-in-place-editor.png)

Press CTRL+Enter to submit changes and exit the in-place editor.


> [!NOTE]
> The Rich Text's content is exported as plain text only when exporting to XLS or XLSX format.

## Bind to Data

You can [bind](../../bind-to-data/bind-controls-to-data-expression-bindings.md) the control's **RTF** property to a data field obtained from a report's data source. Click the control's smart tag, expand the **Rtf Expression**'s drop-down list and select the data field.
 
![](../../../../../images/eurd-win-rich-text-bind-to-data.png)

You can bind the control to a data field that provides HTML content in the same way. To do this, click the control's smart tag and use the **Html Expression**'s drop-down list.

Click the **Rtf Expression** or **Html Expression** option's ellipsis button to invoke the **Expression Editor**. This editor allows you to construct a complex binding expression with two or more data fields. 

You can also drag and drop any field from the [Field List](../../report-designer-tools/ui-panels/field-list.md) with the right mouse button and select the **Rich Text** menu item. This creates a new Rich Text control bound to this field.

![](../../../../../images/eurd-win-rich-text-drop-fom-field-list.png)

The Rich Text also enables you to merge data fields and static content in its text. 

![](../../../../../images/eurd-win-rich-text-mail-merge.png)

See the [Bind Controls to Data](../../bind-to-data/bind-controls-to-data-expression-bindings.md) and [Use Embedded Fields](../../bind-to-data/use-embedded-fields-mail-merge.md) topics for more information.
