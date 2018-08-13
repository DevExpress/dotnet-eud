---
title: Parameters Overview
author: Anna Gubareva
---
# Parameters Overview

You can use report parameters to pass data to a report before it has been published. Parameter values are specified in a Print Preview's **Parameters** panel.

## <a name="createparameters"></a>Create Parameters
To create a report parameter, switch to the [Field List](../../report-designer-tools/ui-panels/field-list.md), right-click the **Parameters** node and click **Add Parameter** in the context menu.

![](../../../../../images/eurd-win-parameters-add-parameter-via-field-list.png)

Alternatively, you can click the **Add Parameter** button in the [Toolbar](../../report-designer-tools/toolbar.md)'s **Home** tab.

![](../../../../../images/eurd-win-parameters-add-parameter-via-toolbar.png)

This invokes the **Add New Parameter** dialog where you can customize the created parameter.

![](../../../../../images/eurd-win-parameters-add-new-parameter-dialog.png)

This dialog provides the following options:

* **Name** - specifies the unique name by which the parameter can be referred to.
* **Description** - specifies the text that will be displayed in a Print Preview along with the corresponding value editor.
* **Type** - specifies the parameter's value type, according to which an appropriate value editor is displayed in a Print Preview.
* **Default value** - specifies the default parameter value.
* **Show in the parameters panel** (corresponds to the parameter's **Visible** property) - enable this option to request the parameter value in a Print Preview. Otherwise, the default parameter value is silently passed to the report.
* **Supports the collection of standard values** - you can enable this option if the parameter is visible (i.e., its value should be requested in a Print Preview). In this case, you can choose a value from a predefined list. You can either manually populate this list with possible values, or specify a data source from where these values should be obtained.
	
	* **Dynamic values**
		
		On this tab, you can specify a data source, data adapter (if required) and data member storing parameter values. The value member defines a data field that will provide values to the parameter. The display member defines a data field storing values displayed in a Print Preview.
		
		![](../../../../../images/eurd-win-parameters-dynamic-values.png)
		
		The value type of the specified data member should match the specified parameter type.
		
		You can filter the list of values by specifying the **Filter String** property. Using this property, you can implement [cascading parameters](create-multi-value-and-cascading-parameters.md).
		
	* **Static values**
		
		Switch to this tab to specify a static list of possible values. Each value should have a description that is displayed in a Print Preview.
		
		![](../../../../../images/eurd-win-parameters-static-values.png)

* **Allow multiple values** (corresponds to the parameter's **Multi-Value** property) - when this option is enabled, a parameter can be assigned a [collection of values](create-multi-value-and-cascading-parameters.md).

## <a name="useparameters"></a>Use Parameters
You can use report parameters to solve the following tasks:

* **Filter Data**
	
	When [filtering report data](../filter-data/filter-data-at-the-report-level.md), parameters can be used for providing values to a report's **Filter String** property.
	
	![](../../../../../images/eurd-win-parameters-in-filter-string.png)
	
	When [filtering data at the level of a data source](../filter-data/filter-data-at-the-data-source-level.md), you can link report parameter to [query parameters](use-query-parameters.md) that are used in the SELECT statement of a SQL string.

* **Bind to Data**
	
	You can bind a report control to a parameter and display its value in the report. To create a new label bound to a parameter, drag the parameter from the [Field List](../../report-designer-tools/ui-panels/field-list.md) and drop it onto the required band.
	
	![](../../../../../images/eurd-win-parameters-for-data-binding.png)
	
	When using [mail merge](../../bind-to-data/use-embedded-fields-mail-merge.md), you can refer to a parameter by adding the **Parameters.** prefix before its name.

* **Specify Expressions**
    
    Parameters can be used as part of [expressions](../../use-expressions.md). To refer to a report parameter, use the **Parameters.** prefix before its name.

    ![](../../../../../images/eurd-win-parameters-in-expression-editor.png)