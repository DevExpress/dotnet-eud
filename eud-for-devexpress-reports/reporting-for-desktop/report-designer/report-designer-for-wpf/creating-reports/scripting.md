---
title: Scripting
author: Anna Gubareva
legacyId: 116357
---
# Scripting
This document describes the basic principles of _scripting_, which can be performed by handling the events of a report, and its [bands](../report-elements/report-bands.md) and [controls](../report-elements/report-controls.md).

This documents consists of the following sections.
- [Scripting](#scripting)
  - [Scripting Overview](#scripting-overview)
  - [Maintaining Scripts](#maintaining-scripts)

<a name="overview"/>

## Scripting Overview
_Scripts_ are program commands, placed within the _event handlers_ of the required report elements. And when the corresponding event occurs (e.g., a mouse click), the script code runs. Scripting is made available to extend the standard functionality as far as may be required.

You can write _scripts_ for a report or any of its elements (bands and controls) to be executed when the report is being [previewed, printed or exported](../document-preview.md).

The Report Designer allows you to write scripts using the [Script Editor](../interface-elements/script-editor.md). This editor supports **C#** and **Visual Basic .NET** scripting languages. This means that the scripting language is independent from the language used to create the report. The language is specified by the **Script Language** property of a report. The selected scripting language must be the same for all scripts used in a report.

![WPFDesigner_ScriptLanguageProperty](../../../images/img123135.png)

<a name="maintain"/>

## Maintaining Scripts
Each report element has its own set of events, which are individual for each element type. To handle an event of a report element, do one of the following.
* Select the required report element (e.g., on the [Design Surface](../interface-elements/design-surface.md)). In the [Properties Panel](../interface-elements/properties-panel.md), expand the **Scripts** property and click the plus button for the event.
	
	![WPFDesigner_AddingScriptViaPropertiesPanel](../../../images/img123167.png)
* Click the **Scripts** button (![WPFDesigner_Toolbar_ScriptEditor](../../../images/img120434.png)) in the [Toolbar](../interface-elements/toolbar.md) to display the Script Editor. Choose the required report element in the dedicated drop-down list at the left top of the Script Editor. Then, select one of the available events in another list at the right top.
	
	![WPFDesigner_AddingScriptViaScriptEditor](../../../images/img123168.png)

After the event is specified, a code template is automatically generated in the current scripting language and added in the Script Editor.

![WPFDesigner_ScriptTemplate](../../../images/img123170.png)

To check for errors in the report's script, click the **Validate** button. The validation result is displayed in the errors panel at the bottom of the Script Editor. Double-click the error item in the panel's list to go to the corresponding line of code. If all scripts are valid, the errors panel is empty.

![WPFDesigner_ScriptErrorPanel](../../../images/img123171.png)
