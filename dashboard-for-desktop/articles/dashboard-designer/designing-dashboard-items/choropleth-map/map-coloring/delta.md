---
title: Delta
---
# Delta
The **Choropleth Map** allows you to indicate the difference between the _actual_ and _target_ values of a particular parameter. This difference is called **delta**.

![ChoroplethMap_DeltaSales](../../../../../images/Img22211.png)

## Delta Options
To specify delta indication settings, click the **Options** button next to the data item container.

![ChoroplethMap_Delta_OptionsButton](../../../../../images/Img22213.png)

This invokes the **Choropleth Map Options** dialog. When the map type is set to **Delta**, this dialog contains the following settings.

![ChoroplethMap_DeltaOptionsDialog](../../../../../images/Img22214.png)
* **Value Type**
	
	You can specify which values to display within map tooltips. Use the **Value type** combo box to select the value that will be displayed as the delta value.
	
	| Value Type | Tooltip |
	|---|---|
	| **Actual value** | ![Map_DeltaValueType_ActualValue](../../../../../images/Img22215.png) |
	| **Absolute variation** | ![Map_DeltaValueType_AbsoluteVariation](../../../../../images/Img22216.png) |
	| **Percent variation** | ![Map_DeltaValueType_PercentVariation](../../../../../images/Img22217.png) |
	| **Percent of target** | ![Map_DeltaValueType_PercentOfTarget](../../../../../images/Img22218.png) |
* **Result Indication**
	
	You can specify the condition that will be used to select the indicator color. To do this, use the **Result indication** combo box.
	
	| Result Indication | Area Color |
	|---|---|
	| **Greater is good** | ![Map_DeltaResultIndicaion_GreaterIsGood_1](../../../../../images/Img22221.png)![Map_DeltaResultIndicaion_GreaterIsGood_2](../../../../../images/Img22222.png) |
	| **Less is good** | ![Map_DeltaResultIndicaion_LessIsGood_1](../../../../../images/Img22223.png)![Map_DeltaResultIndicaion_LessIsGood_2](../../../../../images/Img22224.png) |
	| **Warning if greater** | ![Map_DeltaResultIndicaion_WarningIfGreater_1](../../../../../images/Img22225.png)![Map_DeltaResultIndicaion_WarningIfGreater_2](../../../../../images/Img22226.png) |
	| **Warning if less** | ![Map_DeltaResultIndicaion_WarningIfLess_1](../../../../../images/Img22227.png)![Map_DeltaResultIndicaion_WarningIfLess_2](../../../../../images/Img22228.png) |
	| **No indication** | ![Map_DeltaResultIndicaion_WarningIfLess_1](../../../../../images/Img22227.png)![Map_DeltaResultIndicaion_WarningIfGreater_2](../../../../../images/Img22226.png) |
* **Threshold type** and **Threshold value**
	
	You can specify that a required indicator should only be displayed when the difference between the actual and target values exceeds a specified value. For instance, the actual value exceeds the target value by 10%, or by $2K.
	
	Use the **Threshold type** combo box to select whether you wish to specify the threshold in percentage values or in absolute values. Then use the **Threshold value** box to specify the threshold value.