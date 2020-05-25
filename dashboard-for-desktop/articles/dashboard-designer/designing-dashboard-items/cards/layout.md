---
title: Layout
author: Natalia Kazakova
legacyId: 118815
---
# Layout
The Card dashboard item allows you to manage the position and visibility of elements displayed on cards. These elements include actual and target values, a [delta indicator and corresponding delta values](delta.md), a [sparkline](sparkline.md), etc.

To manage the position and visibility of card elements, choose a predefined layout template and customize its settings.
* [Available Layout Templates](#available)
* [Default Layout](#default)
* [Change Layout](#change)

## <a name="available"/>Available Layout Templates
The table below contains information about the available layout templates:

| Layout Type | Example | Description |
|---|---|---|
| Stretched | ![Card_StretchedLayout](../../../../images/img128069.png) | The _Stretched_ layout template arranges card elements so that they occupy an entire card area. |
| Centered | ![Card_CompactLayout](../../../../images/img128070.png) | The _Centered_ layout template is used to center card elements so that they occupy a specified width/height. |
| Compact | ![Card_CompactLayoutTemplate](../../../../images/img128402.png) | The _Compact_ layout template is used to arrange card elements so that they occupy the minimum area. |
| Lightweight | ![Card_LightweightLayoutTemplate](../../../../images/img128403.png) | The _Lightweight_ layout template displays the minimum set of elements within a card. |

For all layout types, you can change the visibility of its elements, or you can specify the display value type for data-bound elements. To learn more, see the [Change Layout](#change) paragraph below.

## <a name="default"/>Default Layout
The Card dashboard item uses the [Stretched](#available) layout template that arranges card visual elements in the following way by default:

![Card_StretchedLayout_VisualElements](../../../../images/img128175.png)

To learn more about the available value types and visual elements, see [Change Layout](#change).

> [!NOTE]
> **Delta Indicator** and delta values (such as **Percent Variation** or **Absolute Variation**) are colored depending on delta settings. To learn how to manage delta settings, see [Delta](delta.md).

## <a name="change"/>Change Layout
To change a card's layout in the Dashboard Designer, click the Options button (the ![DataItemsArea_OptionsButton](../../../../images/img20167.png) icon) displayed next to the data item container in the **[Cards](providing-data.md)** section.

![Cards_DeltaOptions_OptionsButton](../../../../images/img19985.png)

This invokes the **Card Settings** dialog.

![CardSettings_LayoutOptionsTab](../../../../images/img128293.png)

On the **Layout Options** tab, select the required layout type in the **Select template** list and specify its settings:
* **Min width** - Specifies the minimum width of the card content.
* **Max width** - Specifies the maximum width of the card content. Use the **Auto** option to determine the maximum width automatically.

You can show/hide the following values and visual elements within the card:

| Value | Description | Example |
|---|---|---|
| **Title** | Displays values of the last (bottommost) dimension placed in the **[Series](providing-data.md)** section. | _Microsoft Office Keyboard_ |
| **Subtitle** | Displays combined values of all dimensions except the last (bottommost) dimension. | _Technology - Computer Peripherals_ |
| **Absolute Variation** | An absolute difference between the actual and target value (see [Delta](delta.md)). | _+18.1K_ |
| **Actual Value** | A summary value for a measure placed in the **[Actual](providing-data.md)** placeholder. | _$392K_ |
| **Card Name** | A card name. | _Revenue vs. Target_ |
| **Percent of Target** | A percent of a target value (see [Delta](delta.md)). | _104.85 %_ |
| **Percent Variation** | A percent difference between the actual and target value (see [Delta](delta.md)). | _4.85 %_ |
| **Target Value** | A summary value for a measure placed in the **[Target](providing-data.md)** placeholder. | _$374K_ |
| **Dimension {Name}** | Allows you to display values of a specific dimension placed in the **[Series](providing-data.md)** section. | _Technology_ |
| Element | Description | Example |
| **Delta Indicator** | Indicates whether the actual value is less or greater than the target value (see [Delta](delta.md)). | ![Card_DeltaIndicatorExample](../../../../images/img128298.png) |
| **Sparkline** | Visualizes the variation of actual or target values. To learn more, see [Sparkline](sparkline.md). | ![Card_SparklineExample](../../../../images/img128299.png) |

Use the **Apply to All Cards** button to propagate the specified layout settings to all cards corresponding to **[Actual-Target](providing-data.md)** pairs. The **Reset** button resets all setting to their default values.