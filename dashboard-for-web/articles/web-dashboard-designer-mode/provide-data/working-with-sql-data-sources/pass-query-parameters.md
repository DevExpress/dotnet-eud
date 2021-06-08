---
title: Pass Query Parameters
author: Natalia Kazakova
legacyId: 117969
---
# Pass Query Parameters
The [Query Builder](../query-builder.md) allows you to [filter queries](filter-queries.md) using parameters. To specify settings of an added query parameter after creating a query, click **Next** in the [Dashboard Data Source Wizard](../dashboard-data-source-wizard.md) dialog.

![wdd-configure-query-parameters](../../../../images/img124954.png)

On the next page, select the query parameter you have created to configure it.

![wdd-configure-query-param-page2](../../../../images/img124955.png)

The following settings are available.
* **Name** - Specifies a parameter's name.
* **Type** - Specifies the parameter's type.
* **Value** - Specifies the parameter's value. If the parameter type is set to _Expression_, invoke the **Expression Editor** dialog using the ellipsis button and specify the required expression. For example, you can use an existing [dashboard parameter](../../data-analysis/dashboard-parameters.md) to pass to the SQL query.

Use **Add** to add a new parameter and the **Remove** button to remove the selected query parameter.

Then, click **Finish** to complete query modifications.