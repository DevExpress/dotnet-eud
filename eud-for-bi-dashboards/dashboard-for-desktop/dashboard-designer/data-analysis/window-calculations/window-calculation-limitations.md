---
title: Window Calculation Limitations
author: Natalia Kazakova
legacyId: 116582
---
# Window Calculation Limitations
## Supported Dashboard Items
Window calculations can be applied to measures of the following dashboard items.
* [Chart](../../dashboard-item-settings/chart.md)
* [Grid](../../dashboard-item-settings/grid.md)
* [Pies](../../dashboard-item-settings/pies.md)
* [Cards](../../dashboard-item-settings/cards.md)
* [Gauges](../../dashboard-item-settings/gauges.md)
* [Pivot](../../dashboard-item-settings/pivot.md)
* [Range Filter](../../dashboard-item-settings/range-filter.md)

## Data Shaping Limitations
The use of calculations imposes the following limitations related to [data shaping](../../data-shaping.md) features.
* [Sorting by measure](../../data-shaping/sorting.md) cannot be applied if the target measure has a calculation applied.
* [Top N](../../data-shaping/top-n.md) cannot be applied if its target measure has a calculation.