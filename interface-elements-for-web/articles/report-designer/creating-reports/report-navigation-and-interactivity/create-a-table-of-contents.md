---
title: Create a Table of Contents
---
# Create a Table of Contents
This topic describes how to provide a report with a table of contents that displays page numbers for bookmarked report elements at different nesting levels, and thus makes it possible to quickly navigate to a specific document page by clicking the corresponding entry.

To demonstrate this feature, use a report with specified bookmarks similar to the one created in the following tutorial: [Create a Document Map with Bookmarks](../../../../../interface-elements-for-web/articles/report-designer/creating-reports/report-navigation-and-interactivity/create-a-document-map-with-bookmarks.md).

To create a table of contents in a report, do the following.
1. Drop the [Table of Contents](../../../../../interface-elements-for-web/articles/report-designer/report-elements/report-controls.md) control from the [Toolbox](../../../../../interface-elements-for-web/articles/report-designer/interface-elements/toolbox.md) onto the [Report Header Band](../../../../../interface-elements-for-web/articles/report-designer/report-elements/report-bands.md). If the report does not contain this band, it will be created automatically.
	
	![EUD_WebDesigner_ToC1](../../../../images/Img123367.png)
2. Double-click the title of the table of contents and specify its text.
	
	![EUD_WebDesigner_ToC2](../../../../images/Img123368.png)
3. To customize title appearance, switch to the [Properties Panel](../../../../../interface-elements-for-web/articles/report-designer/interface-elements/properties-panel.md), expand the **Behavior** category and use the **Level Title** option's settings.
	
	![EUD_WebDesigner_ToC3.](../../../../images/Img123369.png)
4. To customize the appearance of all other levels, use the **Level Default** option's settings in the **Behavior** category.
	
	![EUD_WebDesigner_ToC4](../../../../images/Img123370.png)
5. To customize a specific level individually, add a corresponding item to the **Levels** collection of the table of contents. After adding a new level, you can access and customize its properties.
	
	![EUD_WebDesigner_ToC5](../../../../images/Img123371.png)

The table of contents is now ready. Switch your report to the [Preview](../../../../../interface-elements-for-web/articles/report-designer/document-preview.md) mode and view the result.

![EUD_WebDesigner_ToC_Result](../../../../images/Img123372.png)