---
title: Add a Cross-Reference
---
This document describes how to add a _cross-reference_ to your report. A cross-reference is simply a link whose target is located within the current document, which allows you to establish easy navigation through a report. In this example, we place a link at the bottom of each group, leading to the beginning of the report.

To demonstrate this feature,  use a report with grouping similar to the one created in the following tutorial: [Grouping Data](../../../../../interface-elements-for-web/articles/report-designer/creating-reports/shaping-data/grouping-data.md).

To create a report with cross-references, do the following.
1. Select the [Report Controls](../../../../../interface-elements-for-web/articles/report-designer/report-elements/report-controls.md) in the [Report Header band](../../../../../interface-elements-for-web/articles/report-designer/report-elements/report-bands.md), and in the [Properties Panel](../../../../../interface-elements-for-web/articles/report-designer/interface-elements/properties-panel.md), expand the **Design** category and set the **Name** property to **reportTop**.
	
	![eud-cross-reference-0](../../../../images/Img119871.png)
2. To accompany the existing Group Header with the corresponding Footer, [add](../../../../../interface-elements-for-web/articles/report-designer/creating-reports/basic-operations/create-report-elements.md) a Group Footer band.
3. Then, drop a label onto the Group Footer band. As it will be the link, change its **Text** to **Top of Report**, and apply the desired formatting to it (e.g., the blue color and underlined text).
	
	Expand the **Navigation** section and set the **Navigation Target** property to **_self** and the **Navigation URL** property to **reportTop**.
	
	![eud-cross-reference-1](../../../../images/Img119872.png)

The report with cross-references is now ready. Switch your report to the [Preview](../../../../../interface-elements-for-web/articles/report-designer/document-preview.md) mode and view the result.

![RD_HowTo_CrossReference_3](../../../../images/Img8879.png)