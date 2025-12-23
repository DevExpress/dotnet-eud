---
title: Rich Text
author: Anna Gubareva
---
# Rich Text

## Overview
The **Rich Text** control displays formatted text (static, dynamic or mixed) in your report.

To add this control to a report, drag the **Rich Text** item from the [Toolbox param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  onto the report's area.

![](..\/..\/..\/..\/images/eurd-win-add-rich-text-to-report.png)

You can load RTF or HTML content from an external file. Click the control's smart tag and select **Load File**.

![](..\/..\/..\/..\/images/eurd-win-rich-text-load-file.png)

In the invoked **Open** dialog, use the drop-down list to define the file's extension (**.rtf**, **.docx**, **.txt**, **.htm** or **.html**), select the file and click **Open**.

You can double-click the Rich Text to invoke its in-place editor and enter static text. Use the [Toolbar param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } 's **Font** group to format the text. 

![](..\/..\/..\/..\/images/eurd-win-rich-text-in-place-editor.png)

Press CTRL+Enter to submit changes and exit the in-place editor.


> [!NOTE]
> The Rich Text's content is exported as plain text only when exporting to XLS or XLSX format.

## Bind to Data

You can [bind param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  the control's **RTF** property to a data field obtained from a report's data source. Click the control's smart tag, expand the **Rtf Expression**'s drop-down list and select the data field.
 
![](..\/..\/..\/..\/images/eurd-win-rich-text-bind-to-data.png)

You can bind the control to a data field that provides HTML content in the same way. To do this, click the control's smart tag and use the **Html Expression**'s drop-down list.

Click the **Rtf Expression** or **Html Expression** option's ellipsis button to invoke the **Expression Editor**. This editor allows you to construct a complex binding expression with two or more data fields. 

You can also drag and drop any field from the [Field List param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  with the right mouse button and select the **Rich Text** menu item. This creates a new Rich Text control bound to this field.

![](..\/..\/..\/..\/images/eurd-win-rich-text-drop-fom-field-list.png)

The Rich Text also enables you to merge data fields and static content in its text. 

![](..\/..\/..\/..\/images/eurd-win-rich-text-mail-merge.png)

See the [Bind Controls to Data param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  and [Use Embedded Fields param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  topics for more information.

## Markup Text

### Supported Tags

The table below lists the supported HTML tags. External links are processed for inline pictures and style sheets (CSS files). The ID and Class attributes are interpreted for all tags, including the unlisted ones. These attributes are used to specify a style for content within a certain tag.

| Tag | Attributes | Notes |
---------|----------|---------
| a | dir |  |
| b | dir |  |
| base |  |  |
| basefont | size<br/>color<br/>face<br/>dir |  |
| big | dir |  |
| blockquote | dir |  |
| br | dir |  |
| center | dir |  |
| code | dir |  |
| del | cite<br/>datetime |  |
| div | page-break-before<br/>page-break-after<br/>page-break-inside<br/>background-color<br/>border (CSS)<br/>dir | Only the **always** property value is supported for the **page-break-before** tag. |
| em | dir |  |
| font | size<br/>color<br/>face<br/>dir |  |
| h1-h6 | align<br/>dir | |
| head |  |  |
| html |  |  |
| hr | align<br/>color<br/>noshade<br/>size<br/>width |  |
| i | dir |  |
| ins | cite<br/>datetime |  |
| img | align<br/>src<br/>height<br/>width | If the **align** attribute is not specified, the image is considered as inline. |
| li | type<br/>value<br/>dir |  |
| link | href<br/>type<br/>media<br/>dir |  |
| meta |  |  |
| ol | type<br/>value<br/>align<br/>dir |  |
| p | align<br/>dir |  |
| script |  | Text inside this tag is ignored. |
| small |  |  |
| span |  |  |
| strike | dir |  |
| strong | dir |  |
| style |  |  |
| sub | dir |  |
| sup | dir |  |
| table | align<br/>bgcolor<br/>border<br/>bordercolor<br/>cellpadding<br/>cellspacing<br/>dir<br/>width | The **dir** attribute reorders table columns. |
| td | align<br/>bgcolor<br/>bordercolor<br/>colspan<br/>height<br/>nowrap<br/>rowspan<br/>text-align<br/>valign<br/>width | The **align** tag is supported in the Internet Explorer only.<br/>The **Rich Text** control's interpretation of the **bordercolor** attribute is different from the HTML browser. |
| th | any allowed |  |
| tr | align<br/>bgcolor<br/>bordercolor<br/>height<br/>text-align<br/>valign | The **align** attribute is supported in the Internet Explorer only. |
| title |  | Text inside this tag is ignored. |
| u | dir |  |
| ul | dir |  |

### Unsupported Tags

* &lt;base&gt; tag with _href_ attribute;
* &lt;div&gt; tag with _border_, _align_ and _float_ CSS attribute;
* &lt;li&gt; tag with _list-style-image_ CSS attribute;
* &lt;margin&gt; tag;
* &lt;tab&gt; tag;
* &lt;table&gt; tag with _cols_ attribute;
* &lt;td&gt; tab with _bordercolor_ and _nowrap_ attributes;
* _!important_ declaration;
* _word-wrap_ and _break-word_ css properties;
* css3 shapes;
* &lt;ui&gt; tag with _type_ attribute.

### Export to Excel

When a report is exported to XLS or XLSX, the following rich-text content is converted from **Rich Text** controls into Excel-native rich-text content:

| | HTML Tags and RTF Equivalents |
| --- | --- |
| Text format | \<b>, \<i>, \<u>, \<s>, \<strong>, \<em> |
| Line break | \<br> |
| Non-breaking space | \&nbsp; |
| Font | \<font face=**[font name]**> |
| Font size | \<font size=**[font size]**> |
| Foreground color | \<font color=**[color]**> |
