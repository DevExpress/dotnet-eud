---
title: Add Page Numbers and System Information to a Report
---
# Add Page Numbers and System Information to a Report
This document describes how to insert _page numbers_ or other system information (e.g., _current date and time_, _user name_, etc.) into a report, using the [Web Report Designer](../../../report-designer.md).

Generally, this auxiliary information is displayed within the Page Header and Footer or Page Margin [bands](../../report-elements/report-bands.md). To add page numbers or system information to your report, drop the [Page Info](../../report-elements/report-controls.md) control from the [Toolbox](../../interface-elements/toolbox.md) onto a band.

![eud-page-numbers-0](../../../../images/img119942.png)

Then, follow the instructions below for your specific task.
* [Add Page Numbers](#pagenumbers)
* [Add System Date and Time](#datetime)
* [Add the User Name](#username)

## <a name="pagenumbers"/>Add Page Numbers
1. Select the **Page Info** control, switch to the [Properties Panel](../../interface-elements/properties-panel.md), expand the **Actions** or **Behavior** category and specify the **Page Information** property.
	
	![eud-page-numbers-1](../../../../images/img119943.png)
	
	You can choose one of the following formats for displaying page numbers:
	* **Number** (displays the current page number only);
	* **NumberOfTotal** (displays the current page number with total pages);
	* **RomLowNumber** (the current page number is written in lowercase Roman letters);
	* **RomHiNumber** (the current page number is written in uppercase Roman letters);
	* **Total** (displays the total number of pages).
2. To format the control's text, specify the **Format** property (e.g., **Page {0} of {1}**). You can also specify the _starting page number_.
	
	![eud-page-numbers-4](../../../../images/img119946.png)

Your report with page numbers is now ready. Switch it to the [Preview](../../document-preview.md) mode to view the result.

![eud-page-numbers-5](../../../../images/img119947.png)

## <a name="datetime"/>Add System Date and Time
Select the **Page Info** control, and in the [Properties Panel](../../interface-elements/properties-panel.md), expand the **Actions** or **Behavior** category. Then, expand the drop-down list for the **Page Information** property and select **DateTime**.

![eud-page-numbers-2](../../../../images/img119944.png)

To format the control's text, click the ellipsis button for the **Format** property, and in the invoked [Format String Editor](../../interface-elements/format-string-editor.md), specify a date and time format string (e.g., **dddd, MMMM dd, yyyy**).

![eud-page-numbers-8](../../../../images/img119951.png)

Switch your report to the [Preview](../../document-preview.md) mode to view the result.

![eud-page-numbers-6](../../../../images/img119948.png)

## <a name="username"/>Add the User Name
Select the **Page Info** control, and in the [Properties Panel](../../interface-elements/properties-panel.md), expand the **Actions** or **Behavior** category. Expand the drop-down list for the **Page Information** property and select **UserName**.

![eud-page-numbers-3](../../../../images/img119945.png)

To format the control's text, specify the **Format** property (e.g., **Current User: {0}**).

![eud-page-numbers-9](../../../../images/img119952.png)

Switch your report to the [Preview](../../document-preview.md) mode to view the result.

![eud-page-numbers-7](../../../../images/img119950.png)