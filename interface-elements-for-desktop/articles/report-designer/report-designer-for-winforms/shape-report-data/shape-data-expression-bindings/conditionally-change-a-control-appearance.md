---
title: Conditionally Change a Control's Appearance
author: Anna Gubareva
---
# Conditionally Change a Control's Appearance

This document describes how to change a report control's appearance based on a specific condition.

> [!Warning]
> Use the approach below if expression bindings **are enabled** in the Report Designer (the [Property Grid](../../report-designer-tools/ui-panels/property-grid.md) provides the **Expressions** ![](../../../../../images/eurd-win-property-grid-expressions-icon.png) tab ).
>
> See [Conditionally Change a Control's Appearance](../shape-data-data-bindings/conditionally-change-a-control-appearance.md) if expression bindings **are not enabled** in the Report Designer (the [Property Grid](../../report-designer-tools/ui-panels/property-grid.md) does not provide the **Expressions** ![](../../../../../images/eurd-win-property-grid-expressions-icon.png) tab).

1. Switch to the [Report Explorer](../../report-designer-tools/ui-panels/report-explorer.md) and right-click the **Styles** category to create a new visual style.
	
	![](../../../../../images/eurd-win-shaping-create-new-report-style.png)

2. Right-click the created style and select **Edit Styles**.
	
	![](../../../../../images/eurd-win-shaping-edit-report-styles.png)

3. In the invoked **Styles Editor**, customize the created style's appearance settings.
	
	![](../../../../../images/eurd-win-shaping-customize-style-settings.png)

4. Create another style by cloning the existing one.
	
	![](../../../../../images/eurd-win-shaping-clone-a-style.png)

5. Customize the new style's appearance settings and close the editor.
	
	![](../../../../../images/eurd-win-shaping-cloned-style-settings.png)

6. Back in the Report Explorer, select a report element to which you wish to assign the created styles.
	
	![](../../../../../images/eurd-win-shaping-select-element-in-report-explorer.png)

7. Switch to the **Expressions** section in the [Property Grid](../../report-designer-tools/ui-panels/property-grid.md) and click the ellipsis button for the control's **Style Name** property.
	
	![](../../../../../images/eurd-win-shaping-style-name-expression-property.png)

8. In the invoked **Expression Editor**, specify the required condition for switching between the created styles.
	
	![](../../../../../images/eurd-win-shaping-style-name-expression.png)

Switch to [Print Preview](../../preview-print-and-export-reports.md) to view the resulting report.

![](../../../../../images/eurd-win-shaping-change-appearance-result.png)