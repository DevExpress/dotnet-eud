---
title: 'Report Design Analyzer'
---
# Report Design Analyzer

The **Report Design Analyzer** shows errors, warnings, and information messages that help you to detect and fix issues in a report.

image goes here...

## Invoke the Report Design Analyzer

Do one of the following to invoke the **Report Design Analyzer**:

* Select **Report Design Analyzer** from the **Windows** drop-down menu in the **View** toolbar tab.

    ![](../../../../../images/eurd-report-design-analyzer-invoke-from-toolbar.png)

* Click the bell icon in the status bar.

    ![](../../../../../images/eurd-report-design-analyzer-invoke-with-bell.png)

## Fix Issues

Each message contains a recommendation on how to fix an issue. Click the Plus icon in front of the message to expand the recommendation.

image goes here...

The **Source** column contains a reference to the control or script that caused the issue. Click the reference to navigate to this control or script.

image goes here...

## Filter Messages by Source

Based on their source, report errors are divided into four groups:

* Report layout errors – occur, for example, when report controls overlap each other or extend beyond the report’s printable area.
* Report creation errors – occur while the report document is created. For instance, it might include notifications about invalid property values or unreachable sources of content.
* Report export errors – happen while the report document is exported to PDF, XLSX, and other formats.
* Report script errors (this group is not displayed if report scripts are disabled in your application) – for example, errors in script syntax.

You can disable messages that belong to a particular source:

image goes here...

## Filter Messages by Type

You can enable/disable messages of each available type ("Error", "Warning", or "Information") or any combination of them. Click the panel in the UI as shown in the image below to enable/disable messages of a corresponding type.

image goes here...

# Report Design Analyzer (Old)

The Report Design Analyzer shows errors, warnings, and information messages that help users create or enhance a report layout in the [Report Designer](../../../report-designer-for-winforms.md).

![](../../../../../images/eurd-report-design-analyzer-win.png)

## Invoke the Report Design Analyzer

Do one of the following to invoke the **Report Design Analyzer**:

* Select **Report Design Analyzer** from the **Windows** drop-down menu in the **View** toolbar tab.

    ![](../../../../../images/eurd-report-design-analyzer-invoke-from-toolbar.png)

* Click the bell icon in the status bar.

    ![](../../../../../images/eurd-report-design-analyzer-invoke-with-bell.png)

## Filter Messages

You can filter messages by one of the following categories:

![](../../../../../images/eurd-report-design-analyzer-filter-messages.png)

* **Report Layout**

    Layout-related messages (for instance, in cases when report controls overlap each other or extend beyond the report's printable area).

* **Report Creation**

    Messages about report creation (for instance, notifications about invalid property values or unreachable sources of content).

* **Report Scripts**

    Messages that highlight issues in report scripts (for instance, errors in script syntax).

* **All**

    All of the above-mentioned messages.

## Correct the Issues

Each message contains a recommendation on how to correct an issue. Click the Plus icon in front of the message to expand the recommendation.

![](../../../../../images/eurd-report-design-analyzer-expand-message.png)

The message's **Source** column contains a reference to the control or script that caused the issue. Click the reference to navigate to this control or script.

![](../../../../../images/eurd-report-design-analyzer-navigate-to-control.png)
