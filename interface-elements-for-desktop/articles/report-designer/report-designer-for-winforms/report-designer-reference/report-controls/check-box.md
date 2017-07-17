---
title: Check Box
author: Eugeniy Burmistrov
legacyId: 5008
---
# Check Box
The **Check Box** control is intended to display True/False or Checked/Unchecked/Indeterminate states in a report, by displaying (or not) a check mark, which can be accompanied by a text description.

![RD_Controls_CheckBox](../../../../../images/img8503.png)

In the [Property Grid](../report-designer-ui/property-grid.md), the Check Box control's properties are divided into the following groups.

## Appearance
* **Background Color**
	
	Specifies the background color for the control. This option is also available in the [Formatting Toolbar](../report-designer-ui/formatting-toolbar.md) (![RD_Toolbars_Format_Back](../../../../../images/img8441.png)).
* **Borders**, **Border Color**, **Border Dash Style** and **Border Width**
	
	Specify border settings for the control.
* **Font**
	
	Specifies the font settings for the control. Some of these settings are available in the [Formatting Toolbar](../report-designer-ui/formatting-toolbar.md).
* **Foreground Color**
	
	Specifies the text color for the control. This option is also available in the [Formatting Toolbar](../report-designer-ui/formatting-toolbar.md) (![RD_Toolbars_Format_Color](../../../../../images/img8440.png)).
