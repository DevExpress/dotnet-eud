---
title: Delta
author: Natalia Kazakova
legacyId: 16609
---
# Delta
The **Choropleth Map** allows you to indicate the difference between the _actual_ and _target_ values of a particular parameter. This difference is called **delta**.

![ChoroplethMap_DeltaSales](../../../../../images/img22211.png)

## Delta Options
To specify delta indication settings, click the **Options** button next to the data item container.

![ChoroplethMap_Delta_OptionsButton](../../../../../images/img22213.png)

This invokes the **Choropleth Map Options** dialog. When the map type is set to **Delta**, this dialog contains the following settings.

![ChoroplethMap_DeltaOptionsDialog](../../../../../images/img22214.png)
* **Value Type**
	
	You can specify which values to display within map tooltips. Use the **Value type** combo box to select the value that will be displayed as the delta value.
	
	| Value Type | Tooltip |
	|---|---|
	| **Actual value** | ![Map_DeltaValueType_ActualValue](../../../../../images/img22215.png) |
	| **Absolute variation** | ![Map_DeltaValueType_AbsoluteVariation](../../../../../images/img22216.png) |
	| **Percent variation** | ![Map_DeltaValueType_PercentVariation](../../../../../images/img22217.png) |
	| **Percent of target** | ![Map_DeltaValueType_PercentOfTarget](../../../../../images/img22218.png) |
* **Result Indication**
	
	You can specify the condition that will be used to select the indicator color. To do this, use the **Result indication** combo box.
	
	| Result Indication | Area Color |
	|---|---|
	| **Greater is good** | ![Map_DeltaResultIndicaion_GreaterIsGood_1](../../../../../images/img22221.png)![Map_DeltaResultIndicaion_GreaterIsGood_2](../../../../../images/img22222.png) |
	| **Less is good** | ![Map_DeltaResultIndicaion_LessIsGood_1](../../../../../images/img22223.png)![Map_DeltaResultIndicaion_LessIsGood_2](../../../../../images/img22224.png) |
	| **Warning if greater** | ![Map_DeltaResultIndicaion_WarningIfGreater_1](../../../../../images/img22225.png)![Map_DeltaResultIndicaion_WarningIfGreater_2](../../../../../images/img22226.png) |
	| **Warning if less** | ![Map_DeltaResultIndicaion_WarningIfLess_1](../../../../../images/img22227.png)![Map_DeltaResultIndicaion_WarningIfLess_2](../../../../../images/img22228.png) |
	| **No indication** | ![Map_DeltaResultIndicaion_WarningIfLess_1](../../../../../images/img22227.png)![Map_DeltaResultIndicaion_WarningIfGreater_2](../../../../../images/img22226.png) |
* **Threshold type** and **Threshold value**
	
	You can specify that a required indicator should only be displayed when the difference between the actual and target values exceeds a specified value. For instance, the actual value exceeds the target value by 10%, or by $2K.
	
	Use the **Threshold type** combo box to select whether you wish to specify the threshold in percentage values or in absolute values. Then use the **Threshold value** box to specify the threshold value.

The **Format** tab allows you to specify the numeric display formats for for different value types, as described in the [Formatting Data](../../../data-shaping/formatting-data.md) document.

![](../../../../../images/choroplethmap_deltaoptionsdialog_format.png)

The tab contains the following settings.

* **Format type** - Specifies format types for numeric values. 
* **Unit** - Specifies the unit to convert the numeric values.
* **Precision** - Specifies the number of fractional digits to display.
* **Currency** - Specifies the currency symbol and format provided by the current culture settings.
* **Culture** - Specifies the name of a culture that defines the currency symbol and format.
* **Include group separator** - Specifies whether separators should be inserted between digit groups.