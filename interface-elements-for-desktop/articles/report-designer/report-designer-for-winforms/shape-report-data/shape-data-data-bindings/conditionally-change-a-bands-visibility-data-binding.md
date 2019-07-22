---
title: Conditionally Change a Band's Visibility
owner: Vera Gorbyliova
seealso: []
---
# Conditionally Change a Band's Visibility

This document describes how to change a report band's visibility.

The report created in this tutorial contains two Detail **sub-bands** with different report controls. These sub-bands are used to display discontinued and current products. 

![1](../../../../../images/conditionally-change-a-bands-visibility.png)

The steps below demonstrate how to change a band's visibility based on a field's value.

1. Create formatting rule(s). 

	- Select a report and click its smart tag. In the invoked actions list, click the ellipsis button for the **FormattingRules** property.
	
		![how-to-conditionally-change-band-visibility-1](../../../../../images/how-to-conditionally-change-band-visibility-124975.png)
	
	- In the invoked **Formatting Rules Editor**, click the **Edit Rule Sheet...** button. The button invokes the **Formatting Rule Sheet Editor**. Click ![Buttons_Plus](../../../../../images/buttons_plus8644.png) to create a new formatting rule.
	
		![](../../../../../images/eurd-web-conditionally-change-a-bands-visibility-add-new-rules.png)
		
		Here, two rules are added.

  	- Specify a condition for the rule. Click the ellipsis button for the rule's **Condition** property. In the invoked **Formatting Rules Editor**, specify the required expression.

		![How to - ConditionallySuppressControls_2](../../../../../images/howto_conditionallysuppresscontrols_28647.png)

	  Here, the **[Discontinued] == true** expression is set for the **formattingRule1**  and the **[Discontinued] == false** expression - for the **formattingRule2**. 
        
	- Specify the **Visible** property for the rule.

        ![](../../../../../images/eurd-web-conditionally-change-a-bands-visibility-set-visibility.png)  

        Here, the **Visible** property is set to **False** for both rules.

	
2. Apply the rule(s) to the required band(s).
 	
	Invoke the **Formatting Rules Editor** for a selected a band and move a rule to the **Rules applied to a control** section.
	
	![](../../../../../images/change-a-bands-visibility-formatting-ruled-editor.png)
	

	Here, the **formattingRule1** is applied to the **SubBand1**, and the **formattingRule2** - to the **SubBand2**.

The Print Preview displays how changes to band visibility influence the Product List. The **SubBand1** is used to display products that have the **Discontinuous** field set to false, and the **SubBand2** is used to display the discontinued products.

![6](../../../../../images/conditionally-change-a-bands-visibility-result.png)
