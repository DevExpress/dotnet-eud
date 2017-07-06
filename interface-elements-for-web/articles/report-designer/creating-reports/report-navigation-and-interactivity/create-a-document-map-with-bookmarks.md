---
title: Create a Document Map with Bookmarks
---
# Create a Document Map with Bookmarks
This document describes the steps to create a report with _bookmarks_ (a so-called _Document Map_). This feature allows you to easily navigate through the report during [Print Preview](../../../../../interface-elements-for-web/articles/report-designer/document-preview.md).

To demonstrate the Document Map feature, use a report with grouping, similar the one created in the following tutorial: [Grouping Data](../../../../../interface-elements-for-web/articles/report-designer/creating-reports/shaping-data/grouping-data.md).

To create a report with bookmarks, do the following.
1. Select the [Label](../../../../../interface-elements-for-web/articles/report-designer/report-elements/report-controls.md) in the [Report Header band](../../../../../interface-elements-for-web/articles/report-designer/report-elements/report-bands.md), and in the [Properties Panel](../../../../../interface-elements-for-web/articles/report-designer/interface-elements/properties-panel.md), expand the **Navigation** category and set the **Bookmark** property to the same value as the Label's text (i.e., **Products by Categories**).
	
	![eud-add-bookmarks-0](../../../../images/Img119889.png)
2. Now, select the Label, which is placed in the report's Group Header band. As this control is bound to data, we will bind its **Bookmark** property to the same data field. To do this, in the **Data** category, expand the **Data Bindings** section and specify the **Bookmark** property.
	
	![eud-add-bookmarks-1](../../../../images/Img119890.png)
	
	Note that as with other bindable properties, you also can apply value formatting to the **Bookmark** property. To do this, set the **Format String** property to **Category {0}**.
3. To define the document map's hierarchy, expand the **Navigation** category and set the **Parent Bookmark** property to the Report Header's label.
	
	![eud-add-bookmarks-2](../../../../images/Img119891.png)

The report with bookmarks is now ready. Switch your report to the [Preview](../../../../../interface-elements-for-web/articles/report-designer/document-preview.md) mode and view the result.

![eud-add-bookmarks-3](../../../../images/Img119892.png)