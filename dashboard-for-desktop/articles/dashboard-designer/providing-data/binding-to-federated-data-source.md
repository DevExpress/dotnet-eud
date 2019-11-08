---
title: Binding to Federated Data Source
author: Margarita Zakhodyaeva
---

# Binding to Federated Data Source
>[NOTE]
>The dashboard should have at least one **SQL**, **Object** or **Excel** data source already connected to it. Otherwise, the **Data Federation** option is not available in the **Data Source Wizard**.

To create a federated data source with the Data Source Wizard, perform the following steps:

1. Click the **New Data Source** button in the **Data Source** ribbon tab.

   ![Choose_new_data_source](../../../images/choose-new-data-source.png)

2. On the first page of the invoked **Data Source Wizard** dialog, select **Data Federation** and click **Next**.

   ![Choose_federated_data_source](../../../images/choose-federated-data-source.png)

3. The [Query Builder](../../dashboard-designer/working-with-data/using-the-query-builder.md) dialog appears that displays the available data sources.

   ![Query_Builder_available_sources](../../../images/query-builder-available-sources.png)

4. Drag-and-drop the data sources, specify the joins and check the columns to include them in the query. When you are finished, click **OK**.

   ![Federated_data_source_settings](../../../images/federated-source-settings.png)

5. The [Data Source Browser](../ui-elements/data-source-browser.md) displays the newly created Federation Data Source:

   ![Federated_data_source_configuration](../../../images/data-source-browser-federated-data-source.png)

    The query name is the same as the root table's name in the query builder. Click the **Rename** button in the **Query** group on the **Data Source** ribbon tab to change the query name.
