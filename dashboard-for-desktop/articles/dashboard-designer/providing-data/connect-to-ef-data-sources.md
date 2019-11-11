---
title: Connect to EF Data Sources
author: Margarita Zakhodyaeva
---
# Connect to EF Data Sources

To bind a dashboard to an Entity Framework data source from the current project, do the following.

1. Click the **New Data Source** button in the **Data Source** ribbon tab.

   ![Choose_new_data_source](../../../images/choose-new-data-source.png)

2. On the first page of the invoked **Data Source Wizard** dialog, select **Entity Framework** and click **Next**.

   ![ef_data_source_wizard](../../../images/ef-data-sourse-wizard.png)

3. On the next page, select the available data context and click **Next**.

   ![select_required_connection](../../../images/select-required-connection.png)

4. On the final page, choose the connection string corresponding to the selected data context and click **Finish**.

   ![choose_connection_string](../../../images/choose-connection-string.png)

   If the application configuration file does not contain the required connection string, or you need to specify the connection string manually, select **No, specify a custom connection string** and click **Next**.

   ![specify_a_connection_string](../../../images/specify-a-connection-string.png)

   On this page, specify a custom connection string and click **Finish**. This creates the data source and displays its fields in the [Data Source Browser](../ui-elements\data-source-browser.md).
