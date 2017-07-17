---
title: Conditionally Hide Bands
author: Anya Vekhina
legacyId: 114737
---
# Conditionally Hide Bands
This document provides the sample, illustrating how to hide bands if a certain logical condition is met. Note that no [scripts](../scripting.md) are required to accomplish this task.

To demonstrate this feature, use a report with grouping, similar to the one created in the following tutorial: [Grouping Data](../shaping-data/grouping-data.md).

To conditionally hide bands in a report, do the following.
1. Select the [Group Header](../../report-elements/report-bands.md) band and in the [Properties Panel](../../interface-elements/properties-panel.md), expand the **Appearance** category. Then, expand the **Formatting Rules** section and add a new formatting rule.
	
	![eud-conditionally-hide-bands-0](../../../../images/img119851.png)
2. Expand the newly created rule and set the **Visible** property to **False**. Click the ellipsis button for the rule's **Condition** property to specify the logical condition, which will define band visibility.
	
	![eud-conditionally-hide-bands-1](../../../../images/img119852.png)
3. In the invoked [Expression Editor](../../interface-elements/expression-editor.md), construct the required logical expression (e.g., **[CategoryID] &lt; 2**) and click **Save**.
	
	![eud-conditionally-hide-bands-2](../../../../images/img119853.png)
4. Apply the formatting rule to the Group Header band by enabling the checkbox for this rule.
	
	![eud-conditionally-hide-bands-3](../../../../images/img119854.png)
	
	Then, apply the same formatting rule to the report's Detail band.

Switch your report to the [Preview](../../document-preview.md) mode and view the result.

![eud-conditionally-hide-bands-4](../../../../images/img119855.png)