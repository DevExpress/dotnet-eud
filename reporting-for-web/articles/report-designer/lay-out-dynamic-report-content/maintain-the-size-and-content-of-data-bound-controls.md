---
title: Maintain the Size and Content of Data-Bound Controls
author: Anna Vekhina
---
# Maintain the Size and Content of Data-Bound Controls

Use the control's **Can Grow** and **Can Shrink** properties to make a data-bound control automatically adjust its height to its contents.

![](../../../images/eurd-web-can-grow-can-shrink-properties.png)

| **Can Grow = No** | **Can Grow = Yes** |
|---|---|
| ![](../../../images/eurd-web-can-grow-false.png) | ![](../../../images/eurd-web-can-grow-true.png) |

| **Can Shrink = No** | **Can Shrink = Yes** |
|---|---|
| ![](../../../images/eurd-web-can-shrink-false.png) | ![](../../../images/eurd-web-can-shrink-true.png) |

> [!NOTE]
> This feature does not work with [anchoring](anchor-controls.md) enabled, as well as for labels that are used to display [summary function results](../shape-report-data/calculate-summaries/calculate-a-summary.md).

Use the **Auto Width** property to make a data-bound [Label](../use-report-elements/use-basic-report-controls/label.md) or [Character Comb](../use-report-elements/use-basic-report-controls/character-comb.md) automatically adjust its width to its content. This option behavior depends on the control's current horizontal alignment (**Text Alignment** property value).

* **Text Alignment = Left**

    ![](../../../images/eurd-web-label-auto-width-left-align.png)

* **Text Alignment = Right**

    ![](../../../images/eurd-web-label-auto-width-right-align.png)

* **Text Alignment = Center**

    ![](../../../images/eurd-web-label-auto-width-center-align.png)

The control's **Word Wrap** property allows you to make a control display its contents in multiple lines when it does not fit into the control's dimensions.

| Auto Width = No, Word Wrap = No | Auto Width = No, Word Wrap = Yes |
|---|---|
| ![](../../../images/eurd-web-auto-width-false-word-wrap-false.png) | ![](../../../images/eurd-web-auto-width-false-word-wrap-true.png) |

| Auto Width = Yes, Word Wrap = No | Auto Width = Yes, Word Wrap = Yes |
|---|---|
| ![](../../../images/eurd-web-auto-width-true-word-wrap-false.png) | ![](../../../images/eurd-web-auto-width-false-word-wrap-true.png) |


You can also use the opposite **Text Fit Mode** property to adjust a label or table cell's font size to fit the control's bounds. Images below show how the **Text Fit Mode** property affects the label's font size.

![](../../../images/eurd-web-label-text-fit-mode-property.png) 

| Text Fit Mode = None | Text Fit Mode = Grow Only | Text Fit Mode = Shrink Only | Text Fit Mode = Shrink And Grow |
|---|---|---|---|
| ![](../../../images/eurd-web-label-text-fit-mode-none.png) | ![](../../../images/eurd-web-label-text-fit-mode-grow-only.png) | ![](../../../images/eurd-web-label-text-fit-mode-shrink-only.png) | ![](../../../images/eurd-web-label-text-fit-mode-shrink-and-grow.png) |

This property is not available in the following cases:

* The **Can Grow**, **Can Shrink** or **Auto Width** option is enabled;
* The label's **Angle** property is specified;
* The control's **Anchor Horizontally** or **Anchor Vertically** property is set to **Both**.