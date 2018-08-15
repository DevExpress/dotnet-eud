---
title: Lay out Dynamic Report Content
author: Anna Gubareva
---
# Lay out Dynamic Report Content

You can use Print Preview to see what the resulting document looks like because data-aware controls' contents are not available at design time. This document describes how to maintain report elements' correct location in a published document.


## <a name="pagebreaks"></a>Maintain Page Breaks
Use the [Page Break](use-report-elements/use-basic-report-controls/page-break.md) control to insert a page break at the required location in a report.

image

You can use the band's **Page Break** property to add a page break before or after printing a specific band.

image

The following bands support this feature:

* detail band
* detail report band
* report header and footer
* group headers and footers

## <a name="bandslocation"></a>Maintain the Band Location on a Page
Use the Group and Report Footer's **Print At Bottom** properties to choose whether these bands should appear at the bottom of a page or immediately after the previous band.

image

| **Print At Bottom = No** | **Print At Bottom = Yes** |
|---|---|
| image | image |


Use the Page Header and Footer's **Print On** property to avoid printing these bands on the same page with a Report Header and/or Footer.

image

* **Print On = All Pages**

    image

* **Print On = Not With Report Header**

    image

Use the Group Header and Footer's **RepeatEveryPage** property to repeat these bands on every page.

image

* **Repeat Every Page = No**

    image

* **Repeat Every Page = Yes**

    image

## <a name="keeptogether"></a>Keep Content Together
You can choose whether a control's content can be split across several pages using its **Keep Together** property.

image

| **Keep Together = No** | **Keep Together = Yes** |
|---|---|
| image | image |

Enabling this property for a single control makes the same band's controls behave like this option is enabled.

Use the ban's **Keep Together** property to enable this feature for all controls within a specific band.

> [!NOTE]
> This feature is not available for the [Chart](use-report-elements/use-charts-and-pivot-grids/use-charts-in-reports.md), [Sparkline](use-report-elements/use-gauges-and-sparklines/add-sparklines-to-a-report.md) and [Subreport](use-report-elements/use-basic-report-controls/subreport.md) controls.

In a master-detail report, you can print the detail band on the same page as the detail report band using the detail band's **Keep Together With Detail Reports** property.

## <a name="maintainsize"></a>Maintain the Size and Content of Data-Bound Controls
Use the control's **Can Grow** and **Can Shrink** properties to make a data-bound control automatically adjust its height to its contents.

image

| **Can Grow = No** | **Can Grow = Yes** |
|---|---|
| image | image |

| **Can Shrink = No** | **Can Shrink = Yes** |
|---|---|
| image | image |

> [!NOTE]
> This feature does not work with [anchoring](#anchoring) enabled, as well as for labels that are used to display [summary function results](shape-report-data/shape-data-expression-bindings/calculate-a-summary.md).

Use the **Auto Width** property to make a data-bound [Label](use-report-elements/use-basic-report-controls/label.md) or [Character Comb](use-report-elements/use-basic-report-controls/character-comb.md) automatically adjust its width to its content. This option behavior depends on the control's current horizontal alignment (**Text Alignment** property value).

image

* **TextAlignment = left**

    image

* **TextAlignment = right**

    image

* **TextAlignment = center**

    image

The control's **Word Wrap** property allows you to make a control display its contents in multiple lines when it does not fit into the control's dimensions.

| Auto Width = No, Word Wrap = No | Auto Width = No, Word Wrap = Yes |
|---|---|
| image | image |

| Auto Width = Yes, Word Wrap = No | Auto Width = Yes, Word Wrap = Yes |
|---|---|
| image | image |


You can also use the opposite **Text Fit Mode** property to adjust an label or table cell's font size to fit the control's bounds.

| TextFitMode = None | TextFitMode = GrowOnly | TextFitMode = ShrinkOnly | TextFitMode = ShrinkAndGrow |
|---|---|---|---|
| image | image | image | image |

This property is not available in the following cases:

* The **Can Grow**, **Can Shrink** or **Auto Width** option is enabled;
* The label's **Angle** property is specified;
* The control's **Anchor Horizontal** or **Anchor Vertical** property is set to **Both**.

## <a name="anchoring"></a>Anchor Controls
You can anchor a control to the top, bottom, or both edges of its parent container using the **Anchor Horizontal** and **Anchor Vertical** properties.

* **AnchorHorizontal = None**

    image

*  **AnchorHorizontal = Right**

    image

* **AnchorHorizontal = Both**

    image

## <a name="suppressing"></a>Suppress Controls
### Avoid Duplicated and Empty Values

When identical or null values appear in a report's data source, you can suppress these values in a report using the following properties:

* **Process Duplicates Mode**
	
	Specifies how to process report controls with identical values (leave them as is, merge, suppress, or suppress and shrink).

* **Process Null Values**
	
	Specifies how to process report controls receiving null values from a data source (leave them as is, suppress, or suppress and shrink).

* **Process Duplicates Target**
	
	Specifies whether to process duplicate the control's **Text** or **Tag** property values.

image

These properties are available for the following controls:

* [Bar Code]use-report-elements/use-basic-report-controls/bar-code.md)
* [Label](use-report-elements/use-basic-report-controls/label.md)
* [Character Comb](use-report-elements/use-basic-report-controls/character-comb.md)
* [Rich Text](use-report-elements/use-basic-report-controls/rich-text.md)
* [Table Cell](use-report-elements/use-tables.md)
* [Picture Box](use-report-elements/use-basic-report-controls/picture-box.md)

### Conditionally Suppress a Control

You can suppress a control when a specified logical condition is met by specifying the required **Visible** property expressions as described in the [Conditionally Suppress Controls](shape-report-data/shape-data-expression-bindings/conditionally-supress-controls.md) topic.

In this case, a space remains in the band at the control's location. You can avoid this by placing these controls onto an [Panel](use-report-elements/use-basic-report-controls/panel.md) and setting its **Can Shrink** property to **true**.

image

For this feature to work correctly, consider the following:

* Specify the **Visible** property's expression to the controls in the panel (and not to the panel itself).
* Do not assign borders to the panel container. Otherwise, they are printed when the panel's content is suppressed.