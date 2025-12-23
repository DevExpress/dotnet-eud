---
title: Edit Content in Print Preview
---
# Edit Content in Print Preview

This document describes how to customize field values in a previewed document.

## <a name="enableediting"></a>Content Editing Overview
Enable a report control's **Edit Options** | **Enabled** property and leave the **Edit Options** | **Read Only** property disabled to make the control's content editable in Print Preview.

![editing-fields-label-edit-options-new](..\/..\/..\/images/eurd-win-editing-fields-label-edit-options-new.png)

Print Preview provides the **Editing Fields** toolbar button if content editing is enabled for at least one control in the displayed report. Click this button to highlight all editable fields available in the document.

![editing-fields-highlight-ribbon-toolbar-sample-report](..\/..\/..\/images/eurd-win-editing-fields-highlight-ribbon-toolbar-sample-report.png)

Use the TAB and SHIFT+TAB keys to navigate between editable fields forward and back.

Click an editable field to invoke an editor and specify a value.

You can enable content editing for data-aware and unbound report controls.

The following report controls support content editing in Print Preview:

| Text | Boolean | Image |
|--- | --- | --- |
| [Label param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  | [Check Box param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  | [Picture Box param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  |
| [Table Cell param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  | | |
| [Character Comb param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  | | |

The sections below provide information about options these controls expose. You can use these options to set up content editing.


## Content Editing Limitations

* Changes made to a control's content in Print Preview does not effect the document's other parts (for example, summary results, grouping, sorting, bookmarks and other settings that were processed before the document was generated).
* A control's **Can Grow** setting is ignored for editable fields. The edited area cannot exceed the control's original dimensions.
* Multi-line values can only be entered when no mask is applied to an editable field.  
* Values entered into editable fields are reset after the document is refreshed (for example, when you submit [report parameter param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  values or expand/collapse data in a [drill-down report param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } ).
* It is not possible to edit content in bands if their **DrillDownControl** property is specified.
* The entered values are not preserved in the Top Margin and Bottom Margin bands when the report is exported as a single file to the following formats:

    * TXT
    * CSV
	* HTML
	* MHT
	* RTF
	* XLS
	* XLSX
	* image

## Text Editors

Text editors are used to customize the [Label param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value } , [Table Cell param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  and [Character Comb param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  report controls' content in Print Preview.

The default text editor is a memo edit. 
	
	
![EditOptions_StandardMemoEditor](..\/..\/..\/images/eurd-win-editoptions_standardmemoeditor.png)


Specify the **Edit Options** | **Editor Name** property to use one of the following text editors:

![EditOptions_EditorName](..\/..\/..\/images/eurd-win-editoptions_editorname.png)

| Numeric | Date-Time | Letters |
| --- | --- | --- |
| Integer | Date | Only Letters | 
| Positive Integer | | Only Uppercase Letters |
| Fixed-Point | | Only Lowercase Letters |
| Positive Fixed-Point | | Only Latin Letters |

Each editor has a specific mask.
	
> [!NOTE]
> If a table cell contains other controls, you cannot edit this cell (they can edit the cell's controls). The following image illustrates this:
> 
> ![eurd-win-content-editing-table-cell-container](..\/..\/..\/images/eurd-win-content-editing-table-cell-container.png)

## Character Comb Editors

The **Character Comb** control displays text so that each character is printed in an individual cell.

![Character Comb](..\/..\/..\/images/eurd-win-character-comb-report-control.png)

Specify the Character Comb's **Edit Options** | **Editor Name** property to use a text editor, as described in the [Text Editors](#text-editors) section above.

## Check Box Editor
The check box editor is used to customize the [Check Box param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  report control's content in Print Preview.

![eurd-win-content-editing-checkboxe](..\/..\/..\/images/eurd-win-content-editing-checkboxe.png)

You can combine several check box editors into a radio group so that you can select only one option within a group at a time. For this, set the [Check Box param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  report controls' **Group ID** property to the same value.

![content-editing-check-box-group](..\/..\/..\/images/eurd-win-content-editing-check-box-group.png)

## Image Editors

Image editors are used to customize the [XRPictureBox param($match) $path = $match.Groups[1].Value; if ($path -notmatch '^https?://' -and $path -notmatch '^~/' -and $path -notmatch '^\.\./\.\./') { '](' + '../' + $path + '.md)' } else { $match.Value }  report control's content in Print Preview.

Use the control's **Edit Options** | **Editor Name** property to assign one of the following image editors.

- **Image Editor**  
    Allows you to load an image and specify the image's size options.

    ![content-editing-image](..\/..\/..\/images/eurd-win-content-editing-image.png)

- **Signature Editor**  
    Allows you to specify brush options and draw a signature.

    ![content-editing-signature](..\/..\/..\/images/eurd-win-content-editing-signature.png)
- **Image and Signature Editor** (default)  
    Allows you to load an image and draw a signature. The image's size options and brush options are available.

    ![content-editing-image-and-signature](..\/..\/..\/images/eurd-win-content-editing-image-and-signature.png)

All these image editors include the ![clear-changes](..\/..\/..\/images/eurd-win-clear-changes.png) button. This button allows you to clear the editor's content.

## Export Editable Fields to PDF AcroForms

Enable the report's **Export Options | PDF Export Options | Export Editing Fields to AcroForms** property to export [text fields](#text-editors), [check boxes](#check-box-editor), [character combs](#character-comb-editors), and [image editors](#image-editors) to PDF as editable form fields (**AcroForms**).

![Export Editing Fields to AcroForms](..\/..\/..\/images/eurd-win-exporteditingfieldstoacroforms.png)

![Report Preview](..\/..\/..\/images/eurd-win-editing-fields-preview.png)