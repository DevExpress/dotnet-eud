---
title: Create a Table of Contents
author: Anna Gubareva
legacyId: 116343
---
# Create a Table of Contents
This tutorial describes how to create a report with a table of contents, which is automatically created based on the [bookmarks](add-bookmarks.md) existing in a report.

To insert a table of contents into a report, do the following.
1. Drop the [Table Of Contents](../../report-elements/report-controls.md) control from the [Toolbox](../../interface-elements/control-toolbox.md) onto the [Report Header Band](../../report-elements/report-bands.md).
	
	![EUD_WpfRD_Toc_0](../../../../../images/img125066.png)
	
	Alternatively, you can double-click the control in the Toolbox. In this case, if the report does not contain a Report Header, it will be created automatically, so that the table of contents can be added to it.
2. Double-click the title of the table of contents and specify its text.
	
	![EUD_WpfRD_Toc_1](../../../../../images/img125067.png)
3. To customize the title's appearance, use the **Level Title** option's settings available in the [Properties Panel](../../interface-elements/properties-panel.md).
	
	![EUD_WpfRD_Toc_2](../../../../../images/img125068.png)
4. To customize the appearance of all other levels, use the **Level Default** option's settings.
	
	![EUD_WpfRD_Toc_3](../../../../../images/img125069.png)
5. To customize a specific level individually, add a corresponding item to the **Levels** collection of the table of contents.
	
	![EUD_WpfRD_Toc_4](../../../../../images/img125070.png)
	
	After adding a new level, you can access and customize its properties.

The table of contents are now ready. Switch to the [Print Preview](../../document-preview.md) and view the result.

![EUD_WpfRD_Toc_5](../../../../../images/img125071.png)