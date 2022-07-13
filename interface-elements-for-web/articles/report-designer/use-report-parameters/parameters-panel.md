---
title: The Parameters Panel
author: Eugene Polevikov
---

# The Parameters Panel

The **Parameters** panel allows you to specify parameter values in a report's **Print Preview**.

![Use the Parameters panel to specify parameter values](../../../images/eurd-web-parameters-panel.png)

## Submit Parameter Values

When you open a report's **Print Preview**, the **Parameters** panel displays default parameter values and descriptions.

![Parameters panel, "Waiting for parameter values" message](../../../images/parameters-panel-waiting-for-parameter-values-message.png)

Specify parameter values and click **Submit** to generate the report's **Print Preview**. Set the report's **RequestParameters** property to **false** to display a report document for the default parameter values when you open the **Print Preview**.

## Reset Parameter Values to Defaults

Click the **Reset** button to reset parameter values to defaults. 

![Reset parameter values to defaults](../../../images/parameters-panel-reset-values-to-defaults.png)

## Hide the Parameters Panel

To remove the **Parameters** panel from a report's **Print Preview**, disable the **Visible** option for all report parameters in the **Report Parameters Editor**.

![Hide a parameter from the Parameters panel](../../../images/hide-parameter-from-parameters-panel.png)

When you hide the **Parameters** panel, the report's **Print Preview** is generated with the default parameter values.

## Customize the Parameters Panel

You can unite report parameters into expandable groups, place parameters side-by-side, add separators, and more.

| Default panel | Customized panel |
| ----------- | ----------- |
| ![](../../../images/default-parameters-panel-1.png) | ![](../../../images/customized-parameters-panel-1.png) |

### Use the Report Parameters Editor

Select the **Parameters** item in the **Field List** and click the **Edit parameters** button.

![](../../../images/invoke-report-parameters-editor.png)

This action invokes the **Report Parameters Editor**.

![](../../../images/edit-parameters-window.png)

Use the menu on the left to create and customize parameters, groups, and separators.

#### Customize a Parameter

Specify the **Orientation** property to choose the position of a parameter label relative to an editor.

![](../../../images/specify-label-orientation.png)

| Label orientation = Horizontal (Default) | Label orientation = Vertical |
| ----------- | ----------- |
| ![](../../../images/label-orientation-horizontal.png) | ![](../../../images/label-orientation-vertical.png) |

#### Create and Customize a Group

Click the **Add group** button to create a new group.

![](../../../images/report-parameters-editor-create-new-group.png)

Use the **Up** and **Down** buttons to change the order of parameters and groups, and place parameters inside or outside a group.

![](../../../images/report-parameters-editor-setup-elements-order.png)

You can also drag-and-drop parameters and groups inside the menu to achieve the same result.

![](../../../images/report-parameters-editor-drag-and-drop-elements-in-menu.png)

To customize a group, select it and use its editors on the right to set up the group appearance. The following example unites the **customerName** and **companyName** parameters into a group called **Select a customer**.

![](../../../images/report-parameters-editor-group-customization-options.png)

| Default panel | Panel with a group |
| ----------- | ----------- |
| ![](../../../images/default-parameters-panel-1.png) | ![](../../../images/customized-parameters-panel-2.png) |

Besides a title, you can also specify the following properties to customize the group appearance:

* Orientation (specifies whether to place parameters inside the group vertically or horizontally).
* Show title
* Show borders
* Show expand/collapse button
* Expanded

#### Add a Separator

Click the **Add separator** button to create a separator.

![](../../../images/report-parameters-editor-create-separator.png)

Similar to parameters and groups, you can use the **Up** and **Down** buttons or drag-and-drop separators inside the menu to specify the location for these separators relative to other elements.

![](../../../images/report-parameters-editor-specify-location-for-separator.png)

The example below shows the **Parameters** panel with a separator between the **Company Name** and **Customer Name** parameters.

| Default panel | Panel with a separator |
| ----------- | ----------- |
| ![](../../../images/default-parameters-panel-3.png) | ![](../../../images/customized-parameters-panel-3.png) |