---
title: 'Report Design Analyzer'
---
# Report Design Analyzer

The Report Design Analyzer shows errors, warnings, and information messages that help users create or enhance a report layout in the [End-User Report Designer](../../report-designer-for-wpf.md).

![Report Design Analyzer panel](../../../images/eurd-report-design-analyzer-wpf.png)

## Invoke the Report Design Analyzer

Do one of the following to invoke the **Report Design Analyzer**:

* Select **Report Design Analyzer** from the **Windows** drop-down menu in the **View** toolbar tab.

    ![View toolbar Windows menu](../../../images/eurd-report-design-analyzer-wpf-invoke-from-toolbar.png)

* Click the bell icon in the status bar.

    ![Bell icon in status bar](../../../images/eurd-report-design-analyzer-wpf-invoke-with-bell.png)

## Filter Messages

Based on their source, report errors are divided into four groups:

* Report layout errors – occur, for example, when report controls overlap each other or extend beyond the report’s printable area.
* Report creation errors – occur while the report document is created. For instance, it might include notifications about invalid property values or unreachable sources of content.
* Report export errors – happen while the report document is exported to PDF, XLSX, and other formats.
* Report script errors – for example, errors in script syntax.

When you invoke a WPF Reporting application, the Report Design Analyzer displays messages from all sources except messages that belong to the Report script errors source.

You can disable messages that belong to a particular source:

![Filter messages by source](../../../images/eurd-report-design-analyzer-wpf-filter-messages.png)

## Fix Issues

Each message contains a recommendation on how to correct an issue. Click the Plus icon in front of the message to expand the recommendation.

![Expand message with recommendation](../../../images/eurd-report-design-analyzer-wpf-expand-message.png)

The message's **Source** column contains a reference to the control or script that caused the issue. Click the reference to navigate to this control or script.

![Navigate to control or script](../../../images/eurd-report-design-analyzer-wpf-navigate-to-control.png)

## Enable Accessibility Validation

Click the **Accessibility** bar item in the UI panel to display accessibility-related issues in the Report Design Analyzer.

![Accessibility validation button](../../../images/report-analyzer-accessibility-validation.png)

Use filters by type and source to navigate long issue lists:

* Like other report design issues, accessibility issues are divided into errors, warnings, and messages. If you deselect the Warnings button, all accessibility warnings will be hidden.
* The source filter allows you to select report controls where issues originate.
