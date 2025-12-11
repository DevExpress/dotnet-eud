---
title: Hierarchical Reports
author: Sergey Andreev
---
# Hierarchical Reports

This tutorial describes how to use the [detail band](../../report-designer/introduction-to-banded-reports.md)'s **Hierarchy Print Options** property to create a hierarchical report.

![eurd-hierarchical-report-result](../../../images/eurd-hierarchical-report-expressions-result.png)

1. [Create a new report](../add-new-reports.md) or [open an existing one](../open-reports.md).

1. [Bind the report](../bind-to-data.md) to a data source.

    ![eurd-hierarchical-report-bind-to-data](../../../images/eurd-hierarchical-report-bind-to-data.png)

    Each record in the data source should include a field that defines the parent-child relationship and thus builds the hierarchy.

1. Arrange controls on the report.

    - Add the [Report Header](../introduction-to-banded-reports.md) and [Page Header](../introduction-to-banded-reports.md) bands (see the **Manage Report Bands | Add Bands** section in the [Introduction to Banded Reports](../introduction-to-banded-reports.md) document for details).

    - Add [data-bound labels](../use-report-elements/use-basic-report-controls/label.md) to the **Detail** band.

    ![eurd-hierarchical-report-add-controls](../../../images/eurd-hierarchical-report-add-controls.png)

    Switch to [PREVIEW](../preview-print-and-export-reports.md) to see an intermediate result.

    ![eurd-hierarchical-report-add-controls-result](../../../images/eurd-hierarchical-report-add-controls-result.png)

1. Switch back to **DESIGN**, select the **Detail** band, and type in "hier" in the **Search field** to navigate to the **Hierarchy Print Options** property pane.

    ![eurd-hierarchical-report-hierarchyprintoptions](../../../images/eurd-hierarchical-report-hierarchyprintoptions.png)

    Set the following options:

    - **Key Field Name** and **Parent Field Name**, or **Child List Field Name**  
    Set the **Key Field Name** and **Parent Field Name** properties if your report's data has the Id-ParentID related fields.  
    Set the **Child List Field Name** property if your report's data is recursive. Assign the collection of child objects (records) if they have the same type as the parent objects (records).

    - **Indent**  
    Specify the child level node offset.

    - **Keep Together with First Child**  
    Specify whether to print a parent node together with its first child node on the next page if these nodes do not fit at the end of a page.

1. Preview the result.

    ![eurd-hierarchical-report-hierarchyprintoptions-result](../../../images/eurd-hierarchical-report-hierarchyprintoptions-result.png)

    As you can see in the image above, the **Detail** band that contains child rows is printed with the specified indent. However, the row (the sum of the label widths) does not fit the page now.

1. Align labels.

    - Anchor the first data-bound label to the Detail band's left and right edges. Set the label's **Anchor Horizontally** property to **Both**.

        ![eurd-hierarchical-report-anchor](../../../images/eurd-hierarchical-report-anchor.png)

    - Anchor the rest of the data-bound labels to the right edge of the Detail band (their container). Set their **Anchor Horizontal** property to **Right**.

        ![eurd-hierarchical-report-anchor-2](../../../images/eurd-hierarchical-report-anchor-2.png)

1. Preview the result.

    ![eurd-hierarchical-report-anchor-result](../../../images/eurd-hierarchical-report-anchor-result.png)

1. Add a **drill-down control** to expand/collapse child rows.
    - Add a [Check Box](../use-report-elements/use-basic-report-controls/check-box.md) control to the **Detail** band at the left-most position.

      ![eurd-hierarchical-report-add-checkbox](../../../images/eurd-hierarchical-report-add-checkbox.png)

    - Set the **Check Box** control's glyph options and remove the unnecessary "checkBox1" text. You can specify different images to indicate the checkbox state. In the **Custom Glyphs** section, specify the ![moveup](../../../images/moveup.png) image for the **Checked** state, and the ![movedown](../../../images/movedown.png) image for the **Unchecked** state.

        ![HierarchicalReport-CheckBoxProperties](../../../images/eurd-hierarchical-report-checkbox-properties.png)

    - Set the **Detail** band's **Drill Down Control** property to the added **Check Box** control.

        ![HierarchicalReport-SetDrillDownControl](../../../images/eurd-hierarchical-report-drilldown.png)

    - Click the **f-button** next to the **Check Box** control to invoke the **Expression Editor**, and assign the following expression to the **Check State** property:
        ```
        Iif( [ReportItems.Detail1.DrillDownExpanded],  'Checked', 'Unchecked')
        ```

        ![HierarchicalReport-CheckStateExpression](../../../images/eurd-hierarchical-report-checkstateexpression.png)

    - Preview the result:

         ![HierarchicalReport-DrillDownControl](../../../images/eurd-hierarchical-report-checkbox-result.png)

1. Sort report data.

    Use the Detail band's **Sort Fields** property to sort data.

    ![HierarchicalReport-SortFieldsProperty](../../../images/eurd-hierarchical-report-sort-fields.png)
    
    Preview the result:

    ![HierarchicalReport-SortedData](../../../images/eurd-hierarchical-report-sort-fields-result.png)

1. Highlight root nodes.

    To format rows based on their nesting level, use the `CurrentRowHierarchyLevel` variable in expressions. Specify the following expressions for the **Detail** band's appearance properties:

    **Background Color**:
    ```
    Iif([DataSource.CurrentRowHierarchyLevel] == 0, Rgb(231,235,244), ?)
    ```
    **Font | Bold**:
    ```
    [DataSource.CurrentRowHierarchyLevel] == 0
    ```

    ![HierarchicalReport-ExpressionVariable](../../../images/eurd-hierarchical-report-expressions.png)

    Preview the result:

    ![HierarchicalReport-HighlightedRootNodes](../../../images/eurd-hierarchical-report-expressions-result.png)
