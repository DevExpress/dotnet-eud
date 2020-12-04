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

    - Add the [Report Header](../introduction-to-banded-reports.md) and [Page Header](../introduction-to-banded-reports.md) bands (see the **Manage Report Bands | Add Bands** section in the [Introduction to Banded Reports](../introduction-to-banded-reports.md) document for details)
    - Add [data-bound labels](../use-report-elements/use-basic-report-controls/label.md) to the **Detail** band.

    ![eurd-hierarchical-report-add-controls](../../../images/eurd-hierarchical-report-add-controls.png)

    Switch to [Preview](../preview-print-and-export-reports.md) mode to see an intermediate result.

    ![eurd-hierarchical-report-add-controls-result](../../../images/eurd-hierarchical-report-add-controls-result.png)

1. Specify the Detail band's **Hierarchy Print Options** property.

    ![eurd-hierarchical-report-hierarchyprintoptions](../../../images/eurd-hierarchical-report-hierarchyprintoptions.png)

    Set the following options:

    - **Key Field Name** and **Parent Field Name**, or **Child List Field Name**  
    Set the **Key Field Name** and **Parent Field Name** properties if your report's data has the Id-ParentID related fields.  
    Set the **Child List Field Name** property if your report's data is recursive. Assign the collection of child objects (records) if they have the same type as the parent objects (records).

    - **Indent**  
    Specify the child level node offset.

    - **Keep Together with First Child**  
    Specify whether to print a parent node together with its first child node on the next page if these nodes do not fit at the end of a page.

    ![eurd-hierarchical-report-hierarchyprintoptions-result](../../../images/eurd-hierarchical-report-hierarchyprintoptions-result.png)

    As you can see in the image above, the **Detail** band that contains child rows is printed with the specified indent. However, the row (the sum of the label widths) does not fit the page now.

1. Align labels.

    - Anchor the first data-bound label to the Detail band's left and right edges. Set the label's **Anchor Horizontally** property to **Both**.

        ![eurd-hierarchical-report-anchor](../../../images/eurd-hierarchical-report-anchor.png)

    - Anchor the rest of the data-bound labels to the right edge of the Detail band (their container). Set their **Anchor Horizontal** property to **Right**.

        ![eurd-hierarchical-report-anchor-2](../../../images/eurd-hierarchical-report-anchor-2.png)

    ![eurd-hierarchical-report-anchor-result](../../../images/eurd-hierarchical-report-anchor-result.png)

1. Add a drill-down control to expand/collapse child rows.

    - Add a [Check Box](../use-report-elements/use-basic-report-controls/check-box.md) control to the **Detail** band at the left-most position.

      ![eurd-hierarchical-report-add-checkbox](../../../images/eurd-hierarchical-report-add-checkbox.png)

    - Set the **Check Box** control's glyph options. Use custom glyphs for the *checked* and *unchecked* checkbox states.

        ![HierarchicalReport-CheckBoxProperties](../../../images/eurd-hierarchical-report-checkbox-properties.png)

    - Set the **Detail** band's **Drill Down Control** property to the added **Check Box** control.

        ![HierarchicalReport-SetDrillDownControl](../../../images/eurd-hierarchical-report-drilldown.png)

    - Set the **Check Box**'s **Check State** property to the following expression: *[ReportItems].[Detail].[DrillDownExpanded]*.

        ![HierarchicalReport-CheckStateExpression](../../../images/eurd-hierarchical-report-checkstateexpression.png)

    ![HierarchicalReport-DrillDownControl](../../../images/eurd-hierarchical-report-checkbox-result.png)

7. Sort report data.

    Use the Detail band's **Sort Fields** property to sort data on each hierarchy level.

    ![HierarchicalReport-SortFieldsProperty](../../../images/eurd-hierarchical-report-sort-fields.png)

    ![HierarchicalReport-SortedData](../../../images/eurd-hierarchical-report-sort-fields-result.png)

8. Highlight root nodes.

    To format rows based on their nesting level, use the **CurrentRowHierarchyLevel** variable in expressions. For example, specify the **Detail** band's appearance properties as listed below:

    - Set the **Background Color** property to *iif([DataSource.CurrentRowHierarchyLevel] == 0, Rgb(231,235,244), ?)*
    - Set the **Font | Bold** property to *[DataSource.CurrentRowHierarchyLevel] == 0*

    ![HierarchicalReport-ExpressionVariable](../../../images/eurd-hierarchical-report-expressions.png)

    ![HierarchicalReport-HighlightedRootNodes](../../../images/eurd-hierarchical-report-expressions-result.png)
