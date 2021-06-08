---
title: Delta
author: Natalia Kazakova
legacyId: 118008
---
# Delta
Gauges allow you to display the difference between the _actual_ and _target_ values of a particular parameter. This difference is called **delta**.

Delta is shown with a _delta indicator_ (indicating whether the actual value is less than or greater than the target value) and _delta values_ (representing this difference as an absolute value or a variation).

![wdd-gauge-delta](../../../../images/img125316.png)

After you add the data item containing _actual_ data, you can add the second data item (optional) that contains _target_ data. To customize settings that relate to the calculation and display of deltas, open the **Delta Options** section of the [data item menu](../../ui-elements/data-item-menu.md).

![wdd-gauge-options](../../../../images/img125312.png)

Use it to define the conditions for displaying delta indication, specify which delta values should be displayed, and introduce the comparison tolerance.The following options are available.

| Option | Description |
|---|---|
| **Value Type** | Specifies which values should be displayed as the main delta value. Additional delta values are selected automatically. |
| **Result Indication** | Specifies the condition for displaying delta indication. |
| **Threshold Type** | Specifies the comparison tolerance in percentage values or in absolute values. |
| **Threshold Value** | Specifies the comparison tolerance value. |