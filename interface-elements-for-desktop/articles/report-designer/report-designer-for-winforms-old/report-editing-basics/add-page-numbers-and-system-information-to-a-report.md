---
title: Add Page Numbers and System Information to a Report
author: Eugeniy Burmistrov
legacyId: 5586
---
# Add Page Numbers and System Information to a Report
This document describes how to insert _page numbers_ or other system information (e.g. _current date and time_, _user name_, etc.) into a report.

Generally, this information is displayed within the [Page Header and Footer](../report-designer-reference/report-bands/page-header-and-footer.md) or [Page Margin](../report-designer-reference/report-bands/page-margin-bands.md) bands. To add page numbers or system information to a report, locate the [Control Toolbox](../report-designer-reference/report-designer-ui/control-toolbox.md) and drag and drop the [Page Info](../report-designer-reference/report-controls/page-info.md) control.

![RD_HowTo_InsertUserName_0](../../../../images/img8518.png)

Then, follow the instructions below for your specific task.
* [Add Page Numbers](#pagenumbers)
* [Add System Date and Time](#datetime)
* [Add the User Name](#username)

## <a name="pagenumbers"/>Add Page Numbers
1. Select the **Page Info** control, click its [Smart Tag](../report-designer-reference/report-designer-ui/smart-tag.md), and in the invoked actions list, expand the drop-down list for the **Page Information** entry.
	
	![RD_HowTo_InsertPageNumber_0](../../../../images/img8535.png)
	
	Select whether to display only the page number (Latin or Roman - uppercase or lowercase), or the current page number with total pages.
2. To [format](change-value-formatting-of-report-elements.md) the control's text, via its Smart Tag, invoked its actions list, and specify the required format (e.g. **Page {0} of {1}**).
	
	![RD_HowTo_InsertPageNumber_1](../../../../images/img8536.png)
3. Using the control's actions list, you also can specify the _starting page number_, and the _running band_ (e.g. this option is available when there are [groups](change-or-apply-data-grouping-to-a-report.md) in a report, and it's required to apply independent page numbering for them). For details on this, refer to [Add Page Numbers for Groups](../create-reports/miscellaneous/add-page-numbers-for-groups.md).

The result is shown below.

![RD_HowTo_InsertPageNumber_2](../../../../images/img8537.png)

## <a name="datetime"/>Add System Date and Time
1. Select the **Page Info** control, click its [Smart Tag](../report-designer-reference/report-designer-ui/smart-tag.md), and in the invoked actions list, expand the drop-down list for the **Page Information** entry, and select **Current Date and Time**.
	
	![RD_HowTo_InsertDateTime_0](../../../../images/img8522.png)
2. To [format](change-value-formatting-of-report-elements.md) the control's text, via its Smart Tag, invoked its actions list, and specify the required format. You can either type it in the **Format** field, or, click its ellipsis button and use the **Format String Editor**.
	
	![RD_HowTo_InsertDateTime_2](../../../../images/img8524.png)

The result is shown below.

![RD_HowTo_InsertDateTime_1](../../../../images/img8523.png)

## <a name="username"/>Add the User Name
1. Select the **Page Info** control, click its [Smart Tag](../report-designer-reference/report-designer-ui/smart-tag.md), and in the invoked actions list, expand the drop-down list for the **Page Information** entry, and select **User Name**.
	
	![RD_HowTo_InsertUserName_1](../../../../images/img8519.png)
2. To [format](change-value-formatting-of-report-elements.md) the control's text, via its Smart Tag, invoke its actions list, and specify the required format (e.g. **Current User: {0}**).
	
	![RD_HowTo_InsertUserName_2](../../../../images/img8520.png)

The result is shown below.

![RD_HowTo_InsertUserName_3](../../../../images/img8521.png)