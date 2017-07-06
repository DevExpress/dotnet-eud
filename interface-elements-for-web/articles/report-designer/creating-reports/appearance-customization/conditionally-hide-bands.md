---
title: Conditionally Hide Bands
---
# Conditionally Hide Bands
This document provides the sample, illustrating how to hide bands if a certain logical condition is met. Note that no [scripts](../../../../../interface-elements-for-web/articles/report-designer/creating-reports/scripting.md) are required to accomplish this task.

To demonstrate this feature, use a report with grouping, similar to the one created in the following tutorial: [Grouping Data](../../../../../interface-elements-for-web/articles/report-designer/creating-reports/shaping-data/grouping-data.md).

To conditionally hide bands in a report, do the following.
1. Select the [Group Header](../../../../../interface-elements-for-web/articles/report-designer/report-elements/report-bands.md) band and in the [Properties Panel](../../../../../interface-elements-for-web/articles/report-designer/interface-elements/properties-panel.md), expand the **Appearance** category. Then, expand the **Formatting Rules** section and add a new formatting rule.
	
	![eud-conditionally-hide-bands-0](../../../../images/Img119851.png)
2. Expand the newly created rule and set the **Visible** property to **False**. Click the ellipsis button for the rule's **Condition** property to specify the logical condition, which will define band visibility.
	
	![eud-conditionally-hide-bands-1](../../../../images/Img119852.png)
3. In the invoked [Expression Editor](../../../../../interface-elements-for-web/articles/report-designer/interface-elements/expression-editor.md), construct the required logical expression (e.g., **[CategoryID] &lt; 2**) and click **Save**.
	
	![eud-conditionally-hide-bands-2](../../../../images/Img119853.png)
4. Apply the formatting rule to the Group Header band by enabling the checkbox for this rule.
	
	![eud-conditionally-hide-bands-3](../../../../images/Img119854.png)
	
	Then, apply the same formatting rule to the report's Detail band.

Switch your report to the [Preview](../../../../../interface-elements-for-web/articles/report-designer/document-preview.md) mode and view the result.

![eud-conditionally-hide-bands-4](../../../../images/Img119855.png)