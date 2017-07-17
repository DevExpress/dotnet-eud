---
title: Label Report
author: Anna Gubareva
legacyId: 116203
---
# Label Report
This tutorial describes the steps required to create a label report containing employee badges.

To accomplish this task, do the following.
1. Click the **New** button on the [Toolbar](../interface-elements/toolbar.md) or the plus button next to the report tab headers to [create a new report](../creating-reports/basic-operations/create-a-new-report.md).
2. The invoked [Report Wizard](../report-wizard.md) will guide you through the process of creating a label report. For detailed instructions on wizard steps, refer to [Label Report](../report-wizard/label-report.md).
3. After performing the above steps you will see that the report's Detail band is divided into three different areas. The first area at the left-hand side indicates the actual available band area for controls to be placed within it. The gray area at the right-hand side is intended for the columns in which labels will be displayed, so it cannot be occupied by controls. Finally, the white area specifies an indent between the available and reserved areas.
	
	![EUD_WpfReportDersigner_LabelReport_1](../../../../images/img123515.png)
4. [Bind a report to a data source](../creating-reports/providing-data/binding-a-report-to-data.md) containing information about employees.
5. Then, drop the required fields from the [Field List](../interface-elements/field-list.md) onto the available Detail band's area, and adjust the layout.
	
	![EUD_WpfReportDersigner_LabelReport_2](../../../../images/img123516.png)

The label report is now ready. Switch your report to the [Print Preview](../document-preview.md) tab and view the result.

![EUD_WpfReportDersigner_LabelReport_Result](../../../../images/img123517.png)