---
title: Script Editor
author: Anna Gubareva
legacyId: 116221
---
# Script Editor
The **Script Editor** allows you to write code for specific event handlers in the [Report Designer](../../report-designer-for-wpf.md) to adjust the behavior of [report controls](../report-elements/report-controls.md), [bands](../report-elements/report-bands.md) or the report itself.

![WPFDesigner_ScriptEditor](../../../../images/img123181.png)

This topic describes the basics of using scripts, the Script Editor interface and shows how to use scripting in a report. The document consists of the following sections.
* [Scripting Overview](#overview)
* [Maintaining Scripts](#maintaining)

<a name="overview"/>

## Scripting Overview
The Script Editor provides you with the capability to write and execute scripts at runtime when a report is generated. Scripting is made available to extend the standard functionality as far as may be required.

The Script Editor supports **C#** and **Visual Basic .NET** scripting languages. This means that the scripting language is independent from the language used to create the report. You can specify the language using the **Script Language** property. The selected scripting language should be the same for all scripts used in a report.

![WPFDesigner_ScriptLanguageProperty](../../../../images/img123135.png)

<a name="maintaining"/>

## Maintaining Scripts
Each report element has its own set of events, which are individual for each element type. To handle an event of a report element, do one of the following.
* Select the required report element (e.g., on the [Design Surface](design-surface.md)). In the [Properties Panel](properties-panel.md), expand the **Scripts** property and click the plus button for the event.
	
	![WPFDesigner_AddingScriptViaPropertiesPanel](../../../../images/img123167.png)
* Click the **Scripts** button (![WPFDesigner_Toolbar_ScriptEditor](../../../../images/img120434.png)) in the [Toolbar](toolbar.md) to display the Script Editor. Choose the required report element in the dedicated drop-down list at the left top of the Script Editor. Then, select one of the available events in another list at the right top.
	
	![WPFDesigner_AddingScriptViaScriptEditor](../../../../images/img123168.png)

After the event is specified, a code template is automatically generated in the current scripting language and added in the Script Editor.

![WPFDesigner_ScriptTemplate](../../../../images/img123170.png)

To check for errors in the report's script, click the **Validate** button. The validation result is displayed in the errors panel at the bottom of the Script Editor. Double-click the error item in the panel's list to go to the corresponding line of code. If all scripts are valid, the errors panel is empty.

![WPFDesigner_ScriptErrorPanel](../../../../images/img123171.png)