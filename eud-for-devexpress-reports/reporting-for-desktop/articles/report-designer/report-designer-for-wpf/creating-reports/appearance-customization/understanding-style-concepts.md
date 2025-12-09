---
title: Understanding Style Concepts
author: Anna Gubareva
legacyId: 116335
---
# Understanding Style Concepts
This document describes how you can provide a professional look to your reports by effectively adjusting the appearance of its elements.

This document consists of the following sections.
* [Appearance Properties](#properties)
* [Visual Styles](#styles)
* [Styles Priority](#priority)

<a name="properties"/>

## Appearance Properties
In the Report Designer, a report and each of its elements ([bands](../../report-elements/report-bands.md) and [controls](../../report-elements/report-controls.md)) has a complete set of appearance options (such as **Background Color**, **Borders**, **Font**, **Foreground Color**, **Text Alignment**, etc.). By default, these properties are not specified, meaning that their real values are obtained from a control's (or band's) _parent_, which is the report itself. So, the appearance specified for a report is distributed to all its child elements. Similarly, the appearance of a band is translated to the controls it contains.

![EUD_WpfReportDesigner_Appearance_1](../../../../../images/img123622.png)

In turn, a control's appearance can be adjusted independently from its parent.

![EUD_WpfReportDesigner_Appearance_2](../../../../../images/img123623.png)

<a name="styles"/>

## Visual Styles
In addition to the capability to specify appearance property values for every control and band, you can create comprehensive global _styles_ (which are stored in the report's _style sheet_), and then assign them to individual report elements.

Click the ellipsis button for the report's **Style Sheet** property to invoke the **Styles Editor**, which allows you to manage a report's style sheets, customize them, save them to a file and load from it.

![EUD_WpfReportDesigner_Appearance_3](../../../../../images/img123624.png)

You can also invoke the **Styles Editor** by right-clicking the report and selecting **Edit Style Sheet...** in the context menu.

![EUD_WpfReportDesigner_Appearance_3a](../../../../../images/img123876.png)

To assign a particular style to a control, invoke the drop-down list for its **Style** property. Then, select one of the styles stored in a report's sheet collection or click the plus button to create a new style sheet.

![EUD_WpfReportDesigner_Appearance_4](../../../../../images/img123625.png)

Note that if a style is assigned to a band, it is applied to all controls that the band contains.

You can also use the [Report Explorer](../../interface-elements/report-explorer.md) to access the style collection. Commands of the context menu allow you to add, edit, clone or delete a style.

![EUD_WpfReportDesigner_Appearance_5](../../../../../images/img123626.png)

<a name="priority"/>

## Styles Priority
A style defines the same appearance properties that are defined by a control's (or band's) appearance properties. When both styles and individual appearance settings are assigned to an element, you can control the priority of their options using an element's **Style Priority** property.

By default, most of the **Style Priority**'s options (**Use Background Color**, **Use Border Color**, etc.) are set to **Yes**. This means that if any style is assigned to a control, its properties will have a higher priority than the appearance properties of this element or its parent. You can assign a higher priority to an element's appearance property by disabling the corresponding **Use*** property.

The following image demonstrates how the **Style Priority** property works.

![EUD_WpfReportDesigner_StylePriority](../../../../../images/img124176.png)

The same principles are applied to the _odd-even styles_ feature, which allows you to alternate the appearance of consecutive data rows in your report. For details on this, refer to [Use Odd and Even Styles](use-odd-and-even-styles.md).

> [!NOTE]
> When [conditional formatting](conditionally-change-a-controls-appearance.md) is applied to an element, its appearance definition has the highest priority.