* **Formatting Rules**
	
	Invokes the Formatting Rules Editor allowing you to choose which rules should be applied to the control during report generation, and define the precedence of the applied rules. To learn more on this, refer to [Conditionally Change a Control's Appearance](../../create-reports/styles-and-conditional-formatting/conditionally-change-a-controls-appearance.md).
* **Glyph Alignment**
	
	Specifies the glyph alignment within the control.
	
	When this property is set to Center, the control's text is not shown.
	
	| Glyph Alignment = Near | Glyph Alignment = Center | Glyph Alignment = Far |
	|---|---|---|
	| ![check-box-glyph-alignment-near](../../../../../images/img125024.png) | ![check-box-glyph-alignment-center](../../../../../images/img125020.png) | ![check-box-glyph-alignment-far](../../../../../images/img125023.png) |
* **Padding**
	
	Specifies indent values which are used to render the contents of a Check Box.
* **Style Priority**
	
	Allows you to define the priority of various style elements (such as background color, border color, etc.). For more information on style inheritance, refer to [Understanding Style Concepts](../../create-reports/styles-and-conditional-formatting/understanding-style-concepts.md).
* **Styles**
	
	Specifies [odd and even styles](../../create-reports/styles-and-conditional-formatting/use-odd-and-even-styles.md) for the control and enables you to assign an existing style to the control (or a newly created one). To learn more, see [Understanding Style Concepts](../../create-reports/styles-and-conditional-formatting/understanding-style-concepts.md).
* **Text Alignment**
	
	Allows you to change the alignment of the control's text. This option is also available in the [Formatting Toolbar](../report-designer-ui/formatting-toolbar.md).
* **Text Trimming**
	
	Specifies the string trimming mode of the control's text.

## Behavior
* **Anchor Horizontally**
	
	Specifies the horizontal anchoring style of the control, so that after page rendering it stays attached to the left control, right control, or both. This property defines how a report control is resized to maintain the distance to the left and right edges of its container control.
* **Anchor Vertically**
	
	Specifies the vertical anchoring style of the control, so that after page rendering it stays attached to the top control, bottom control, or both. The property setting is useful for data-bound Check Boxes located between upper and lower controls, which are allowed to resize depending on their contents.
* **Can Publish**
	
	Specifies whether or not a report control is displayed in a printed or exported document.
* **Edit Options**
	
	Provides access to options that define whether and how a control's content can be edited in Print Preview. For more information, see [Enable Content Editing in Print Preview](../../create-reports/report-navigation-and-interactivity/enable-content-editing-in-print-preview.md).
* **Keep Together**
	
	Specifies whether the contents of a Check Box can be horizontally split across pages. In other words, if a Check Box occupies more space than remains on the page, this property specifies whether this Check Box should be split between the current page and the next, or whether it will be printed entirely on the next page. This property is in effect only when a Check Box's content does not fit on the current page. If it does not fit on the next page either, then the Check Box will be split despite this property's value.
* **Scripts**
	
	This property contains events, which you can handle with the required scripts. For more information on scripting, refer to [Handle Events via Scripts](../../create-reports/miscellaneous/handle-events-via-scripts.md).
* **Visible**
	
	Specifies whether the control should be visible in print preview.
* **Word Wrap**
	
	When this property is set to Yes, text entered into a Check Box is wrapped to the next line if it doesn't fit the line.

## Data
* **(Data Bindings)**
	
	If the current report is [bound to data](../../create-reports/binding-a-report-to-data.md), this property allows you to bind some of the control's properties (Bookmark, Check State, Navigation URL, Tag and Text) to a data field obtained from the report's data source, and to apply a [format string](../../report-editing-basics/change-value-formatting-of-report-elements.md) to it. For more information on this, refer to [Displaying Values from a Database (Binding Report Elements to Data)](../../report-editing-basics/displaying-values-from-a-database-(binding-report-elements-to-data).md).
* **Check State**
	
	This property allows you to quickly specify the Checked/Unchecked/Indeterminate state of a Check Box (the Indeterminate state is displayed as a grayed out checked box.) Note that if you only want to use Checked and Unchecked states, you may use the Checked property, instead.
* **Checked**
	
	This property allows you to define whether a Check Box is checked or not.
* **Tag**
	
	This property allows you to add some additional information to the control; for example its id, by which it can then be accessible via [scripts](../../create-reports/miscellaneous/handle-events-via-scripts.md).
	
	If the current [report has a data source](../../create-reports/binding-a-report-to-data.md), the Tag property can be bound to a data field obtained from the data source. To do this, expand the (Data Bindings) property and in the Tag.Binding drop-down selector, select the required data field.
* **Text**
	
	Allows you to define a line of static text to be displayed. Note that when a Check Box is selected in the designer, you may simply start typing the text, and it will be automatically entered into the in-place editor.
	
	![RD_Controls_Label_1](../../../../../images/img8287.png)
	
	If the current [report has a data source](../../create-reports/binding-a-report-to-data.md), the Text property can be bound to a data field obtained from the data source. To do this, expand the (Data Bindings) property, and in the Text.Binding drop-down selector, select the required data field. For more information on this, refer to [Displaying Values from a Database (Binding Report Elements to Data)](../../report-editing-basics/displaying-values-from-a-database-(binding-report-elements-to-data).md).
* **Xlsx Format String**
	
	Specifies the native XLSX format string for the control's content, which is to be preserved when the report is being [exported](../../../../print-preview/print-preview-for-winforms/exporting/exporting-from-print-preview.md) to XLSX. This format string is independent from the general [value formatting](../../report-editing-basics/change-value-formatting-of-report-elements.md).

## Design
* **(Name)**
	
	Determines a control's name, by which it can be accessed in the [Report Explorer](../report-designer-ui/report-explorer.md), [Property Grid](../report-designer-ui/property-grid.md) or via [scripts](../../create-reports/miscellaneous/handle-events-via-scripts.md).

## Layout
* **Location**
	
	Specifies the control's location, measured in [report units](../../create-reports/basic-operations/change-measurement-units-of-a-report.md).
* **Size**
	
	Specifies the control's size, measured in [report units](../../create-reports/basic-operations/change-measurement-units-of-a-report.md).
* **Snap Line Margin**
	
	Specifies the margin (measured in [report units](../../create-reports/basic-operations/change-measurement-units-of-a-report.md)), which is to be preserved around the control when it is [aligned using Snap Lines](../../create-reports/basic-operations/controls-positioning.md), or when other controls are aligned next to it.

## Navigation
* **Bookmark** and **Parent Bookmark**
	
	These properties are intended for the creation of a hierarchical structure within a report called a document map. For an explanation and help, refer to [Add Bookmarks](../../create-reports/report-navigation-and-interactivity/add-bookmarks.md).
	
	If the current [report has a data source](../../create-reports/binding-a-report-to-data.md), the Bookmark property can be bound to a data field obtained from the data source. To do this, expand the (Data Bindings) property and in the Bookmark.Binding drop-down selector, select the required data field.
* **Navigation URL** and **Navigation Target**
	
	Use the Navigation URL property to specify a URL for web browser navigation when a user clicks a Check Box. The web browser displays a page in a window or a frame as specified by the Navigation Target property. Note that a URL should have an appropriate prefix (e.g. "http://"). You can create cross-references within the report by assigning the name of the target control to the Navigation URL property, and setting the Navigation Target property to "_self". For more information, refer to [Create Hyperlinks](../../create-reports/report-navigation-and-interactivity/create-hyperlinks.md).
	
	If the current [report has a data source](../../create-reports/binding-a-report-to-data.md), the Navigation URL property can be bound to a data field obtained from the data source. To do this, expand the (Data Bindings) property and in the Navigation URL.Binding drop-down selector, select the required data field.

## Printing
* **Right to Left**
	
	Specifies the direction of text and check box position within the control. Use this option to correctly render text written in right-to-left languages.
	
	By default, all report controls have this property set to Inherit, so enabling it for a report will apply this setting to all its controls.
	
	The right-to-left layout is preserved when [exporting a report](../../../../print-preview/print-preview-for-winforms/exporting/exporting-from-print-preview.md) to any of the supported formats (e.g., PDF, Excel, or RTF).