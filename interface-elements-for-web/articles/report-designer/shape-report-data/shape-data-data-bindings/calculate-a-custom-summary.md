---
title: Calculate a Custom Summary
author: Anna Vekhina
---
# Calculate a Custom Summary

This tutorial describes the steps required to calculate a custom summary that is not one of the built-in summary functions.

> [!Warning]
> Use the approach below if expression bindings **are not enabled** in the Report Designer (the Designer does not provide the [Expressions](../../report-designer-tools/ui-panels/expressions-panel.md) panel).
>
> See [Calculate an Advanced Summary](../shape-data-expression-bindings/calculate-an-advanced-summary.md) if expression bindings **are enabled** in the Report Designer (the Designer provides the [Expressions](../../report-designer-tools/ui-panels/expressions-panel.md) panel).

1. [Create a new report](../../add-new-reports.md) or open an existing one and [bind it to a data source](../../bind-to-data.md).

2. Insert the [Group Header](../../introduction-to-banded-reports.md) band, select the **Group Fields** section in the **Actions** category and add a new group field to group the report's data by the required field. 

    ![](../../../../images/eurd-web-label-legacy-custom-summary-group-data.png)

3. Insert the Group Footer band. Drop a required data field onto the group footer to display the summary result. 

4. Select the label, expand the **Summary** section in the **Actions** category and set the **Running** property to **Group**. Set the **Function** property to **Custom** and use the **Format String** property to format the summary's value.

    ![](../../../../images/eurd-web-label-legacy-custom-summary-settings.png)

5. When selecting the **Custom** option, three more events are added to the available events' drop-down list: **Summary Get Result**, **Summary Reset** and **Summary Row Changed**.

    ![](../../../../images/eurd-web-label-legacy-custom-summary-scripts.png)

    You can handle these events in the following way using the [Script Editor](../../report-designer-tools/script-editor.md).

    **C#**

    ```csharp

    // Declare a summary and a pack.
    double totalUnits = 0;
    double pack = 15;

    private void OnSummaryReset(object sender, System.EventArgs e) {
        // Reset the result each time a group is printed.
        totalUnits = 0;
    }

    private void OnSummaryRowChanged(object sender, System.EventArgs e) {
        // Calculate a summary.
        totalUnits += Convert.ToDouble(GetCurrentColumnValue("UnitsOnOrder"));
    }

    private void OnSummaryGetResult(object sender, 
    DevExpress.XtraReports.UI.SummaryGetResultEventArgs e) {
        // Round the result, so that a pack will be taken into account 
        // even if it contains only one unit.
        e.Result = Math.Ceiling(totalUnits / pack);
        e.Handled = true;
    }

    ```
    **VB.NET**

    ```vb

    ' Declare a summary and a pack.
    Private totalUnits As Double = 0
    Private pack As Double = 15

    Private Sub OnSummaryReset(ByVal sender As Object, ByVal e As System.EventArgs)
        ' Reset the result each time a group is printed.
        totalUnits = 0
    End Sub

    Private Sub OnSummaryRowChanged(ByVal sender As Object, ByVal e As System.EventArgs)
        ' Calculate a summary.
        totalUnits += Convert.ToDouble(GetCurrentColumnValue("UnitsOnOrder"))
    End Sub

    Private Sub OnSummaryGetResult(ByVal sender As Object,  _ 
    ByVal e As DevExpress.XtraReports.UI.SummaryGetResultEventArgs)
        ' Round the result, so that a pack will be taken into account 
        ' even if it contains only one unit.
        e.Result = Math.Ceiling(totalUnits / pack)
        e.Handled = True
    End Sub

    ```

Switch to [Print Preview](../../preview-print-and-export-reports.md) to see the result.

![](../../../../images/eurd-web-label-advanced-summary-result.png)