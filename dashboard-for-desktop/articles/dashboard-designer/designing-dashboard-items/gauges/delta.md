---
title: Delta
author: Natalia Kazakova
legacyId: 16595
---
# Delta
Gauges allow you to display the difference between the _actual_ and _target_ values of a particular parameter. This difference is called **delta**.

Delta is shown with a _delta indicator_ (indicating whether the actual value is less than or greater than the target value) and _delta values_ (representing this difference as an absolute value or a variation).

![Delta_Gauge](../../../../images/img20029.png)

To customize settings that relate to the calculation and display of deltas, use the options buttons (the ![DataItemsArea_OptionsButton](../../../../images/img20167.png) icon) displayed next to the data item container in the Gauges section of the DATA ITEMS pane.

![Gauges_DeltaOptions_OptionsButton](../../../../images/img19991.png)

These buttons invoke the **Gauge Options** dialog.

![Gauges_DeltaOptions_OptionsWindow](../../../../images/img19992.png)

Use it to define the condition for displaying delta indication, specify which delta values should be displayed, and introduce the comparison tolerance.
* [Delta Values](#deltavalues)
* [Delta Indication](#deltaindicationcondition)
* [Comparison Tolerance](#comparisontolerance)

## <a name="deltavalues"/>Delta Values
You can specify which values should be displayed within gauges. Use the **Value type** combo box in the **Gauge Options** window to select the value that will be displayed as the delta value.

| Value Type | Result |
|---|---|
| Actual Value | ![Gauges_Delta_Values_ActualValue](../../../../images/img20094.png) |
| Absolute Variation | ![Gauges_Delta_Values_AbsoluteVariation](../../../../images/img20093.png) |
| Percentage Variation | ![Gauges_Delta_Values_PercentVariation](../../../../images/img20096.png) |
| Percentage of Target | ![Gauges_Delta_Values_PercentOfTarget](../../../../images/img20095.png) |

## <a name="deltaindicationcondition"/>Delta Indication
You can specify the condition for displaying delta indication. To do this, use the **Result indication** combo box in the **Gauge Options** window.
* Greater is Good - The 'good' indication is displayed if the actual value exceeds the target value; if the target value exceeds the actual value, the 'bad' indication is displayed. 
	
	![Gauges_Delta_Indication_GreaterIsGood](../../../../images/img20088.png)
* Less is Good - The 'bad' indication is displayed if the actual value exceeds the target value; if the target value exceeds the actual value, the 'good' indication is displayed. 
	
	![Gauges_Delta_Indication_LessIsGood](../../../../images/img20089.png)
* No Indication - Indication is not displayed. 
	
	![Gauges_Delta_Indication_NoIndication](../../../../images/img20090.png)
* Warning if Greater - A warning is displayed if the actual value exceeds the target value; otherwise, no indication is displayed. 
	
	![Gauges_Delta_Indication_WarningIfGreater](../../../../images/img20091.png)
* Warning if Less - A warning is displayed if the target value exceeds the actual value; otherwise, no indication is displayed. 
	
	![Gauges_Delta_Indication_WarningIfLess](../../../../images/img20092.png)

## <a name="comparisontolerance"/>Comparison Tolerance
The comparison tolerance allows you to create more advanced conditions for displaying delta indication. For instance, you can specify that a specific indication should be displayed when the actual value exceeds the target value _by 10%_ or _by $2K_.

Use the **Threshold type** combo box to select whether you wish to specify the comparison tolerance in percentage values or in absolute values. Then use the **Threshold value** box to specify the comparison tolerance.