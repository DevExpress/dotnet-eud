---
title: Display the Current Date and Time in a Report
---
# Display the Current Date and Time in a Report

This tutorial demonstrates how to insert the current system date and time into a report using the [PageInfo](..\use-report-elements\use-basic-report-controls\page-info.md) control.

![eurd-win-insert-datetime-result](../../../../images/eurd-win-insert-datetime-result.png)

Do the following to include information about the current date and time into a report:

1. Typically, the current date and time are displayed within the [Report Header](..\introduction-to-banded-reports.md) band. To add it to the report, right click anywhere on the report's surface. In the invoked menu, point to **Insert Band** and click **ReportHeader**.
	
	![eurd-win-insert-datetime-add-reportheader-band](../../../../images/eurd-win-insert-datetime-add-reportheader-band.png)
2. Drop the [PageInfo](..\use-report-elements\use-basic-report-controls\page-info.md) control from the [Toolbox](..\report-designer-tools\toolbox.md) onto the **ReportHeader** band.
	
	![eurd-win-insert-date-time-add-pageinfo](../../../../images/eurd-win-insert-date-time-add-pageinfo.png)
3. Set the control's **PageInformation** property to *DateTime* (e.g. using the smart tag).
	
	![eurd-win-insert-datetime-set-pageinfo](../../../../images/eurd-win-insert-datetime-set-pageinfo.png)
4. To apply a format string to the control's contents, type **Created at {0:h:mm tt dd MMMM yyyy}** into its **TextFormatString** property.
	
	![eurd-win-insert-datetime-set-formatstring](../../../../images/eurd-win-insert-datetime-set-formatstring.png)