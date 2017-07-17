---
title: Add Page Numbers for Groups
author: Eugeniy Burmistrov
legacyId: 7489
---
# Add Page Numbers for Groups
This tutorial demonstrates how to display page numbers individually, for each group in your report. To demonstrate this feature, we'll use a report, similar to the one created in the following tutorial: [Change or Apply Data Grouping to a Report](../../report-editing-basics/change-or-apply-data-grouping-to-a-report.md).

To add page numbers for groups, do the following.
1. From the [Toolbox](../../report-designer-reference/report-designer-ui/control-toolbox.md), drop the [Page Info](../../report-designer-reference/report-controls/page-info.md) control onto the [Group Footer](../../report-designer-reference/report-bands/grouping-bands.md).
	
	![RD_HowTo_GroupsPaging](../../../../../images/img11154.png)
2. Then, select the control, and set its **Running Band** to **GroupHeader1**.
	
	![RD_HowTo_GroupsPaging_0](../../../../../images/img11155.png)
	
	If required, you also can specify its **Format** property (e.g. **Page {0} of {1}**).
3. Now, you should force each new group to start on a separate page. Otherwise, group page numbers will be calculated incorrectly.
	
	To do this, select the Group Footer, and set its **Page Break** to **After the Band**.
	
	![RD_HowTo_GroupsPaging_2](../../../../../images/img11157.png)
4. Finally, select the Group Footer, and click its [Smart Tag](../../report-designer-reference/report-designer-ui/smart-tag.md). In its actions list, check the **Repeat Every Page** option.
	
	![RD_HowTo_GroupsPaging_1](../../../../../images/img11156.png)
	
	Then, you can do the same for the Group Header, as well.

The report is now ready. Switch to the [Preview Tab](../../report-designer-reference/report-designer-ui/preview-tab.md), and view the result.

![RD_HowTo_GroupsPaging_3](../../../../../images/img11158.png)