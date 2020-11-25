---
title: Stored Procedures
author: Natalia Kazakova
legacyId: 114170
---
# Stored Procedures
If you use a stored procedure to supply the dashboard with data, you should specify the stored procedure parameters. In the [Query Editor](using-the-query-editor.md) dialog, select the required stored procedure and click **Next**.

![QueryEditorDialog_StoredProcedure](../../../images/img118171.png)

On the next page, you can specify the parameter settings.

![QueryEditorDialog_StoredProcedureParameters](../../../images/img118172.png)
* **Name** - Displays the parameter name.
* **Type** - Displays the parameter type.
* **Expression** - Specifies whether the expression is used to specify a parameter value.
* **Value** - Specifies a parameter value. If the **Expression** check box is checked, you can invoke the **Expression Editor** dialog to specify the required [expression](../../dashboard-designer/data-analysis/expression-constants-operators-and-functions.md) or select an existing [dashboard parameter](../data-analysis/using-dashboard-parameters.md) to use it as a stored procedure parameter.

Click the [Preview...](preview-data.md) button to preview the query result. Then, click **Finish** to complete query modifying.