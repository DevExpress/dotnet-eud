---
title: Calculations
---
# Calculations
**Window calculations** provide the capability to apply specific computations to measure values and allow you to perform different analytical tasks such as computing running totals, percentages of totals, differences, etc.

To create a window calculation, invoke the [Bindings](../ui-elements/dashboard-item-menu.md) menu and click the required measure. In the invoked [Data Item Menu](../ui-elements/data-item-menu.md), go to **Calculations** and select one of the available calculations.

![WebDashboard_CalculationsMenu](../../../images/img126064.png)
* [Percent of Total](#percentoftotal)
* [Running Summary](#runningrummary)
* [Difference](#difference)
* [Percentage Difference](#percentagedifference)
* [Moving](#moving)
* [Rank](#rank)
* [Custom](#custom)

After you have selected the required calculation, you can change its default settings by clicking the **Edit** button (the ![wdd-icon-edit-collection-value-item](../../../images/img126050.png) icon). 
This invokes the special window containing common and specific calculation settings:

## <a name="percentoftotal"/>Percent of Total
A calculation is used to compute a percentage of the total for the specified measure across a window.

![WebDashboard_Calculations_PercentOfTotalSettings](../../../images/img126069.png)
* **Window Definition** specifies a window that limits measure values participating in a calculation. You can choose between the _Predefined_ and _Specific_ window definitions. 
	* For the _Predefined_ window definition, you can specify the **Definition mode** that depends on the dashboard item type.
	* For the _Specific_ window definition, you can manually specify the set of dimensions that fall into the window.
* **Expression** displays an expression generated for the current calculation. To change the expression, click **Edit**.

In the Grid below, **Percent of Total** is applied to a fourth column to show a contribution of individual quarterly sales to total sales.

![WebDashboard_Calculations_PercentOfTotalExample](../../../images/img126094.png)

## <a name="runningrummary"/>Running Summary
Can be used to compute a cumulative total for the specified measure across a window.

![WebDashboard_Calculations_RunningSummarySettings](../../../images/img126070.png)
* **Window Definition** specifies a window that limits measure values participating in a calculation. You can choose between the _Predefined_ and _Specific_ window definitions. 
	* For the _Predefined_ window definition, you can specify the **Definition mode** that depends on the dashboard item type.
	* For the _Specific_ window definition, you can manually specify the set of dimensions that fall into the window.
* **Summary Type** - Specifies a summary function used to apply a calculation.
* The **Expression** displays an expression generated for the current calculation. To change the expression, click **Edit**.

In the Grid below, the **Running Total** is applied to a fourth column to display cumulative sales across all quarters.

![WebDashboard_Calculations_RunningTotalExample](../../../images/img126095.png)

## <a name="difference"/>Difference
Can be used to compute the difference between measure values across a window.

![WebDashboard_Calculations_DifferenceSettings](../../../images/img126071.png)
* **Window Definition** specifies a window that limits measure values participating in a calculation. You can choose between the _Predefined_ and _Specific_ window definitions. 
	* For the _Predefined_ window definition, you can specify the **Definition mode** that depends on the dashboard item type.
	* For the _Specific_ window definition, you can manually specify the set of dimensions that fall into the window.
* **Target** - Specifies the value used to calculate the difference. The following values are available: _Previous_, _Next_, _First_ and _Last_.
* **Difference Type** - Specifies whether the absolute or percentage difference is calculated.
* **Expression** displays an expression generated for the current calculation. To change the expression, click **Edit**.

In the Grid below, the **Difference** is applied to a fourth column to show absolute differences between quarterly sales.

![WebDashboard_Calculations_DifferenceExample](../../../images/img126096.png)

## <a name="percentagedifference"/>Percentage Difference
A calculation is used to compute the difference in percentages between measure values across a window.

![WebDashboard_Calculations_PercentageDifferenceSettings](../../../images/img126072.png)
* **Window Definition** specifies a window that limits measure values participating in a calculation. You can choose between the _Predefined_ and _Specific_ window definitions.
	* For the _Predefined_ window definition, you can specify the **Definition mode** that depends on the dashboard item type.
	* For the _Specific_ window definition, you can manually specify the set of dimensions that fall into the window.
* **Target** - Specifies the value used to calculate the difference. The following values are available: _Previous_, _Next_, _First_ and _Last_.
* **Difference Type** - Specifies whether the absolute or percentage difference is calculated.
* **Expression** displays an expression generated for the current calculation. To change the expression, click **Edit**.

In the Grid below, **Percentage Difference** is applied to a fourth column to show percentage differences between quarterly sales.

![WebDashboard_Calculations_PercentDifferenceExample](../../../images/img126097.png)

## <a name="moving"/>Moving
The Moving calculation uses neighboring values to calculate a total.

![WebDashboard_Calculations_MovingSettings](../../../images/img126073.png)
* **Window Definition** specifies a window that limits measure values participating in a calculation. You can choose between the _Predefined_ and _Specific_ window definitions.
	* For the _Predefined_ window definition, you can specify the **Definition mode** that depends on the dashboard item type.
	* For the _Specific_ window definition, you can manually specify the set of dimensions that fall into the window.
* **Summary Type** - Specifies a summary function used to apply a calculation.
* **Start Offset**/**End Offset** - Specify start/end offsets from the currently processed value. For instance, if you specified offsets as 1/1, the previous and next values will be used along with the current value to apply the Moving calculation.
* The **Expression** displays an expression generated for the current calculation. To change the expression, click **Edit**.

In the Grid below, a **Moving** calculation is applied to a fourth column to show a moving average across all quarters.

![WebDashboard_Calculations_MovingAverageExample](../../../images/img126098.png)

## <a name="rank"/>Rank
Use the Rank calculation to compute rankings for the specified measure across a window.

![WebDashboard_Calculations_RankSettings](../../../images/img126074.png)
* **Window Definition** specifies a window that limits measure values participating in a calculation. You can choose between the _Predefined_ and _Specific_ window definitions.
	* For the _Predefined_ window definition, you can specify the **Definition mode** that depends on the dashboard item type.
	* For the _Specific_ window definition, you can manually specify the set of dimensions that fall into the window.
* **Rank Type** - Specifies the type of ranking. The following ranking types are available: _Unique_, _Competition_, _Dense_, _Modified_ and _Percentile_.
* **Rank Order** - Specifies the order of ranking. You can select _Ascending_ or _Descending_.
* The **Expression** displays an expression generated for the current calculation. To change the expression, click **Edit**.

In the Grid below, a **Rank** calculation is applied to a fourth column to show a ranking of sales for individual quarters.

![WebDashboard_Calculations_RankExample](../../../images/img126099.png)

## <a name="custom"/>Custom
Use Custom to specify a custom calculation by adding the required calculation functions inside the measure expression.

![WebDashboard_Calculations_CustomSettings](../../../images/img126075.png)
* **Window Definition** specifies a window that limits measure values participating in a calculation. You can choose between the _Predefined_ and _Specific_ window definitions.
	* For the _Predefined_ window definition, you can specify the **Definition mode** that depends on the dashboard item type.
	* For the _Specific_ window definition, you can manually specify the set of dimensions that fall into the window.
* The **Expression** allows you to change the expression for the current measure. To change the expression, click **Edit**.