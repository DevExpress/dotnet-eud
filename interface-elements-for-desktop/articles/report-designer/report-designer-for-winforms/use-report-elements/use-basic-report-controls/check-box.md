---
title: Check Box
author: Anna Gubareva
---
# Check Box

The **Check State** property specifies the checkbox state:

![report-control-check-box](../../../../../images/eurd-checkbox-checkstates.png)

The **Checked** checkbox indicates whether the checkbox is checked (displays a check mark) or not (is empty).

The **Text** property specifies the checkbox caption. Double-click the checkbox to invoke its in-place editor and type the caption text.

![report-control-check-box-text](../../../../../images/eurd-label-inline-editor.png)

## Bind to Data

Drag a Boolean field from the [Field List](../../../../../articles/report-designer/report-designer-for-winforms/report-designer-tools/ui-panels/field-list.md) onto your report. This adds a new checkbox to your report and binds its **Check State** property to the dragged field.

![report-control-check-box-add-from-toolbox](../../../../../images/eurd-checkbox-drag-from-fieldlist.png)

If you added a checkbox from the [Toolbox](../../../../../articles\report-designer\report-designer-for-winforms\report-designer-tools\toolbox.md), click the control's [smart tag](../../../../../articles/report-designer/report-designer-for-winforms/use-report-elements/manipulate-report-elements/select-report-elements-and-access-their-settings.md), expand the [](xref:DevExpress.XtraReports.UI.XRCheckBox.CheckState) property's **Expression** drop-down list and select a data field. This [binds](../../../../articles/report-designer/report-designer-for-winforms/bind-to-data.html) your control's [](xref:DevExpress.XtraReports.UI.XRCheckBox.CheckState) property to a data source field.

![report-control-check-box-bind-to-data](../../../../../images/eurd-chekbox-bind-to-data.png)

The data field value determines the checkbox state:

* **True** or **1** - activates the **Checked** state;
* **False** or **0** - activates the **Unchecked** state;
* Any other value - activates the **Indeterminate** state.

You can [bind](../../../../articles/report-designer/report-designer-for-winforms/bind-to-data.html) your control's [](xref:DevExpress.XtraReports.UI.XRCheckBox.CheckState) the checkbox caption to a data source field. Click the control's [smart tag](../../../../../articles/report-designer/report-designer-for-winforms/use-report-elements/manipulate-report-elements/select-report-elements-and-access-their-settings.md), expand the **Expression** drop-down list and select the data field.

The **Expression** option's ellipsis button invokes the **Expression Editor**. This Editor allows you to construct a complex binding expression with two or more fields.

![report-control-check-box-bind-to-data](../../../../../images/eurd-checkbox-expression-editor.png)

Refer to the [Bind to Data](../../../../articles/report-designer/report-designer-for-winforms/bind-to-data.html) topic for more information about the available data binding modes and how to create data-aware controls.

## Interactivity

Change the **Enabled** checkbox within the **Edit Options** group to specify if users can [change the checkbox state](../../../../../articles/report-designer/report-designer-for-winforms/provide-interactivity/edit-content-in-print-preview.md) in Print Preview.

![report-control-check-box-interactivity](../../../../../images/eurd-checkbox-enabled.png)

You can create checkbox groups to make them behave like radio lists. To group checkboxes, set their **Group ID** option within the **Edit Options** group a group ID value.

![report-control-check-box-interactivity](../../../../../images/eurd-checkbox-groupid.png)

## Customization

The **Glyph Options** property provides access to glyph settings.

* **Style** - specifies a predefined glyph style.

  ![report-control-check-box-customization](../../../../../images/eurd-checkbox-glyph-style.png)

* **Alignment** - specifies the glyph alignment within the control.

  ![report-control-check-box-customization](../../../../../images/eurd-checkbox-glyph-alignment.png)

* **Size** - specifies the glyph size.

* **Custom Glyphs** - specifies a custom glyph image for each checkbox state (Checked/Unchecked/Indeterminate).
