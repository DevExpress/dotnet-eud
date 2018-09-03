---
title: Display the User Name in a Report
---
# Display the User Name in a Report

This tutorial demonstrates how to insert the current user name in a report using the [PageInfo](..\use-report-elements\use-basic-report-controls\page-info.md) control.

![eurd-win-insert-username-result](../../../../images/eurd-win-insert-username-result.png)

Do the following to insert the user name into a report:

1. Typically, the user name is displayed within the [Report Header](..\introduction-to-banded-reports.md) band. To add it to the report, right click anywhere on the report's surface. In the invoked menu, point to **Insert Band** and click **ReportHeader**.
	
	![eurd-win-insert-datetime-add-reportheader-band](../../../../images/eurd-win-insert-datetime-add-reportheader-band.png)
2. Drop the [PageInfo](..\use-report-elements\use-basic-report-controls\page-info.md) control from the [Toolbox](..\report-designer-tools\toolbox.md) onto the **ReportHeader** band.
	
	![eurd-win-insert-date-time-add-pageinfo](../../../../images/eurd-win-insert-date-time-add-pageinfo.png)
3. Set the control's **PageInfo** property to *UserName* (e.g. using the smart tag).
	
	![eurd-win-insert-username-set-pageinfo](../../../../images/eurd-win-insert-username-set-pageinfo.png)
4. Next, to apply a format string to the control's contents, type **Current User: {0}** into its **Text Format String** property.
	
	![eurd-win-insert-username-set-formatstring](../../../../images/eurd-win-insert-username-set-formatstring.png)