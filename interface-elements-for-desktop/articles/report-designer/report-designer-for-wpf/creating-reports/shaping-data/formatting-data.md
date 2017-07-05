---
title: Formatting Data
---
This topic describes how to change value formatting of [report elements](../../../../../../interface-elements-for-desktop/articles/report-designer/report-designer-for-wpf/report-elements/report-controls.md) in the Report Designer. For instance, you can format a numeric value as a currency, display a date/time value in one of the standard forms depending on the culture, etc.

To apply value formatting for a [data-bound control](../../../../../../interface-elements-for-desktop/articles/report-designer/report-designer-for-wpf/creating-reports/providing-data/binding-report-controls-to-data.md)'s content, do the following.
1. Right-click the control, and select **Edit...** in the context menu. In the invoked dialog, click the ellipsis button for the **Format String** property.
	
	![EUD_WpfReportDersigner_Formatting_1](../../../../../images/Img123603.png)
2. In the invoked **Format String Editor**, select one of the predefined standard formats or specify a custom one.
	
	![EUD_WpfReportDersigner_Formatting_2](../../../../../images/Img123604.png)
	
	To quit the dialog and apply the changes, click **OK**.

In a similar way, you can apply formatting to a control's **Bookmark**, **Navigation URL** and **Tag** properties using the [Properties Panel](../../../../../../interface-elements-for-desktop/articles/report-designer/report-designer-for-wpf/interface-elements/properties-panel.md). Note that the set of bindable properties depends on the control type.

![EUD_WpfReportDersigner_Formatting_3](../../../../../images/Img123607.png)

When a summary function is applied to a control's dynamic content, value formatting is specified separately as described in the [Calculating Summaries](../../../../../../interface-elements-for-desktop/articles/report-designer/report-designer-for-wpf/creating-reports/shaping-data/calculating-summaries.md) document.

Independently from general and summary value formatting, you can specify a native XSLX format string, which is preserved when the report is exported to XLSX. You can do this using a control's **Xlsx Format String** property.