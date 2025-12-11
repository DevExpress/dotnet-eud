---
title: Grouping Data
author: Anna Gubareva
legacyId: 116280
---
# Grouping Data
This document demonstrates how to group report data. Grouping allows you to split data into groups based on identical values in a field or fields. Note that data grouping can be performed only if a report is [bound to a data source](../providing-data/binding-a-report-to-data.md).

To group records in a report, do the following.
1. [Create a new report](../basic-operations/create-a-new-report.md) and [bind it to a data source](../providing-data/binding-a-report-to-data.md). This tutorial starts with the following report.
	
	![EUD_WpfReportDersigner_Grouping_InitialReport](../../../../../images/img123495.png)
2. Next, switch to the [Group and Sort Panel](../../interface-elements/group-and-sort-panel.md), and click **Add a Group**. In the invoked drop-down list, select a data member across which the report is to be grouped.
	
	![EUD_WpfReportDersigner_Grouping_1](../../../../../images/img123496.png)
3. After this, the [Group Header](../../report-elements/report-bands.md) band is added to the report with the specified data member set as its grouping criterion.
	
	Drop the data field, which is specified as the grouping criterion, from the [Field List](../../interface-elements/field-list.md) panel onto the Group Header band. This data field will be displayed as a header for each group.
	
	![EUD_WpfReportDersigner_Grouping_2](../../../../../images/img123497.png)
4. In addition, you can enable the corresponding Group Footer band by enabling the **Show Footer** option in the Group and Sort Panel.
	
	![EUD_WpfReportDersigner_Grouping_3](../../../../../images/img123498.png)
	
	Use the **Sort Order** drop-down list to manage the sorting order of the group's items (ascending or descending) or to disable sorting in grouped data. If multiple groups are created, you can specify the priority for each group by selecting it in the Group and Sort Panel and using the **Move Up** and **Move Down** buttons.
5. Then, you can [calculate a total](calculating-summaries.md) across the group by placing a [Label](../../report-elements/report-controls.md) onto the Group Footer band and specifying its **Summary** properties in the following way.
	
	![EUD_WpfReportDersigner_Grouping_4](../../../../../images/img123499.png)
	
	Note also that value formatting is applied to a summary independently of the [general formatting](formatting-data.md), and has a greater priority.

The report is now ready. Switch to the [Print Preview](../../document-preview.md) tab and view the result.

![EUD_WpfReportDersigner_Grouping_Result](../../../../../images/img123500.png)