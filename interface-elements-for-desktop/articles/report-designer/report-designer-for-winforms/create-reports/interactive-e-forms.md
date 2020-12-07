---
title: Interactive E-Forms
author: Anna Gubareva
---
# Interactive E-Forms

This tutorial describes how to create a form that is fillable in Print Preview.

![eForm-report-result](../../../../images/eurd-win-EForm-Result.png)

To get started with this tutorial, [create a new report](../add-new-reports.md) or [open an existing one](../open-reports.md).

## Add Form Fields

Add the [Label](..\use-report-elements\use-basic-report-controls\label.md) report controls to the report and arrange them according to the form's template. Set the labels' **Text** property to the form's field names.

![EForm-Add-Form-Fields](../../../../images/eurd-win-EForm-Add-Form-Fields.png)

## Add Fillable Cells

Use the [Character Comb](..\use-report-elements\use-basic-report-controls\character-comb.md) control for the form's text fields. This control displays letters in individual cells and allows you to fill these cells in Print Preview.

1. Drop the Character Comb item from the Toolbox onto the report.
	
	![eForm-report-add-character-comb](../../../../images/eurd-win-EForms-Character-Comb.png)
2. Select all the added Character Combs and set their properties in the **Property Grid**:
	- **Cell Size Mode**
	- **Cell Height**,
	- **Cell Width**,
	- and other cell settings.
	
	![eForm-report-character-combs-cell-settings](../../../../images/eurd-win-eform-report-character-combs-cell-settings.png)
3. Enable the Character Combs' **Edit Options** 
| **Enabled** property.
	
	![eForm-report-character-combs-edit-options-enabled](../../../../images/eurd-win-eform-report-character-combs-edit-options-enabled.png)
4. Choose editors for the Character Comb controls' edit mode.

	- Controls that allow you to enter letters  
		Invoke a drop-down list for the **Editor Name** property and select the **Only Uppercase Letters** item in the **Letters** category.
	
		![eForm-report-character-combs-editor-name-letters](../../../../images/eurd-win-eform-report-character-combs-editor-name-letters.png)

	- Controls that allow you to enter integers  
		Invoke a drop-down list for the **Editor Name** property and select the **Positive Integer** item in the **Numeric** category.
	
		![eForm-report-character-combs-editor-name-integer-positive](../../../../images/eurd-win-eform-report-character-combs-editor-name-integer-positive.png)

## Add Check Box Editors

Add [Check Box](..\use-report-elements\use-basic-report-controls\check-box.md) controls for the *Male/Female* fields.

![eForm-report-add-check-boxes](../../../../images/eurd-win-eform-report-add-check-boxes.png)

Use the following properties to set up these controls:

- Set the **Text** property.

- Set appearance properties.

- Enable the **Edit Options** | **Enabled** property switch check box states in Print Preview.

- Set the **Edit Options** | **Group ID** property to the same value to combine these two check boxes into a logical group. This allows you to select only one option at a time.
	
	![eForm-report-check-boxes-edit-options](../../../../images/eurd-win-eform-report-check-boxes-edit-options.png)

## Add the Signature Editor

Add the [PictureBox](..\use-report-elements\use-basic-report-controls\picture-box.md) report control for the form's *Signature* field.

![EForm-add-signature-picture-box](../../../../images/eurd-win-EForm-add-signature-picture-box.png)

Do the following to enable drawing in Print Preview:

1. Enable the control's **Edit Options** | **Enabled** property.

2. Set the **Edit Options** | **Editor Name** property to **Signature**.

	![EForm-Signature-content-editing](../../../../images/eurd-win-EForm-Signature-content-editing.png)

## Get the Result
Switch to the [Preview tab](..\preview-print-and-export-reports.md) to see the result.

![eForm-report-result](../../../../images/eurd-win-EForm-Preview.png)

Click the ![highlight-fields-icon-bars](../../../../images/eurd-win-highlight-fields-icon-bars126306.png) button on the Print Preview toolbar to highlight all the editable fields on the form.

![eForm-report-result](../../../../images/eurd-win-EForm-Preview-Editing-Fields.png)


Click a field to invoke its editor. 

![eForm-report-result](../../../../images/eurd-win-EForm-Result.png)

Use TAB and SHIFT+TAB to navigate between editable fields.