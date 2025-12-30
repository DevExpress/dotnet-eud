---
title: Requesting Parameter Values
author: Natalia Kazakova
legacyId: 16726
---
# Requesting Parameter Values
The **Web Dashboard** provides a built-in **Dashboard Parameters** dialog, which allows you to change dashboard parameter values.

To invoke the **Dashboard Parameters** dialog, click the **Parameters** button (the ![Parameters_ParametersButtonWin_Title](../../images/img21814.png) icon) in the [dashboard title](../data-presentation/dashboard-layout.md).

![Parameters_DashboardParametersDialog_Web](../../images/img21818.png)

Select the required parameter values and click the **Submit** button to apply the changes. To reset changes to the default values, click the **Reset** button.

## Request Parameter Values before Data Loading

If you see a Dashboard Parameters window at startup, you need to input parameter values before a dashboard loads and aggregates data. Dashboard items display the following message: "Waiting for Parameter Values…".

![dashboard-parameter-request-before-loading](~/eud-for-bi-dashboard/dashboard-for-web/images/dashboard-parameter-request-before-loading.png)

The Web Dashboard control loads data only after you submit all visible parameters. The dashboard displays a Dashboard Parameters pop-up before it fetches data. This operation mode prevents unnecessary data requests and ensures the dashboard fetches only data you actually need. 

To change this mode, open the [dashboard menu](../../web-dashboard-designer-mode/ui-elements/dashboard-menu.md) in Designer Mode, switch to the **Parameters** page, and use the following checkbox: **Request Parameter Values before Data Loading**. The setting value is saved in the dashboard XML definition.