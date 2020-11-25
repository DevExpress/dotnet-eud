---
title: Bind to a Stored Procedure
---
# Bind to a Stored Procedure

This wizard page allows you to add stored procedures to the data source, configure their parameters and preview the results of a stored procedure’s execution.

![eurd-win-reportwizard-ef-stored-procedure-preview-data](../../../../../../images/eurd-win-reportwizard-ef-stored-procedure-preview-data.png)

To bind to a stored procedure, do the following.
1. Click **Add**. Then, in the invoked window, select a required stored procedure and click **OK**.
	
2. [Configure the parameters](../../../bind-to-data/specify-query-parameters.md) to be passed to the selected stored procedure. Make sure that the value of the passed parameter's **Type** property corresponds to the actual type of the stored procedure parameter.

Click **Next** to proceed to the next wizard page. If you have added more than one stored procedures on this page or if the current Entity Framework model additionally provides data tables, go to the [Select a Data Member](select-a-data-member.md) page.